---
published: true
title: journal club jan 2016
layout: post
tags: [ion_channels, rgc]
---
### The effect of morphology upon electrophysiological responses of retinal ganglion cells (RGCs): simulation results

--- 


## Links 
* [Paper](http://link.springer.com/article/10.1007/s10827-013-0463-7/fulltext.html)

## Objective

To explore the relationship between differences in morphology of RGCs and certain electrophysiological phenomena that have been described.

## Main outcome

**Model prediction:** difference between ON and OFF ganglion cells due to the presence of low voltage activated calcium currents in OFF cells and a lack of them in ON cells.

**Model scope:** The model seems to most accurately predict experimental outcomes for cells that have a large soma to total surface area.


## Background knowledge (notes)

1. Light enters the eye
1. Hits the photo-receptors
1. They connect to ON and OFF bipolar cells
1. ...retinal magic
1. ON and OFF pathways converge in the visual cortex as simple cells



RGCs differ in stratification layer and size... this is an image from cat RGCs:
![Morphologies](https://raw.githubusercontent.com/KikoBlog/KikoBlog.github.io/master/images/jc_2016_01/morphologies.jpg)

[src](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC2290089/)



## ...the model

### Multicompartment cell model 
<img style="width: 500px" src="https://raw.githubusercontent.com/KikoBlog/KikoBlog.github.io/master/images/jc_2016_01/morphology.gif"/>

SOBC: sodium band channel: more sodium channels (d'uh) 

### Membrane dynamics: Hodgekin-Huxley type model (eq 1):
Included parameters:
* Leak, sodium, calcium, delayed rectifier potassium, A-type, Ca-activated potassium current - everything neatly modelled like others before this paper.
* Calcium reversal potential varied with time
* Calcium concentration depends on the calcium current (d'uh) 

### Ion channel distribution:
Different ion channel concentrations are given in Table 4.

### This might be important - but maybe not:
* Leak conductance needed adjustment compared to a reference, because this study included additional inward currents that weren't modelled in the other paper. If not for this adjustment, the outcome wouldn't have matched the experimental  values. 

### The model was tuned:
* certain ion channel conductances (NaP, T, h) were evaluated using data of another publication

### The model was validated
...by comparing it to data.


## The interesting bit (results)

