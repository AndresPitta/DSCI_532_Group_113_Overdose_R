## Proposal
### Section 1: Motivation and Purpose
According to recent article published by the journal of Drug and Alcohol Dependence<sup>[1]</sup>, Connecticut, U.S has suffered from a sever escalation in overdose deaths in the period between 2012 and 2018. This has prompted the attention of health professionals and public policy makers and research institutions to understand the roots of this issue.

To contribute to the effort towards the prevention of accidental death overdose in Connecticut, we are proposing a data visualization app that will assist the health professionals, public policy makers and research institutions to identify the people who are most vulnerable to die from accidental overdose.  The app will include user-interactive plots and graphs linking to different attributes of the people who lost their lives to the accidental overdose including their age, gender, and ethnicity and the number of drugs contributed to the death. Furthermore, it will offer users the options to explore the data from numerous perspectives including the distribution of number of deaths per month for years from 2012 to 2018. In addition, there will be a dynamic bar plot to show the ranking for drugs which claimed the highest number of deaths during these years. A plot showing the total stolen years due to the accidental death overdose is also included.
 
### Section 2:  Description of the data
**Accidental drug related deaths 2012-2018 data set (State of Connecticut)**

This data is provided by the local government of the state of Connecticut and was retrieved from [the State of Connecticut’s open data webpage](https://data.ct.gov/) through [US open data] (https://catalog.data.gov/dataset/accidental-drug-related-deaths-january-2012-sept-2015). 

The data was gathered from an investigation held by the Office of the Chief Medical Examiner and contains information extracted from scene investigations, death certificates and toxicity test performed to the victims.

**Content**

The dataset contains 5,105 reported accidental deaths caused by drug overdose in the state of Connecticut, from January 2012 to December 2018. From each observation, there is demographic information (such as `race`, `gender`, `age`, `place of residence`), information related to the scene investigation (`place of death`, `date of death`), and information about the results of the toxicity test for each of the drugs tested (`heroin`, `cocaine`, `fentanyl`, etc.). In addition, it contains the descriptions of the death as reported in the death certificate.

It is important to note that, for each drug examined during the toxicity test, there is a categorical variable that has Y if the drug tested positive, and NaN if not.

**Wrangling**

For the wrangling stage of the project, all the toxicity test results were casted into a binary variable in which 1 means that the drug tested positive in the toxicity test, and 0 if not. In addition, 25 observations were removed because the manner of death was reported as natural or it is still pending. NaNs from other variables were replaced with ‘No description’, in order to prevent from dropping valuable information.

### Section 3: Research questions and usage scenarios
#### The research question
What concerns us most is the people died from overdose. How should we describe them? Thus, we would like to raise the research questions as: 

**Who are the people who died the most from drug overdose?**  
**Which drug killed them the most?**

*The first question will be answered using information about age, gender and ethnicity*

#### Usage scenario

As a social worker, Marks wants to know which drugs are contributing to the overdose crisis and what kind of people are being affected the most by those drugs. This information can help Mark direct his effort into educating people regarding the most common drugs and the most common victims involved in accidental overdoses. Thus, the app was created to be used in the following way:

First when Mark logs on to the “Drug Overdose Observation App”, he will see a ranking chart with the most common drugs used in overdose cases. Then, he will see a heatmap showing the most common combinations of drugs present in overdose cases. This information is going to give a Mark a sense on which drugs are being related the most to overdose cases. Then, if Mark wanted to know more information about related to the drug (such as usage, production or chemical formula), he would be able to by selecting one drug in the drop down below. This action, will not only give him information about the chosen drug, but is going to show the age, gender and ethnicity distribution of the casualties that were related to that drug. 


*Reference[1]: GregRhee et al. (2019). Accidental drug overdose deaths in Connecticut, 2012–2018: The rise of polysubstance detection. Journal of Drug and Alcohol Dependence. Volume 205, 1 December 2019, 107671*
