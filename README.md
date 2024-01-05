# python-satisfaction

## Visualizing employee satisfaction comparisons in Python

### About
Analyzing a dataset with Python to provide insights to the Human Resources (HR) department of a large consulting firm. Relevant Python Packages: numpy, Pandas, Scipy, seaborn, Matplotlib, statsmodels, scikit-learn

### Overview
This project served as the basis for the capstone of my Google Advanced Data Analytics Certificate (01/2024)—which a cleaned up version of the Jupyter notebook file is included in this repository ([python_satisfaction.ipynb](https://github.com/i-am-nate/python-satisfaction/blob/main/python_satisfaction.ipynb)). It shows my work from beginning to end and my process of importing, data cleaning, transformation, formulization, and visualization using Python.

The accompanying .csv ([HR_capstone_dataset.csv](https://github.com/i-am-nate/python-satisfaction/blob/main/HR_capstone_dataset.csv)) is third-party data synthesized and provided by Google and the Coursera certificate course from which this capstone project originated, and it is used by permsission.

The goal of with this project is to analyze a dataset that can provide insights to the Human Resources (HR) department of a large consulting firm concerning high turnover. Ultimately, it was revealed that higher average monthly working hours, longer comparative and actual tenure, safer working environment, but relatively no upward mobility (meritocratic or otherwise), despite equivalent performance reviews — this all most likely contributes to the the high turnover.

### Business understanding
The problem the business was trying to solve — in this case, the fictitious Salifort Motors — was looking at why the turnover rate is so high and to shed some light on potential ways to raise satisfaction scores (and ultimately retain more employees). An initial metric was satisfaction level, of which the mean averaged 22 points lower for those who had left vs. those still remaining at the company; this is not a surprising finding.

Yet the most recent evaluation scores were around equivalent between the two groups, showing performance neither waned nor soared. In fact, in later analysis, I actually discovered some findings that shed light on how the leaving group may actually be better employees overall.

### Data understanding
The first step was to import relevant packages and the csv into a pandas dataframe. I then performed basic data cleaning by checking for empty cells (none) and duplicate values (3008 found and removed), renaming columns, and converting categorical features into numerical representations.

In exploring the data, we had exactly 10,000 observations of employees who stayed — 83.4% of the entire base. I started with inititally visualizing employee satisfaction score to other features, looking for a connection. But I quickly noticed the overall company promotion rate looked very low, and indeed was: only 1.69% of employees across the entire company had been promoted over a 5 year period.

![](https://github.com/i-am-nate/python-satisfaction/blob/main/images/1.jpg)

Upon further inspection, breaking it down by department, as low as 2 people in IT (0.2%) and 0% of all 686 product management department employees had seen promotion; the only outlier was 8.26% of the smallest department of 436 people: management.

![](https://github.com/i-am-nate/python-satisfaction/blob/main/images/2.jpg)

Worse yet, it appeared as if the employees who left actually had better overall performance as employees and weren't being recognized for it. Looking at low- to mid-income salary employees, those who left had average 6-9 months longer tenure at the company (almost 4 years) vs. those who remained. Further, those who left had averaged working an additional 9-10 monthly hours while maintaining a 2-4x safer work accident rate. Remember, this is despite equivalent employee evaluation scores as well.

![](https://github.com/i-am-nate/python-satisfaction/blob/main/images/3.jpg)

### Modeling
At the end, I included an OLS regression formula but ended up not needing to further model for my purposes. Relevent Python packages used in the project: numpy, Pandas, Scipy, seaborn, Matplotlib, statsmodels, scikit-learn.

### Conclusion
Overall, one of the biggest factors in retaining specifically low- to mid-level income employees comes down to recognition. With such low promotion rates, it might behoove the company as a next step to develop more rigorous review and reward mechanisms for promotion from within — or to evaluate root causes as to current low promotion rate.
