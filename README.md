# Family Size Modeling in Portugal

Analyzed data from Portugal's 1979 fertility survey to examine how literacy and age at marriage relate to family size. Used Poisson and negative binomial regression in R to estimate associations while accounting for current age, region, and marriage duration.

## Approach

- **Data preparation:** Imported fixed-width survey data and recoded literacy, marriage-age groups, and region. Visualized the distribution of children and compared family sizes across literacy and marriage-age groups.
- **Count modeling:** Fitted a Poisson regression with a log link and a log-years-married offset to model the number of children relative to marriage duration. Used ages 22–25 and rural areas with fewer than 10,000 residents as reference groups.
- **Model comparison:** Fitted a negative binomial model with the same predictors to allow for extra-Poisson variation, and compared coefficient estimates and confidence intervals across the two specifications.
- **Statistical interpretation:** Used rate ratios, 95% confidence intervals, and significance tests to summarize associations between demographic characteristics and the modeled rate of children per year of marriage.

## Results

In the reported Poisson model, women without literacy had a **42.4% higher modeled rate** than literate women, holding the included predictors constant (**rate ratio: 1.424; 95% CI: 1.356–1.496**). Marriage at ages 25–30 and 30+ was associated with rates approximately **10.8% and 20.1% higher**, respectively, than marriage at ages 22–25.

Poisson and negative binomial models produced similar coefficient estimates, with the negative binomial model allowing for additional variation. These are adjusted associations in historical survey data, not causal effects.

**Tools:** R, ggplot2, dplyr, glmmTMB, jtools, gridExtra, knitr, and kableExtra.

