---
layout: page
title: Dynamics of duplicated networks in polyploids
---

<div>
<p align="center">
  <a href="#challenges">challenges and pitfalls</a> |
  <a href="#seed">seed development</a> |
  <a href="#">fiber domestication</a>
  <br><br>
</p>
</div>

<a name="challenges"></a>
## Challenges and pitfalls in the use of partitioned gene counts for homoeologous gene expression and co-expression network analyses


As shown below in an allotetraploid genome, homoeologs refers to the duplicated gene pairs originated from its parental diploids. Only sequencing reads containing homoeolog distinguishing SNPs can be assigned to either homoeolog genes, while some reads like the two grey ones here remain indistinguishable. 
![](/research/pitfall1.png)

Ideally, based on the expression profiles of homoeolog we can build separate network for each sub-genome. But the reality is that a portion of RNA-seq reads per gene are not specific to either homoeolog, which are un-useable to network construction. What we can do is building networks based on only homoeolog-specific read counts. The resulted networks will show differences from the expected network, as indicated by arrows.
![](/research/pitfall2.png)

Therefore we want to ask how do such differences affect our downstream analysis. Applying the analysitic workflow below, we tested different methods at multiple stages as a possible source of technical variance, and also compared their performances. Eventually, we would like to define a reasonable practice for this kind of analysis and and avoid major artifacts.
![](/research/pitfall3.png)

<a name="seed"></a>
## Co-expression gene network of cottonseed development

To gain insight into phenotypic diversification in cotton seeds, we conducted co-expression network analysis of developing seeds from diploid and allopolyploid cotton species and explored network properties.

![](/research/seedNet.phenotype.jpg)

Two different conceptual approaches were explored to help understand network conservation and divergence at various evolutionary timescales and across ploidy levels..

**Approach One**: construct a multispecies coexpression network to provide a global view of coexpression network topology among species, followed by identifying key modules associated with devlopmental dynamics and phenotypic diversification  
![](/research/seedNet.multi1.jpg)
![](/research/seedNet.multi2.jpg)

**Approach Two**: construct individual coexpression networks for comparison to reveal topological changes in response to evolutionary events
![](/research/seedNet.indiv.jpg)  
![](/research/seedNet.oilNet.jpg)


----

## Homoeolog gene co-expression network implicates biased recruitment of regulatory architecture of seed development  
Instead of using the aggregated expression of homoeolog gene pairs, we now constructed allopolyploid co-expression networks based on homoeolog-specific expressions. This approach allows direct comparisons of sub-genome networks against their corresponding diploid parental networks. In addition to revealing topological modificantions of the "redundant" duplicated seed network following allopolyploidization, this work aims to explore the assymetric evolution of parental regulatory connections underlying phenotypic evolution and domestication.

Stay tuned!



