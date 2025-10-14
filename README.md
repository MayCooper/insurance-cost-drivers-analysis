# Insurance Cost Drivers Analysis  

**Exploratory and inferential analysis of a health insurance dataset using univariate, bivariate, and statistical testing to identify cost drivers, risk factors, and regional health trends.**

---

## Project Overview  
This project examines a health insurance dataset containing demographic, lifestyle, and medical cost information for 1,338 insured individuals.  
The goal is to analyze how factors such as **age**, **sex**, **BMI**, **smoking status**, and **region** affect healthcare costs.  
Using Python, the analysis combines **data validation**, **univariate**, **bivariate**, and **inferential** techniques to uncover significant relationships and support fair pricing and targeted health programs.

---

## Data Validation and Cleaning  
Before analysis, the dataset was validated to identify and correct anomalies. During inspection, non-numeric entries were found in the **BMI** column containing text such as explanatory statements rather than numeric data. These invalid rows were removed to ensure accurate statistical testing.  

After cleaning, the dataset contained consistent numeric and categorical fields with no missing or undefined values across the main analytical variables.  

This process ensured data integrity and reliability, providing a sound foundation for subsequent analysis.

---

## Univariate Analysis  
Univariate analysis was performed to understand the distribution of each variable.  

**Charges:**  

<img width="851" height="549" alt="image" src="https://github.com/user-attachments/assets/6e3aadcb-cb0a-476f-abf0-e5d0fcd7530d" />

Medical charges were heavily right-skewed, indicating that while most individuals incurred moderate expenses, a small group experienced exceptionally high medical costs. These outliers likely represent patients with chronic conditions or intensive care needs.  

**BMI:**  

<img width="851" height="549" alt="image" src="https://github.com/user-attachments/assets/b0a6c8bf-73ec-48ea-9cee-7a9dee5bcda1" />

BMI was approximately normally distributed with a mean near 30, reflecting that many individuals fall into overweight or obese categories. This finding is important because elevated BMI levels are commonly linked to higher health risks and medical expenditures.  

**Sex:**  

<img width="696" height="549" alt="image" src="https://github.com/user-attachments/assets/b6a022cd-438b-4234-9751-115a19af12c6" />

The dataset showed a nearly even gender distribution, with 662 males and 676 females, ensuring balanced representation for analysis.  

**Smoker:**  

<img width="705" height="549" alt="image" src="https://github.com/user-attachments/assets/aca860f1-94e3-4be5-90f0-339fc287a47a" />

A majority of individuals were non-smokers, while approximately 20% reported smoking. This smaller but distinct subgroup plays a significant role in explaining cost variability across the population.

---

## Bivariate Analysis  
Bivariate analysis explored interactions between variables to identify meaningful relationships.

**BMI and Charges:**  

<img width="869" height="549" alt="image" src="https://github.com/user-attachments/assets/66bc1850-633c-4748-a640-9f9a23684f1b" />

A scatterplot of BMI versus medical charges revealed a weak but statistically significant positive correlation (r = 0.20, p < 0.001).  
Individuals with higher BMI tend to have higher medical expenses, although BMI alone does not strongly predict cost.

**Smoking and Charges:**  

<img width="873" height="556" alt="image" src="https://github.com/user-attachments/assets/7ecc2ac8-cc4f-4a23-aacc-7aaaa3a78249" />

A boxplot comparison of smokers and non-smokers showed a clear difference in medical costs. Smokers had a broader range and higher median charges, often double those of non-smokers. This finding supports smoking as a primary cost driver in insurance modeling.  

**Regional Differences in BMI:**  

<img width="847" height="556" alt="image" src="https://github.com/user-attachments/assets/c4690bd9-f364-4e12-bd50-4e6d449bddf4" />

Boxplots across U.S. regions showed that BMI varies significantly by geography. The Southeast region exhibited the highest median BMI, while the Northwest had the lowest, aligning with the results of the Kruskal–Wallis test described below.

---

## Inferential Statistical Testing  

### Welch’s t-test (Smoker vs. Non-Smoker Charges)
**Research Question:**  
Is there a statistically significant difference in mean medical charges between smokers and non-smokers?

**Results:**  
- **t-statistic:** 32.75  
- **p-value:** < 0.001  
- **Decision:** Reject the null hypothesis.  

**Interpretation:**  
Smokers have significantly higher medical charges than non-smokers. This strong evidence supports cost-based policy differentiation and targeted health intervention programs.

---

### Kruskal–Wallis H-test (BMI Across Regions)
**Research Question:**  
Do median BMI values differ significantly across U.S. regions?

**Results:**  
- **Test Statistic:** 94.69  
- **p-value:** < 0.001  
- **Decision:** Reject the null hypothesis.  

**Interpretation:**  
BMI differs significantly by region, revealing geographic health disparities. The Southeast has the highest median BMI, while the Northwest shows healthier averages.

---

## Key Findings  
- **Medical charges are highly right-skewed**, driven by a small percentage of high-cost patients.  
- **Smokers incur significantly higher charges** than non-smokers, both statistically and practically.  
- **BMI varies significantly across regions**, with notable disparities between the Southeast and Northwest.  
- **BMI and charges are weakly but positively correlated**, with compounding effects when smoking is considered.  
- **Data validation identified and resolved inconsistencies** in BMI entries, ensuring accurate inferential results.

---

## Business Insights  
- Smoking behavior is a dominant cost driver, justifying differentiated premium strategies.  
- Regional BMI disparities highlight the need for geographically tailored wellness programs.  
- Combining demographic and lifestyle variables enables insurers to improve pricing fairness and cost predictability.  
- The analysis supports the development of data-driven wellness incentives and risk management initiatives.

---

## Tools and Techniques  
- **Python 3.x**  
- **Pandas** for data manipulation  
- **NumPy** for statistical computation  
- **Matplotlib** and **Seaborn** for visualization  
- **SciPy** for Welch’s t-test and Kruskal–Wallis testing  

---

## Results Summary  
- Smokers’ medical charges are statistically higher than those of non-smokers.  
- BMI differs significantly among regions, revealing health inequality patterns.  
- Statistical validation supports the accuracy and interpretability of findings.  
- The results inform pricing models, public health planning, and targeted insurance programs.  

---

## Future Improvements  
- Incorporate additional lifestyle, socioeconomic, and medical history data for deeper insights.  
- Apply regression and predictive modeling to estimate premiums more precisely.  
- Automate reporting dashboards in Tableau or Power BI for decision-maker accessibility.

---

© 2025 May Cooper. All rights reserved.
