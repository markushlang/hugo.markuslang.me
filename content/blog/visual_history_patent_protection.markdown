---
title: "A Visual History of Patent Protection"
date: '2021-09-03'
categories:
- R
- visualization
- patent
footnotes: no
htmlwidgets: no
mathjax: no
---

I noticed that most articles in economic journals avoid to visualize the scores of patent rights indexes. But doing so is quite helpful to understand how patentability, compulsory licensing and patent terms have changed over time. 

### Patent Rights Index

The following graphs are based on the widely used patent rights index by [Park and colleagues](http://fs2.american.edu/wgp/www/2EFWch2.pdf). This index is available for 122 countries over 55 years and consist of five main categories: 

1. coverage +
2. membership + 
3. loss of rights + 
4. duration +
5. enforcement

### Coverage

A country has high coverage, according to the index, if it grants more patents for formerly unpatentable „technologies“:

1) pharmaceuticals,
2) chemicals,
3) food,
4) plant and animal varieties,
5) surgical products,
6) microorganisms, and
7) utility models (somewhat problematic)

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/coverage.png" alt="coverage" caption="Patent Rights Index (Category: Coverage), 1960-2015" %}}

### Membership

Park and colleagues assume that membership in the following international agreements generally equals higher protection: 

1. [Paris Convention](https://www.wipo.int/treaties/en/ip/paris/)
2. [PCT](https://www.wipo.int/pct/en/)
3. [UPOV](https://www.upov.int/portal/index.html.en)
4. [TRIPS](https://www.wto.org/english/tratop_e/trips_e/trips_e.htm)

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/membership.png" alt="membership" caption="Patent Rights Index (Category: Membership), 1960-2015" %}}

### Loss of Rights 

An additional assumption of the index is that countries without (!) the following provisions provide higher protection to patent owners:

1) working requirements 
2) compulsory licensing requirements 
3) straightout revocation

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/loss_of_rights.png" alt="loss_of_rights" caption="Patent Rights Index (Category: Loss of Rights), 1960-2015" %}}

### Patent Term

To determine whether the patent term in a given country is long or short, the index compares available years to the "appropriate maximal term of protection". If a country allows 15 years of protection, but could have allowed 20, it receives a score of 0.75  (15 years/20 years).

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/duration.png" alt="duration" caption="Patent Rights Index (Category: Duration), 1960-2015" %}}

### Enforcement 

Does country x make the following enforcement mechanisms available to patent owners? 

1. preliminary injunctions
2. contributory infringements
3. burden-of-proof reversals

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/enforcement.png" alt="enforcement" caption="Patent Rights Index (Category: Enforcement), 1960-2015" %}}

### Overall 

The final index just sums up the scores across all five categories to get overall scores for each country.

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/overall.png" alt="overall" caption="Patent Rights Index (Overall), 1960-2015" %}}

### Yearly Averages

Heatmaps are helpful to explore timeseries of individual countries over time. To be able to spot more general averages, I have also plotted yearly averages.

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/averages.png" alt="averages" caption="Patent Rights Index (Cross-Country Averages)" %}}

### Code

Code (+data) is available here: [https://github.com/markushlang/patent_rights_index](https://github.com/markushlang/patent_rights_index)
