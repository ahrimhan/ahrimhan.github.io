---
title: "Refactoring Candidate Identification"
#excerpt: "short project description<br/><img src='/images/researchBDMeasure.png'>"
collection: portfolio
---

# Refactoring Candidate Identification

Period: March 2008 - December 2017

## Table of Contents
1. [Motivation and Goal](#mg)
2. [Method](#method)  
  2.1. [Overview of refactoring identification process](#overview)
  2.2. [Software design is captured into a graph](#step1)  
  2.3. [Delta Table calculation](#step2)  
3. [Evaluation](#evaluation)  
  3.1 [Research questions](#RQ)
  3.2 [Data sets](#datasets)  
  3.3 [Evaluation method](#evaluationmethod)
4. [Results](#results)  
  4.1 [Efficiency](#RQ1)
  4.2 [Usefulness](#RQ2)  
5. [Conclusion](#conclusion)  
6. [Papers](#papers)  
7. [Tools](#tools)  
8. [Awards](#awards)  

## Motivation and Goal
scipy numpy
search Based


prediction model constructed based on the structural dependencies, change history, and textual information.

- search-based

This competition is evaluated on the weighted categorization accuracy of your predictions (the percentage of camera models correctly predicted).

weighted_accuracy(y,ŷ )=1n∑i=1nwi(yi=ŷ i)∑wi
where n is the number of samples in the test set, y is the true camera label, y_hat is the predicted camera label, and w_i is 0.7 for unaltered images, and 0.3 for altered images.

evaluation metric : precision / recall

# Method

### Overview of the refactoring identification process <a name="overview"></a>
![researchDeltaOverview](/images/researchRefactoringOverview.png)
To identify refactoring sequence automatically, refactoring candidates are extracted and assessed using a ``fitness function`` measuring maintainability. Then, the refactoring that most improves the maintainability in terms of the ``fitness function`` is selected and applied. We use the ``stepwise approach`` which selects the most beneficial refactoring for each iteration of the refactoring process. This process is iterated until there are no more improvements. In this study, the refactoring candidates indicate the possible moves of methods to classes in the system (i.e., ``Move Method``).



# Evaluation


```
Maintainability metric
```

In [previous paper](http://dx.doi.org/10.1016/j.infsof.2012.12.002), we used the ``maintainability metric`` as  <sup>cohesion</sup>&frasl;<sub>coupling</sub> because ``this metric produces larger fitness values`` as the software gets more maintainable with ``higher cohesion`` and ``lower coupling``. In object-oriented software, high cohesion and low coupling have been accepted as important factors for good software design quality in terms of maintenance, because less propagation of changes to other parts of the system or side effects would occur. Cohesion corresponds to the degree to which elements of a class belong together, and coupling refers to the strength of association established by a connection from one class to another.
* ``Cohesion metric``: [``MSC (Message Similarity Cohesion)``](https://dl.acm.org/citation.cfm?id=1185469)
* ``Coupling metric``: [``MPC (Message Passing Coupling)``](https://dl.acm.org/citation.cfm?id=170622)






This competition is evaluated on the weighted categorization accuracy of your predictions (the percentage of camera models correctly predicted).

weighted_accuracy(y,ŷ )=1n∑i=1nwi(yi=ŷ i)∑wi
where n is the number of samples in the test set, y is the true camera label, y_hat is the predicted camera label, and w_i is 0.7 for unaltered images, and 0.3 for altered images.

evaluation metric : precision / recall


## Period  
March 2006 - February 2009


## Motivation

Software changed either to add new functionalities or to fix bugs. Some part of the software may be more prone to be changed than others. Finding software parts that are more likely to change can be useful because we can decide how to effectively invest the software maintenance efforts.

In previous studies, most of the metrics used to build a change-proneness predictive model are based on the structural complexity of software programs.

<!--First, developing a flexible software would be much easier by modifying the design before implementing to source codes or by making a decision among several alternative design models. Second, development cost can be reduced, since the largest percentage of the software development effort is spent on maintenance.

Previous work efforts of change-proneness prediction have been made on source codes. Furthermore,
-->

## Objective and Method

To improve the accuracy of the change-proneness prediction, I proposed the new behavioral dependency metric that captures the aspects of the dynamic behavior program.

The key concept for measuring the behavior dependency metric is to measure the dependency by weighting the control flows
(e.g., `choice` or `loops`)
into messages exchanged between the two classes.

The illustrative example for calculating all reachable paths for all pairs of objects in the system:  
![researchBDMeasure](/images/researchBDMOverview.png)

<!---
## Data preparation

## Prediction model

## Key result

## Accomplishment
-->


## Experiment

* **Goal**
  * To show that the behavioral dependency metric is the useful and additional explanatory variable for change-proneness prediction


* **Data sets**
  * [JFreeChart ver 1.0.0](https://sourceforge.net/projects/jfreechart/files/1.%20JFreeChart/1.0.0/)
    * Open-source Java class library for generating various types of charts


* **Method**
  * **Compare goodness of the fit** of the **multivariate regression models** with the two different independent variable sets
    * **Dependent variables (metric of change-proneness)**: **Total amount of changes** (source lines of coded added and deleted) across the six releases (ver 1.0.1 ~ ver 1.0.6)
    * **Independent variables**: [C&K metrics](https://ieeexplore.ieee.org/document/295895/) (NOC, DIT, WMC, RFC, CBO, LCOM) **vs.** **behavioral dependency metric** + C&K metrics


## Results

> R<sup>2</sup> is increased by 8% using the behavioral dependency metric.

* **Regression model with only C&K metrics**:  
![graphCK](/images/researchBDMGraphCK.png)
  * Explains around 56% (adjusted R<sup>2</sup> of <ins>0.55</ins>)
  * Selected variables: WMC (1<sup>st</sup>), CBO (2<sup>nd</sup>), and LCOM (3<sup>rd</sup>)


* **Regression model with the behavioral dependency metric in addition to C&K metrics**:  
![graphCK](/images/researchBDMGraphBDM.png)
  * Explains around 64% (adjusted R<sup>2</sup> of <ins>0.64</ins>)
  * Selected variables: WMC (1<sup>st</sup>), **BDM (behavioral dependency metric) (2<sup>nd</sup>)**, and CBO (3<sup>rd</sup>), LCOM (4<sup>th</sup>), and NOC (5<sup>th</sup>)


## Conclusion

The behavioral dependency metric in conjunction with existing structural metrics help to make a more accurate prediction change-proneness model.


## Papers



## Tools


## Awards

* Nov. 2014 - Apr. 2017, **sole Principal Investigator**, Individual Basic Science & Engineering Research Program   
[National Research Foundation of Korea (NRF)](http://www.nrf.re.kr/eng/main), $125,000
[[certificate]](https://ahrimhan.github.io/files/fund2Individual.pdf) [[translated version]](https://ahrimhan.github.io/files/fund2IndividualTranslate.pdf)
