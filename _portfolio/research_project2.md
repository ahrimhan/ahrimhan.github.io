---
title: "Efficient refactoring candidate identification"
#excerpt: "short project description<br/><img src='/images/researchBDMeasure.png'>"
collection: portfolio
---

Period: March 2008 - December 2017

## Table of Contents
1. [Motivation and Goal](#mg)  
  1.1 [Overview of the refactoring identification process](#framework)  
2. [Method](#method)  
  2.1. [Dynamic profiling-based refactoring identification](#dynamic)  
  2.2. [Multiple and independent refactoring identification](#multiple)    
  2.3. [Two-phased search-based refactoring identification](#twophase)    
3. [Evaluation](#evaluation)  
  3.1 [Research questions](#RQ)  
  3.2 [Data sets](#datasets)  
4. [RQ1. Effectiveness of the dynamic information](#RQ1)  
5. [RQ2. Efficiency of multiple refactorings](#RQ2)  
6. [RQ3. Efficiency of the two-phased approach](#RQ3)  
7. [Conclusion](#conclusion)  
8. [Papers](#papers)  
9. [Tools](#tools)  
10. [Awards](#awards)  

## Motivation and Goal

Recent research was focused on defining the cost-effective software refactoring process by suggesting the refactoring candidates that can maximize improvement in software design quality (e.g., maintainability). As the software is getting larger and more complex, it is harder to find the refactoring candidates because of the lack of resources in computing power and time. Therefore, we need a method to efficiently identify refactoring candidates for the large-scale software.

In this project, I propose the several new methods to improve the efficiency of the refactoring identification process.


### Overview of the refactoring identification process <a name="framework"></a>  
![researchRefactoringOverview](/images/researchRefactoringOverview.png)  
To identify refactoring sequence automatically, refactoring candidates are extracted and assessed using a ``fitness function`` measuring maintainability. Then, the refactoring that most improves the maintainability in terms of the ``fitness function`` is selected and applied. We use the ``stepwise approach`` which selects the most beneficial refactoring for each iteration of the refactoring process. This process is iterated until there are no more improvements. In this study, the refactoring candidates indicate the possible moves of methods to classes in the system (i.e., ``Move Method``).

## Method

### Dynamic profiling-based refactoring identification [[IST'2013]](http://dx.doi.org/10.1016/j.infsof.2012.12.002) <a name="dynamic"></a>  
![researchRefactoringDynamic](/images/researchRefactoringDynamic.png)
To identify the candidates in classes where real changes have occurred, I provided the method to use the ``dynamic profiling technique`` for finding the ``most frequently used functions`` based on the several scenarios of user behavior. Then, refactoring candidates are extracted to ``reduce the dependencies among the entities used in the most frequently used functions``.


### Multiple and independent refactoring identification [[IST'2015]](http://dx.doi.org/10.1016/j.infsof.2014.10.007) <a name="multiple"></a>  
![researchRefactoringMultiple](/images/researchRefactoringMultiple.png)
To find a sequence of cost-effective refactorings, I proposed the method for selecting ``multiple refactorings that have no dependencies each other and can be applied simultaneously`` based on the concept of ``maximal independent set (MIS)``.


### Two-phased search-based refactoring identification [[TSE'2017]](https://dx.doi.org/10.1109/TSE.2017.2731853) <a name="twophase"></a>
![researchRefactoringTwophase](/images/researchRefactoringTwophase2.png)  
``To reduce the search space of candidates to be examined``, I suggested using the ``two-phase approach``. In the first phase, the refactoring candidates that are more likely to improve maintainability are chosen using the [``Delta Table``](/portfolio/research_project3/), lightweight and fast candidate assessment. In the second phase, only the chosen refactoring candidates are evaluated using a more complex and precise fitness function.


## Evaluation

### Research questions <a name="RQ"></a>

> **RQ1.** Is the dynamic information helpful in identifying refactorings that effectively improve maintainability?  
**RQ2.** Do the multiple refactorings reduce the computational cost required to achieve the same maintainability?  
**RQ3.** Is the two-phase assessment approach efficient?  
How well does the ``Delta Table`` correctly identify refactoring candidates that have actual higher maintainability metric values?



### Data sets

Open source projects written in Java

* **For RQ1 and RQ2**

|Name (Version)| [``jEdit (jEdit-4.3)``](https://sourceforge.net/projects/jedit/files/jedit/4.3)| [``Columba (Columba-1.4)``](https://sourceforge.net/projects/columba/files/Columba/1.4/)| [``JGit (JGit-1.1.0)``](https://projects.eclipse.org/projects/technology.jgit)|
|:------:|:------:|:------:|:------:|
|Type |Text editor| Email clients |Distributed source version control system|
|Total # of revisions | 19501 | 458 | 1616 |
|Report period | 2001-09 ~ 2011-09 | 2006-07 ~ 2011-07 | 2009-09 ~ 2011-09|
|Number of developers |25 |9 |9|
|Class #| 952| 1506 |689|
|Method # |6487 |8745| 5334|
|Attribute #| 3523 |3967 |2989|


* **For RQ3** (for larger and more recent version)

| Project | [``Apache Ant 1.9.6``](https://ant.apache.org/antnews.html) | [``JGit 4.1.0``](https://projects.eclipse.org/projects/technology.jgit) | [``JHotDraw 7.0.6``](https://sourceforge.net/projects/jhotdraw/files/JHotDraw/JHotDraw%207.0.x/) |
|:------:|:------:|:------:|:------:|
| Type | Java application build tool |Distributed source version control system |Java GUI framework |
| Lines of code | 222,256 | 166,415 | 135,233|
| Class # | 1,186 | 946 | 751 |
| Entity # (Method # + Field #) | 16,268 | 11,686 | 10,313 |
| Method #|  10,546 | 7,543 | 7,314|
| Field # | 5,722 | 4,143 | 2,999 |

## RQ1. Effectiveness of the dynamic information <a name="RQ1"></a>

### Experimental design
To assess the capability of refactorings for maintainability improvement, we use the ``change simulation`` method.
``We assume that as the software becomes more maintainable, the less propagated changes would be occurred.``
Therefore, we inject changes and count the propagated changes on the three different approaches, and ``compare the reduced number of propagated changes``.


|Comparators|
|:---|
| - Approach using dynamic information only (``Dynamic``) <br> - Approach using static information only (``Static``) <br> - Combination of the two approaches (``Dynamic + Static``) |


### Evaluation measure  
The efficiency of the identified refactorings can be evaluated by observing how fast the number of the propagated changes is reduced.

|Evaluation measure|
|:---|
| Rate of reduction for propagated changes (%)|

The rate of reduction for propagated changes (%) can be calculated as:   
{ Percentage of reduction for propagated changes(final) - Percentage of reduction for propagated changes(initial) } / # applied refactorings.


### Results
> The ``average rate of reduction for propagated changes`` of the ``approaches using dynamic information are higher`` than that of the approach using only static information.

* **Number of impacted methods and classes for accommodating changes in ``Columba``**
![researchRefactoringDynamicResult2](/images/researchRefactoringDynamicResult2.jpg)
For example in ``Columba``, the approaches using dynamic information reduce the number of propagated changes ``faster`` than the approach using only static information does.

* **``Percentage of reduction for propagated changes (%)``, ``Rate of reduction for propagated changes (%)``**
![researchRefactoringDynamicResult](/images/researchRefactoringDynamicResult.png)
In ``Columba``, the average rate of reduction for propagated changes are ``9.09% (Dynamic + Static)``, ``7.67% (Dynamic)``, and ``7.10% (Static)``. From the results in the table, we can observe that the ``average rate of reduction for propagated changes`` of the ``approaches using dynamic information are higher`` than that of the approach using only static information.

## RQ2. Efficiency of multiple refactorings <a name="RQ2"></a>

### Experimental design
We compare the approach of identifying ``multiple refactorings (our approach)`` with that of identifying a ``single refactoring`` at each iteration of the refactoring identification process.

|Comparators|
|:---|
| - Multiple refactorings (our approach) <br> - Single refactoring |

### Evaluation measures

|Required cost to reach the final solution of maintainability metric|
|:---|
|- Number of iterations <br> - Time |

Please note that, in our [paper](http://dx.doi.org/10.1016/j.infsof.2012.12.002), we defined the ``maintainability metric`` as  <sup>cohesion</sup>&frasl;<sub>coupling</sub> because ``this metric produces larger fitness values`` as the software gets more maintainable with ``higher cohesion`` and ``lower coupling``. In object-oriented software, high cohesion and low coupling have been accepted as important factors for good software design quality in terms of maintenance, because less propagation of changes to other parts of the system or side effects would occur. Cohesion corresponds to the degree to which elements of a class belong together, and coupling refers to the strength of association established by a connection from one class to another.
* ``Cohesion metric``: [``MSC (Message Similarity Cohesion)``](https://dl.acm.org/citation.cfm?id=1185469)
* ``Coupling metric``: [``MPC (Message Passing Coupling)``](https://dl.acm.org/citation.cfm?id=170622)


### Results
> Compared to the selection method involving single refactoring, our approach of ``multiple refactorings`` selects refactorings that improve the maintainability of the software design at ``lower computation costs`` with respect to ``smaller number of iterations`` or ``shorter elapsed time``.

* **``Number of iterations`` to reach the final solution**  
![researchRefactoringMultipleResult](/images/researchRefactoringMultipleResult.png)  
The table summarizes the results of the required costs in terms of the ``number of iterations`` to reach the final solution and the ``number of applied refactorings per iteration`` for ``jEdit``, ``Columba``, and ``JGit``, respectively. The total number of iterations required to reach to the final solution using our approach is much smaller than that required by the method of selecting a single refactoring: ``jEdit (26 < 1586)``, ``Columba (39 < 2290)``, and ``JGit (74 < 620)``.

* **``Time`` to reach the final solution**  
![researchRefactoringMultipleResult2](/images/researchRefactoringMultipleResult2.png)  
The graphs of required costs in terms of elapsed ``time`` to reach the final solution for ``jEdit``, ``Columba``, and ``JGit``, respectively. The ``x-axis`` shows the elapsed ``time``, and the ``y-axis`` shows the ``maintainability metric``.
For all projects, ``maintainability metric`` of our approach increases rapidly, while that of the single refactoring approach increases comparatively slowly.
Even though there is an overhead to compute ``maximal independent set (MIS)`` in the first step for the selection of multiple refactorings (denoted as ``Preprocessing Time`` in the graphs), ``our approach can attain the same degree of maintainability improvement at a much lower cost`` (i.e., ``time`` or the ``number of iterations``). Thus, the benefit outweighs this necessary overhead.


## RQ3. Efficiency of the two-phased approach <a name="RQ3"></a>

### Experimental design  

We compare our approach with the no-reduction approach. Our approach indicates the two-phase approach in that top 20% ranked using the Delta Table are evaluated using a fitness function (Delta top 20%). The approach to investigate all possible candidates is called the no-reduction approach.

|Comparators|
|:---|
| - Delta top 20% (our approach) <br> - No-reduction approach |

The used ``fitness functions`` are ``MPC (Message Passing Coupling)``, ``Connectivity``, and ``EPM (Entity Placement metric)``.
For improving maintainability, fitness functions should be increased or decreased: ``MPC (-)``, ``Connectivity (+)``, and ``EPM (-)``.

### Evaluation measures

* **Efficiency of the two-phased approach**  

|Efficiency measures|
|:---|
| - Total time <br> - Speed up|

Speed up x means that time of Delta top 20% (our approach) is x times as fast as time of no-reduction approach. Speed up can be calculated as: Speed up = Time for no-reduction / Time for Delta top 20%.

* **Performance of the ``Delta Table`` to find the candidates having higher fitness functions**

|Performance measures|
|:---|
|- Precision <br> - Recall |

```
 - Precision = |D ∩ E| / |D|   
 - Recall = |D ∩ E| / |E|
```
D: set of refactoring candidates in ``Delta Table``   
E: set of refactoring candidates with positive effects on each fitness function   


### Results
> - Our approach is efficient in that it saves a considerable amount of time while still achieving the same amount of fitness improvement as the no-reduction approach. Our approach is 2.6 (min) to 13.5 (max) times faster than the no-reduction approach.
- The Delta Table perfectly identified all refactoring candidates that improved MPC. For Connectivity and EPM, more than 74% of candidates that have positive effects on each fitness function can be identified by the Delta Table.

* **``Time`` and ``Speed up``**
![researchRefactoringTwophaseResult](/images/researchRefactoringTwophaseResult.png)

* **``Precision`` and ``Recall``**
![researchRefactoringTwophaseResult2](/images/researchRefactoringTwophaseResult2.png)


## Conclusion

To improve the efficiency of the refactoring identification process, I proposed the new methods: 1) using the dynamic information, 2) selecting multiple refactorings that can be applied simultaneously, and 3) using the two-phased approach to reduce the scope of candidates to be assessed using a fitness function. The efficient refactoring identification is important for computing the large-scale software.

## Papers

* [**Two-phase Assessment Approach to Improve the Efficiency of Refactoring Identification**](https://dx.doi.org/10.1109/TSE.2017.2731853)  
   **Ah-Rim Han**, Sungdeok Cha    
   IEEE Transactions on Software Engineering (TSE), Online Published at July 25, 2017        
   [[PDF]](/files/TSE2017proof.pdf) [[DOI]](https://dx.doi.org/10.1109/TSE.2017.2731853)

* [**An efficient approach to identify multiple and independent Move Method refactoring candidates**](http://dx.doi.org/10.1016/j.infsof.2014.10.007)  
  **Ah-Rim Han**, Doo-Hwan Bae, Sungdeok Cha  
  Information and Software Technology (IST), Vol. 59, pp. 53–66, Mar. 2015  
  [[PDF]](/files/ist2015MultipleRef.pdf) [[DOI]](http://dx.doi.org/10.1016/j.infsof.2014.10.007)  


* [**Dynamic profiling-based approach to identifying cost-effective refactorings**](http://dx.doi.org/10.1016/j.infsof.2012.12.002)  
  **Ah-Rim Han**, Doo-Hwan Bae  
  Information and Software Technology (IST), Vol. 55, No. 6, pp. 966-985, Jun. 2013  
  [[PDF]](/files/ist2013DynamicProfilingRef.pdf) [[DOI]](http://dx.doi.org/10.1016/j.infsof.2012.12.002)


## Tools

* [Delta search](https://github.com/ahrimhan/delta-search) (written in ``Python``)  
Prototype of the two-phased refactoring identification approach: search space reduction based on the ``Delta Table``

* [Mass refactoring](https://github.com/ahrimhan/mass-refactoring) (written in ``Python``)  
Implementation for choosing multiple refactoring candidates with the ``Delta Table``

* [Rank distance](https://github.com/ahrimhan/rank-distance) (written in ``Python``)  
Implementation for comparing the rank distance between static based and dynamic based refactoring approaches (for experiment purpose)

* [Java Code Quality Analysis   Tool](https://github.com/ahrimhan/artool-java) (written in ``Java``)
Java source code analysis and metric measurement tool


## Awards and Contribution

* Nov. 2014 - Apr. 2017, **sole Principal Investigator**, Individual Basic Science & Engineering Research Program   
[National Research Foundation of Korea (NRF)](http://www.nrf.re.kr/eng/main), $125,000
[[certificate]](/files/fund2Individual.pdf) [[translated version]](/files/fund2IndividualTranslate.pdf)

* [Suggestions of Refactoring Candidates to Active Open Source](https://github.com/ahrimhan/jgit/commit/29f61768bd8b66e5351142333b4d49ecc9adaae4)  
We applied the identified refactorings to the active open source project, ``JGit (version 4.7.1)``. We performed our approach of refactoring identification process automatically by choosing the refactorings that improve the maintainability of a fitness function to the greatest extent. Among the suggested refactorings, we selected to submit ``two of the refactorings`` found when using the fitness function of ``EPM``: **Move Method** ``clean`` from class ``WindowCache`` to class ``Entry`` and **Move Method** ``clean`` from class ``DfsBlockCache`` to class ``HashEntry``. The class ``Entry`` and the class ``HashEntry`` are the inner classes. The method ``clean`` tends to access the methods and attributes in each inner class (i.e., ``Feature Envy`` design problems); thus, it is better to move the methods to those inner classes where those methods are actually used.
