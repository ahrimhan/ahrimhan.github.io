---
title: "Breast cancer prediction"
#excerpt: "short project description<br/><img src='/images/researchBDMeasure.png'>"
collection: portfolio
---

# Breast cancer prediction

## Period  
May 2018


## Problem statement

It is difficult to forecast airline ticket prices because they fluctuate according to various conditions, and airlines do not disclose pricing policies. Therefore, even if you board the same plane, the amount of money you pay for a seat varies greatly.

A smart shopper would probably want to pay a small sum and buy an airplane ticket, but it is very difficult to decide when to buy an airplane ticket. Therefore, this report uses data mining techniques learned during class to find out the knowledge or patterns contained in these data based on the data on the factors affecting the air ticket price and helps to purchase airline ticket (Airline Ticket Purchase) .


<!--First, developing a flexible software would be much easier by modifying the design before implementing to source codes or by making a decision among several alternative design models. Second, development cost can be reduced, since the largest percentage of the software development effort is spent on maintenance.

Previous work efforts of change-proneness prediction have been made on source codes. Furthermore,
-->

## Data

The key concept for measuring the behavior dependency metric is to measure the dependency by weighting the control flows
(e.g., `choice` or `loops`)
into messages exchanged between the two classes.

<details><summary>
**Illustrative example for calculating all reachable paths for all pairs of objects in the system**
</summary>
![researchBDMOverview](/images/researchBDMOverview.png)
</details>  

<details><summary>
**Overview of the change-proneness prediction**
</summary>
![researchBDMProcedure](/images/researchBDMProcedure.jpeg)
</details>

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
    * Measured metrics  
     * [C&K metrics](https://ieeexplore.ieee.org/document/295895/)
     ```
       - NOC (number of children)
       - DIT (depth of inheritance tree)
       - WMC (weighted methods per class)
       - RFC (response for a class)
       - CBO (coupling between objects)
       - LCOM (lack of cohesion in methods)
     ```
     * Metric of change-proneness
     ```
     Total amount of changes (source lines of coded added and deleted) across the six releases (ver 1.0.1 ~ ver 1.0.6)
     ```


* **Method**
  * **Compare goodness of the fit (R<sup>2</sup> )** of the **multivariate regression models** constructed with and without the behavioral dependency metric along with the two different independent variable sets
    * **Dependent variables**: metric of change-proneness
    * **Independent variables**: behavioral dependency metric + C&K metrics  **vs.** C&K metrics  


## Results

> R<sup>2</sup> is increased by 8% using the behavioral dependency metric.

* **Regression model with only C&K metrics**:  
![researchBDMGraphCK](/images/researchBDMGraphCK.png)
  * Explains around 56% (adjusted R<sup>2</sup> of <ins>0.55</ins>)
  * Selected variables: WMC (1<sup>st</sup>), CBO (2<sup>nd</sup>), and LCOM (3<sup>rd</sup>)


* **Regression model with the behavioral dependency metric in addition to C&K metrics**:  
![researchBDMGraphBDM](/images/researchBDMGraphBDM.png)
  * Explains around 64% (adjusted R<sup>2</sup> of <ins>0.64</ins>)
  * Selected variables: WMC (1<sup>st</sup>), **BDM (behavioral dependency metric) (2<sup>nd</sup>)**, and CBO (3<sup>rd</sup>), LCOM (4<sup>th</sup>), and NOC (5<sup>th</sup>)


## Conclusion

The behavioral dependency metric in conjunction with existing structural metrics help to make a more accurate prediction change-proneness model.


## Papers

* [**Measuring behavioral dependency for improving change-proneness prediction in UML-based design models**](http://dx.doi.org/10.1016/j.jss.2009.09.038)  
**Ah-Rim Han**, Sang-Uk Jeon, Doo-Hwan Bae, Jang-Eui Hong  
Journal of Systems and Software (JSS), Vol. 83, No. 2, pp. 222-234, Feb. 2010  
[[PDF]](https://ahrimhan.github.io/files/jss2010BehavioralDependency.pdf)
[[DOI]](http://dx.doi.org/10.1016/j.jss.2009.09.038)

* [**Behavioral Dependency Measurement for Change-proneness Prediction in UML 2.0 Design Models**](http://dx.doi.org/10.1109/COMPSAC.2008.80)  
**Ah-Rim Han**, Sang-Uk Jeon, Doo-Hwan Bae, Jang-Eui Hong  
Proceedings of the 32nd Annual IEEE International Computer Software and Applications (COMPSAC), pp. 76-83, Jul. 2008  
(19.5% acceptance ratio, 46/236)   
[[PDF]](https://ahrimhan.github.io/files/compsac2008bdm.pdf)
[[DOI]](http://dx.doi.org/10.1109/COMPSAC.2008.80)
[[Slide]](https://ahrimhan.github.io/files/slideCompsac2008.pdf)

## Awards

The paper ``Behavioral Dependency Measurement for Change-proneness Prediction in UML 2.0 Design Models`` was invited for the publication to the Special Issue for Journal of Systems and Software. The top quality papers of the IEEE International Conference on Computer Software and Applications 2008 are selected by program committee.
