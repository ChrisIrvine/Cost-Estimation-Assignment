# SEP Research Notes

## Improving Cost Estimation

### A Systematic Review of Software Development Cost Estimation Studies
[Paper Here](https://bura.brunel.ac.uk/bitstream/2438/1076/3/04027147.pdf)

- 304 papers in 76 journals
- recommended changes to estimation research
	- increase breadth of the search from relevant studies
	- search manually for relevant papers in a carefully selected set of journals when it completeness is essential
	- conduct more studies on estimation methods used by the software industry
	- increase awareness of how properties of th edata set s impact th eresults when evaluating methods

Personal Conclusion: *This paper is good for directing my research, but otherwise useless to answering the question of improving cost estimation*

### Feature Subset Selection Can Imporve Software Cost Estimation Accuracy 
[paper here](http://blankslatetech.com/project1/trunk/promisedata.org/pdf/stlouis2005ChenMenziesPortBoehm.pdf)

- concludes that COCOMO can be improved with feature subsets
	- PRED(30) improved without increasing variance
- proposes that Feature Subset Selection (FSS) can improve the accuracy of COCOMO
	- "...FSS is an efficient heuristic search through subsets of the available attributes."
- what is COCOMO
	- Constructive Cost Model
	- used for estimating software cost, effort and schedule
	- open source
- used COCOMO I (more data available)
	- COCOMO-81 (63 projects)
	- COCOMO NASA (60 projects)
	- three largest subsets of COCOMO NASA
- Performance of COCOMO is PRED(30) which is calculated from the relative error (RE)

RE<sub>i</sub> = estimate<sub>i</sub> - actual<sub>i</sub> / actual<sub>i</sub>

From there we calculate the mean magnitude of the relative error (MMRE)

Magniture of Relative Error (MRE<sub>i</sub>) = *abs(RE<sub>i</sub>)*
MMRE<sub>i</sub> = *100/T E<sup>T</sup><sub>i</sub> MRE<sub>i</sub>*

(T = Data Size - |Training set size|)

PRED(N) is then calcualted using:

PRED(N) = 100/T E<sup>T</sup><sub>i</sub> { 1 if MRE<sub>i</sub> <= N/100 || 0 otherwise

PRED(30) = 50% means that half the estimates are within 30% of the actual cost. 

- Study uses WRAPPER FSS method implemented by open source Data Mining toolk kit WEKA
- Results from using WRAPPER FSS in conjunction with COCOMO
	- First cut means were always lower that means seen in other cut sets
	- 3rd cut onwards yielded best results.
	- overall the accuracy of COCOMO improved as seen by figure 1 vs figure 7

### Improving analogy-based software cost estimation by a resampling method
[paper here](https://www.sciencedirect.com/science/article/pii/S0950584907000328)

- iterative resampline (iterative bagging) to improve Estimation by Analogy (EbA)
- theory suggests iterative bagging improves various regression models
	- reduces prediction error
- implementing iterative bagging to real and artificial data resulted in significant improving
- iterative bagging
	- Machine Learning Technique
	- each data point in the collection to be sample has an equal chance of being selected to be bagged
- MMRE and MdMRE imporved significantly from iterave bagging during the analogy estimation method
- figure 1 for improvements