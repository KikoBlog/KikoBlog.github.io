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


## (notes)

1. Light enters the eye
1. Hits the photo-receptors
1. They connect to ON and OFF bipolar cells
1. ...retinal magic
1. ON and OFF pathways converge in the visual cortex as simple cells

ON increases firing frequency with increasing light intensity
OFF S-cell: sustained, spontaneous spiking in darkness, a sustained component of spiking activity during illumination
OFF T-cell: transient, quiet in darkness, transient spikes at light offset

...what is alpha-like behaviour?

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

1. For certain cells, this model reproduced experimental data, for others it didn't (see Table 5). The authors investigated the morphologies of the cells that did and didn't work with the model. 
1. The authors also explored the effect of soma and dendrite surface area on the intrinsic electrophysiological properties of the cells.

### Regarding 1:
* 88 of 200 cells did not meet the constraints. (some did not produce action potential, others spiked during hyperpolarizing stimulus...)
<img style="width: 500px" src="https://raw.githubusercontent.com/KikoBlog/KikoBlog.github.io/master/images/jc_2016_01/histogram.gif"/>
Cells not meeting the constraints had a high ratio of dendritic to total surface area, a larger soma, and a lower input resistance.

### Regarding 2:
* Dendritic and somatic compartment size were (independently) reduced step by step - resting potential, spontaneous and rebound burst frequencies were calculated, rest was simulated.
<img style="width: 500px" src="https://raw.githubusercontent.com/KikoBlog/KikoBlog.github.io/master/images/jc_2016_01/phaseplot.gif"/>
Off S (sustained) cell
Arrows point in the direction of decreasing size.
*a* dendritic surface reduction: The action potentials increased in maximal amplitude, and changed faster(?) - does that mean higher firing rate?
*d* somatic surface reduction: The action potentials decreased in maximal amplitude and changed more slowly.