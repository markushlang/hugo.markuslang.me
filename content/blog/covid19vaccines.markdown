---
title: "Covid-19 Vaccines"
date: 2020-04-12T13:18:50-04:00
categories: [R,visualization,covid19]
footnotes: false
htmlwidgets: false
mathjax: false
---

For a few weeks I have tried to keep up with the [draft vaccine landscape documents](https://www.who.int/blueprint/priority-diseases/key-action/Novel_Coronavirus_Landscape_nCoV_11April2020.PDF) published by the WHO. I figured that if I do this work anyway I might as well bundle the dataset in an R package. The package is called [`covid19vaccines`](https://markushlang.github.io/covid19vaccines/) and contains various updates of the WHO Draft Landscape in a tidy table.

The [package homepage](https://github.com/markushlang/covid19vaccines) has installation details and an example. I also added a [Shiny web app](https://markushlang.shinyapps.io/covid19vaccines/) that makes it somewhat easier to filter through the table.

{{% figure src="https://markuslang.me/files/misc/covid19vaccines_app.png" alt="Covid-19 Vaccines" caption="Screenshot of the covid19vaccines Shiny app" %}}

I hope to be able to update the package each week. In building the package I profited from a number of sources:

This [post](http://www.davekleinschmidt.com/r-packages/) by David F. Kleinschmidt.

Kieran Healy's beautifully simple [nycdogs](http://kjhealy.github.io/nycdogs) package.
