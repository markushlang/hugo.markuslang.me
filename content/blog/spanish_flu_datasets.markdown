---
title: "Spanish Flu Datasets"
date: 2020-04-15T13:18:50-04:00
categories: [R,visualization,covid19]
footnotes: false
htmlwidgets: false
mathjax: false
---

I have bundled a few datasets mentioned in Alfred W. Crosby’s (2003) book [“America’s Forgotten Pandemic”](https://www.amazon.com/Americas-Forgotten-Pandemic-Influenza-1918/dp/0521541751) into an R package. In addition to Crosby’s data, I have also added data on non-pharmaceutical interventions by larger U.S. cities during the 1918 and 1919 outbreak from [Howard Markel and colleagues](https://jamanetwork.com/journals/jama/fullarticle/208354).

The [`spanishflu` package](https://github.com/markushlang/spanishflu) can be used to create figures similar to current [COVID-19 figures](https://www.ft.com/coronavirus-latest).

This is a small example on how to do that:

{{< highlight r >}}

# load packages
library(pacman)
pacman::p_load("tidyverse","lubridate","ggrepel","paletteer","scales","prismatic")
pacman::p_load_gh("markushlang/spanishflu")

# prepare cumulative counts
flu_curve <- deaths_registered_in_certain_cities %>%
  select(date,city,deaths) %>%
  group_by(city) %>%
  arrange(date) %>%
  mutate(deaths = ifelse(is.na(deaths),0,deaths)) %>%
  mutate(cu_deaths = cumsum(deaths)) %>%
  filter(cu_deaths > 9) %>%
  mutate(days_elapsed = date - min(date),
         end_label = ifelse(date == max(date), city, NA))

# create cumulative deaths plot
flu_curve %>%
  filter(city %in% c("New York","Philadelphia","Chicago",
                     "Boston","Pittsburgh")) %>%
  ggplot(mapping = aes(x = days_elapsed, y = cu_deaths,
         color = city, label = end_label,
         group = city)) +
  geom_line(size = 0.8) +
  geom_text_repel(nudge_x = 1.1,
                  nudge_y = 0.1,
                  segment.color = NA) +
  guides(color = FALSE) +
  theme_minimal() +
  scale_color_manual(values = prismatic::clr_darken(paletteer_d("jcolors::default"), 0.2)) +
  scale_y_continuous(labels = scales::comma_format(accuracy = 1),
                     trans = "log2") +  
  labs(x = "Days Since 10th Confirmed Death",
       y = "Cumulative Number of Deaths (log scale)",
       title = "Cumulative Deaths from the Spanish Flu, Selected U.S. Cities") +
    theme(plot.title = element_text(size = rel(1), face = "bold"),
          axis.text.y = element_text(size = rel(1)),
          axis.title.x = element_text(size = rel(0.75)),
          axis.title.y = element_text(size = rel(0.75)),
          axis.text.x = element_text(size = rel(1)),
          legend.text = element_text(size = rel(1))
          )

{{< /highlight >}}

{{% figure src="https://github.com/markushlang/spanishflu/raw/master/man/figures/README-example-1.png" alt="Cummulative Deaths from the Spanish Flu" caption="Selected U.S. Cities" %}}
