---
title: "Improvement of change-proneness prediction"
#excerpt: "short project description<br/><img src='/images/researchBDMeasure.png'>"
collection: portfolio
---

Period: March 2006 - February 2009

## Table of Contents
1. [Motivation and Goal](#mg)  
2. [Method](#method)   
3. [Experiment](#evaluation)  
  3.1 [Goal](#goal)  
  3.2 [Data sets](#datasets)  
  3.3 [Evaluation method](#evaluationmethod)  
4. [Results](#results)  
5. [Conclusion](#conclusion)  
6. [Papers](#papers)  
7. [Awards](#awards)  

## Motivation and Goal <a name="mg"></a>

Software changed either to add new functionalities or to fix bugs. Some part of the software may be more prone to be changed than others. Finding software parts that are more likely to change can be useful because we can decide how to effectively invest the software maintenance efforts. In previous studies, most of the metrics used to build a change-proneness predictive model are based on the structural complexity of software programs.

To improve the accuracy of the change-proneness prediction, I propose the new behavioral dependency metric that captures the aspects of the dynamic behavior program.

<!--First, developing a flexible software would be much easier by modifying the design before implementing to source codes or by making a decision among several alternative design models. Second, development cost can be reduced, since the largest percentage of the software development effort is spent on maintenance.

Previous work efforts of change-proneness prediction have been made on source codes. Furthermore,
-->

## Method <a name="method"></a>

**Overview of the change-proneness prediction**  
![researchBDMProcedure](/images/researchBDMProcedure.jpeg)


**Illustrative example for calculating all reachable paths for all pairs of objects in the system**  
![researchBDMOverview](/images/researchBDMOverview.png)  
The key concept for measuring the behavior dependency metric is to measure the dependency by weighting the control flows
(e.g., `choice` or `loops`) into messages exchanged between the two classes.



## Experiment <a name="experiment"></a>

### Goal <a name="goal"></a>
To show that the behavioral dependency metric is the useful and additional explanatory variable for change-proneness prediction


### Data sets <a name="datasets"></a>
[JFreeChart ver 1.0.0](https://sourceforge.net/projects/jfreechart/files/1.%20JFreeChart/1.0.0/): Open-source Java class library for generating various types of charts  

* Measured metrics: six [C&K metrics](https://ieeexplore.ieee.org/document/295895/)

|Independent variables|
|:---|
| - ``NOC (number of children)``<br> - ``DIT (depth of inheritance tree)`` <br> - ``WMC (weighted methods per class)`` <br> - ``RFC (response for a class)`` <br> - ``CBO (coupling between objects)`` <br> - ``LCOM (lack of cohesion in methods)``|

* Metric of change-proneness

|Dependent variables|
|:---|
|Total amount of changes (source lines of coded added and deleted) across the six releases (ver 1.0.1 ~ ver 1.0.6)|

### Evaluation method <a name="evaluationmethod"></a>
**Compare goodness of the fit (R<sup>2</sup>)** of the **multivariate regression models** constructed with and without the behavioral dependency metric along with the two different independent variable sets  

|Comparators| Description |
|:---|:---|
| Model with behavioral dependency metric in addition to C&K metrics (our approach) | - Dependent variables: metric of change-proneness <br> - Independent variables: ``behavioral dependency metric`` + ``C&K metrics`` |
| Model with only C&K metrics | - Dependent variables: metric of change-proneness <br> - Independent variables: ``C&K metrics`` |

| Evaluation measure |
|:---|
| Goodness of the fit (R^2)|


## Results <a name="results"></a>

> R<sup>2</sup> is increased by 8% using the behavioral dependency metric.

* **``Regression model with only C&K metrics``**:  
![researchBDMGraphCK](/images/researchBDMGraphCK.png)
  * Explains around 56% (adjusted R<sup>2</sup> of <ins>0.55</ins>)
  * Selected variables: WMC (1<sup>st</sup>), CBO (2<sup>nd</sup>), and LCOM (3<sup>rd</sup>) <br>


* **``Regression model with the behavioral dependency metric in addition to C&K metrics``**:  
![researchBDMGraphBDM](/images/researchBDMGraphBDM.png)
  * Explains around 64% (adjusted R<sup>2</sup> of <ins>0.64</ins>)
  * Selected variables: WMC (1<sup>st</sup>), **BDM (behavioral dependency metric) (2<sup>nd</sup>)**, and CBO (3<sup>rd</sup>), LCOM (4<sup>th</sup>), and NOC (5<sup>th</sup>)


## Conclusion <a name="conclusion"></a>

The behavioral dependency metric in conjunction with existing structural metrics help to make a more accurate prediction change-proneness model.


## Papers <a name="papers"></a>

* [**Measuring behavioral dependency for improving change-proneness prediction in UML-based design models**](http://dx.doi.org/10.1016/j.jss.2009.09.038)  
**Ah-Rim Han**, Sang-Uk Jeon, Doo-Hwan Bae, Jang-Eui Hong  
Journal of Systems and Software (JSS), Vol. 83, No. 2, pp. 222-234, Feb. 2010  
[[PDF]](/files/jss2010BehavioralDependency.pdf) [[DOI]](http://dx.doi.org/10.1016/j.jss.2009.09.038)

* [**Behavioral Dependency Measurement for Change-proneness Prediction in UML 2.0 Design Models**](http://dx.doi.org/10.1109/COMPSAC.2008.80)  
**Ah-Rim Han**, Sang-Uk Jeon, Doo-Hwan Bae, Jang-Eui Hong  
Proceedings of the 32nd Annual IEEE International Computer Software and Applications (COMPSAC), pp. 76-83, Jul. 2008  
(19.5% acceptance ratio, 46/236)   
[[PDF]](/files/compsac2008bdm.pdf) [[DOI]](http://dx.doi.org/10.1109/COMPSAC.2008.80) [[Slide]](/files/slideCompsac2008.pdf)

## Awards <a name="awards"></a>

The paper ``Behavioral Dependency Measurement for Change-proneness Prediction in UML 2.0 Design Models`` was invited for the publication to the Special Issue for Journal of Systems and Software. The top quality papers of the IEEE International Conference on Computer Software and Applications 2008 are selected by program committee.
