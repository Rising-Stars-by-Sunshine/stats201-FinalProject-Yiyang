# Machine Learning for The Effect of Natural Disaster in 1960 on Life Expectancy in China
## Project information
- **Author**: Yiyang Zhang, Computation and Design with tracks in Digital Media, Class of 2025, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: Submissions to the Final Project for [STATS201 Introduction to Machine Learning for Social Science, 2022 Autumn Term (Seven Week - Second)](https://ms.pubpub.org/) instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: Acknowledgment: Thanks to Professor Luyao Zhang for guiding my project. Thanks for Xintong Wu's encouragement and Eddile Lin's peer review. And thanks to all Stats 201 students for their suggestions and comments.
- **Project Summary**: 
  - [Summarize the Background/Motivation]The 1960 famine in China was one of the largest natural disasters in human history, resulting in widespread hunger and mortality. The famine was caused by a combination of natural disasters, such as drought and floods, and poor agricultural policies (Ashton et al. 1984). Despite the significant impacts of the famine on the population, including a decline in life expectancy, it is unclear how the natural disaster affected life expectancy in the long term.
  - [Research Questions]How does the natural disaster of 1960 affect life expectancy in China?

![image](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/spotlight/figures/Chatgpt%20answer.png)

  - [Application Scenario (Data Source)]https://ourworldindata.org/life-expectancy
  - [Methodology] Linear regression analysis and causal inference.
  - [Results]According to the collected data, life expectancy in China, which had been rising steadily, did decline sharply in 1960 (Roser, Ortiz-Ospina, and Ritchie 2019). But after 1960, it showed a different change than predicted.
Contrary to expectations, life expectancy in China rose sharply after 1960 and almost kept rising at a similar rate. This sharp rise is due to the fact that people who had a significant negative impact on life expectancy in 1960 may have died and not been included in subsequent statistics when the data were compiled. This overturns previous assumptions and suggests that the 1960 natural disaster may have had a positive effect or have no significant effect on life expectancy in China. 
By comparing historical conditions, development process, environment and climate, and other factors, the health background of Hong Kong is similar to that of China (Yao and Wu 2008). But because Hong Kong is relatively isolated from mainland China, it is hardly affected by natural disasters and shows no anomalies in life expectancy statistics. After the 1960 natural disaster, the trend in life expectancy in China remained similar to that in Hong Kong, which was unaffected. This further illustrates the limited impact of the 1960 natural disaster on life expectancy in China.
  - [Intellectual Merits and Practical impacts of your project.] Although many people die of starvation during natural disasters, others who survive may have greater resilience. But there is also a suspicion that healthy people with higher life expectancy are more likely to survive famine.
Since data on health is collected on a yearly basis, the data sets are not large enough for machine learning and may lead to inaccurate final results. However, it has also inspired the creation of more frequent health data sets, which may be the direction of future research. Machine learning for health must be repeatable but machine learning in health is poor in reproducibility metrics, such as data sets and code accessibility, compared to other areas and has a long way to go (McDermott et al. 2021).
In addition, life expectancy may be influenced by other factors, such as changes in national health policies after the natural disaster and increased health awareness among people. The development of technology and medical technology may also be taken into account, and the analysis of these combined factors may be the direction of further research.

## Table of Contents
- [data](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/README.md#Data)
- [code](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/README.md#Code)
- [spotlight](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/README.md#Spotlight)
- [more about the author](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/README.md#More_about_the_Author)
- [references](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/README.md#References)
- [GitHub Page](https://rising-stars-by-sunshine.github.io/stats201-FinalProject-Yiyang/)


## Data
- Data Source: https://ourworldindata.org/life-expectancy
- Meta Data Infomation:

| Data Files | Data Type | Data Content |
| ----- | ----- | ----- | 
|  [life-expectancy.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/life-expectancy.csv)| Queried | life expectancy of all countries and regions | 
| [explanation.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/explanation.csv) | Queried | literatures for explanation| 
| [HL.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/HL.csv) | Processed | arranged life expectancy of all countries and regions | 
| [CHL.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/CHL.csv) | Processed | life expectancy of China | 
| [HHL.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/HHL.csv) | Processed | life expectancy of Hong Kong | 
| [Regression_Train.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/Regression_Train.csv) | Processed | Training data for regression | 
| [Regression_Test.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/Regression_Test.csv) | Processed | Testing data for regression | 

- Data Dictionary

| File Name | Variable Name | Description | Frecuency | Unit | Type |
| ----- | ----- | ----- | ----- | ----- | ----- |
|  [life-expectancy.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/life-expectancy.csv)| Entity | country and region | \ | \ | str | 
|  | Code | resource of data | \ | \ | str |
|  | Year | year of data collected | yearly | year | int |
|  | Life expectancy at birth (historical) | Life expectancy at birth each year | yearly | year | float |
| [explanation.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/explanation.csv) | Title | titles of collected literature | \ | \ | str | 
|  | Abstract | abstracts of collected literature | \ | \ | str |
| [HL.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/HL.csv) | Entity | country and region | \ | \ | str | 
|  | Code | resource of data | \ | \ | str |
|  | Year | year of data collected | yearly | year | int |
|  | Life expectancy at birth (historical) | Life expectancy at birth each year | yearly | year | float |
| [CHL.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/CHL.csv) | Year | year of data collected in China | yearly | year | int |
|  | Life expectancy at birth (historical) | Life expectancy at birth each year in China | yearly | year | float |
| [HHL.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/HHL.csv) | Year | year of data collected in Hong Kong | yearly | year | int |
|  | Life expectancy at birth (historical) | Life expectancy at birth each year in Hong Kong | yearly | year | float |
| [Regression_Train.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/Regression_Train.csv) | theta | yearly life expectancy | yearly | year | float |
|  | theta_past_ma10 | average life expectancy of past 10 years | yearly | year | float |
| [Regression_Test.csv](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/data/Regression_Test.csv) | theta | yearly life expectancy | yearly | year | float |
|  | theta_past_ma10 | average life expectancy of past 10 years | yearly | year | float |


## Code

Explaination Code Source: https://github.com/sunshineluyao/design-principle-blockchain

Prediction Code Source: https://github.com/Rising-Stars-by-Sunshine/stats201-tutorial-prediction

Causal Event Certification Code Source: https://numpy.org/doc/stable/reference/generated/numpy.polyfit.html

| Explaination | Prediction | Causal Inference |
| ----- | ----- | ----- | 
|  [explanation.ipynb](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/code/explanation.ipynb) |  [Process_Data_Prepare_X_and_Y_for_Classification_and_Regressions.ipynb](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/code/Process_Data_Prepare_X_and_Y_for_Classification_and_Regressions.ipynb)  | [Query_Data.ipynb](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/code/Query_Data.ipynb) |
|  | [Analyze_Data_Machine_Learning_for_Predicting_Market_Congestion_ipynb.ipynb](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/code/Analyze_Data_Machine_Learning_for_Predicting_Market_Congestion_ipynb.ipynb) | [Process_Data.ipynb](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/code/Process_Data.ipynb) |
|  |  | [Analyze_Data.ipynb](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/code/Analyze_Data.ipynb) | 

## Spotlight
- Poster
![image](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/spotlight/figures/poster.png)
- Explaination
![image](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/spotlight/figures/bigram.png)
![image](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/spotlight/figures/Life%20expectancy%20in%20China%20from%201930%20to%202020.png)
- Prediction
![image](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/spotlight/figures/Linear%20Regression.png)
- Causal Event
![image](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/spotlight/figures/Continuity%20Assumption.png)
- Result
![image](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/spotlight/figures/Casual%20Inference.png)

## More about the Author
- headshot
![image](https://github.com/Rising-Stars-by-Sunshine/stats201-FinalProject-Yiyang/blob/main/headshot.png)
- self-introduction
Yiyang Zhang,a DKU student from class of 2025, major in Computer and Design / Digital Media. Student Worker for DKU social media team. Research interest is digital design and media interaction. 
- Final reflections 
  - intellectual growth
  - professional growth
  - living a purposeful life

## References

### Data Source
- https://ourworldindata.org/life-expectancy
### Code Source
- https://github.com/Rising-Stars-by-Sunshine/stats201-portfolio
- https://github.com/sunshineluyao/design-principle-blockchain
- https://github.com/Rising-Stars-by-Sunshine/stats201-tutorial-prediction
### Articles
- https://ourworldindata.org/life-expectancy
- https://www.sciencedirect.com/science/article/pii/S0953620522002266
- https://link.springer.com/chapter/10.1007/978-1-4899-1231-2_9
- https://www.science.org/doi/abs/10.1126/scitranslmed.abb1655
- https://link.springer.com/article/10.1007/s11205-008-9326-4
### Literature
- Ashton, Basil, Kenneth Hill, Alan Piazza, and Robin Zeitz. 1984. “Famine in China, 1958-61.” Population and Development Review 10 (4): 613. https://doi.org/10.2307/1973284.
‌- McDermott, Matthew B. A., Shirly Wang, Nikki Marinsek, Rajesh Ranganath, Luca Foschini, and Marzyeh Ghassemi. 2021. “Reproducibility in Machine Learning for Health Research: Still a Ways to Go.” Science Translational Medicine 13 (586). https://doi.org/10.1126/scitranslmed.abb1655.
- Roser, Max, Esteban Ortiz-Ospina, and Hannah Ritchie. 2019. “Life Expectancy.” Our World in Data. October 2019. https://ourworldindata.org/life-expectancy.
‌- Yao, Grace, and Chia-huei Wu. 2008. “Similarities and Differences among the Taiwan, China, and Hong-Kong Versions of the WHOQOL Questionnaire.” Social Indicators Research 91 (1): 79–98. https://doi.org/10.1007/s11205-008-9326-4.
- You, Wenpeng, and Frank Donnelly. 2022. “Physician Care Access Plays a Significant Role in Extending Global and Regional Life Expectancy.” European Journal of Internal Medicine, June. https://doi.org/10.1016/j.ejim.2022.06.006.
- Zhang, Luyao (Sunshine). 2022. “Machine Learning for Causal Inference.” Machine Learning for Social Science, November. https://ms.pubpub.org/pub/causal-inference/release/8.
- Zhang, Luyao (Sunshine), Zesen Zhuang, and Xinyu (Michelle) Tian. 2022. “Machine Learning for Predictions.” Machine Learning for Social Science, November. https://ms.pubpub.org/pub/ml-prediction/release/4.
‌

