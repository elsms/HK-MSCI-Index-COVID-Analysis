[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-orange)](Project.ipynb)
[![Bloomberg Terminal](https://img.shields.io/badge/Bloomberg%20Terminal-Data%20Source-yellow)](https://www.bloomberg.com/professional/products/bloomberg-terminal/#overview)

# Introduction 
This notebook explores whether COVID-19 affected the Hong Kong MSCI Index returns. It was developed as part of the [Econometrics Analysis for Finance](https://www.reading.ac.uk/modules/documents?acyear=2025%252f6&modcode=ICM337&schoolcode=HBS%20DME%20G%7CHBS%20DME%20W%7CHBS%20FIN%20G%7CHBS%20FIN%20W%7CHBS%20IBS%20G%7CHBS%20IBS%20W%7CHBS%20LBR%20G%7CHBS%20LBR%20W%7CHBS%20MGM%20W%7CHBS%20REP%20G%7CHBS%20REP%20W&_ga=2.25857272.458363835.1771460903-1103066443.1771460903) module at [Henley Business School](https://www.henley.ac.uk/#).

The group assignment involved selecting one of two MSCI indexes (Hong Kong or South Korea) and addressing related research questions. This notebook presents my individual contribution, analyzing the impact of COVID-19 on the chosen index’s returns and comparing the findings with existing literature.

# Data 
The [data](Data) used in this analysis was sourced from the [Bloomberg Terminal](https://www.bloomberg.com/professional/products/bloomberg-terminal/), [LSEG](https://www.lseg.com/en) and a [website curated by the Hong Kong Government](https://data.gov.hk/en-data/dataset/hk-dh-chpsebcddr-novel-infectious-agent). 

# Methodology 

### Dataset Description 
The dataset used in the analysis entails the following variables. 
| Variable | Meaning |
|----------|--------------------|
| HK MSCI Returns | Monthly logarithmic HK MSCI returns over 2015-2023, used as the model’s dependent variable.  |
| Stringency Index | Government response tracker developed by the Blavatnik School of Government at the University of Oxford and sourced from London Stock Exchange Group (LSEG). It compiles policy responses to COVID-19 and is included because containment and economic measures (e.g., lockdowns, social distancing) have been shown to mitigate market impacts and support stock returns (Beer, Maniora, and Pott, 2023; Deng, Xu, and Lee, 2022; Guven et al., 2022; Jiang et al., 2022).  |
| Hang Seng Returns | Monthly logarithmic returns of the Hang Seng Index. Included because Hong Kong’s equity market was negatively affected by the outbreak, and prior research shows stock returns interact significantly with developing pandemics (Al-Awadhi, 2020; Jin, Lu, and Zhang, 2022). |
| Number of death cases related to COVID-19 | Daily deaths aggregated to monthly totals. Included as confirmed cases and deaths negatively impact stock returns and volatility (Ashraf, 2020; Guven et al., 2022; Harjoto et al., 2021). |
| Outbreak Severity | Sum of hospitalized cases in critical condition and the ratio of deaths to confirmed cases. Included due to evidence that higher severity negatively affects stock returns and volatility (Ashraf, 2020; Guven et al., 2022; Harjoto et al., 2021). |
| Spread | Ratio of confirmed cases to total monthly tests. Included as higher case rates negatively impact stock returns (Ashraf, 2020; Guven et al., 2022; Harjoto et al., 2021).  |
| Recovery | Sum of discharged cases and the ratio of ruled-out cases to confirmed cases. Included because recoveries have been shown to influence stock returns, though the effect is weaker than cases or deaths (Basuony, 2021).  |
| Time Dummy | Time dummy defined as follows: 1 = from January 1st, 2020, to December 31st, 2022, and 0 = from January 1st, 2015, to December 31st , 2019. Adopted to differentiate between pre-pandemic and pandemic periods, as in prior studies (Basuony et al., 2021; Khan, Fifield, and Power, 2024).  |
| MSCI COVID-19 | Interaction term specified as the product of MSCI Returns and the Time Dummy variable to capture potential changes in market sensitivity during the pandemic period, as stock markets exhibited intensified reactions during this period (Ashraf, 2020; Bai et al., 2023).  |

### Model Specification 

To test for a COVID-19 effect on the dependent variable, two models are specified:

* a **simple linear regression** with the *time dummy* variable as the only explanatory variable.
*  a **multiple linear regression** including all previously listed variables.





# Key Findings 


# Conclusion 
