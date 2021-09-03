---
title: "A Visual History of Patent Protection"
date: '2021-09-03T13:18:50-04:00'
categories:
- R
- visualization
- patent
footnotes: no
htmlwidgets: no
mathjax: no
---

I noticed that most articles in economic journals avoid to visualize the scores of patent rights indexes. 

But doing so is quite helpful to understand how much patentability, compulsory licensing and patent terms have changed over time. 

The following graphs are based on the widely used patent rights index by Park and colleagues. This index is available for 122 countries over 55 years and consist of five main categories: 

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
7) utility models (weird)

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/coverage.png" alt="coverage" caption="" %}}

---

### Membership

Park and colleagues assume that membership in the following international agreements generally equals higher protection: 

Paris Convention
PCT
UPOV
TRIPS

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/membership.png" alt="membership" caption="" %}}

---

### Loss of Rights 

An additional assumption of the index is that countries without (!) the following provisions provide higher protection to patent owners:

1) working requirements 
2) compulsory licensing requirements 
3) straightout revocation

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/loss_of_rights.png" alt="loss_of_rights" caption="" %}}

### Patent Term

To determine whether the patent term in a country is long or short, the index compares available years to the „appropriate maximal term of protection“.  

If a country allows 15 years of protection, but could have allowed 20, it receives a score of 0.75  (15/20).

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/duration.png" alt="duration" caption="" %}}

### Enforcement 

Does country x make the following enforcement mechanisms available to patent owners? 

a) preliminary injunctions
b) contributory infringements
c) burden-of-proof reversals

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/enforcement.png" alt="enforcement" caption="" %}}

### Overall 

The final index just sums up the scores across all five categories to get overall scores for each country.

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/overall.png" alt="overall" caption="" %}}

### Cross-Country Averages

Heatmaps are helpful to see what happens to individual countries over time. But averages across all countries are much better to compare trends. 

For instance, the average number of memberships and loss of rights requirements increases roughly at the same time.

{{% figure src="https://raw.githubusercontent.com/markushlang/patent_rights_index/main/averages.png" alt="averages" caption="" %}}

This is not an endorsement of this specific index, just a visualization. 

If you have ideas to measure patent protection differently, I would like to hear them.

---

### Code

Code (+data) is available here: [https://raw.githubusercontent.com/markushlang/patent_rights_index](https://raw.githubusercontent.com/markushlang/patent_rights_index)
