# The Relationship between Macronutrients, Energy Density and Satiety

## Overview
Obesity remains a major global health issue, with approximately 890 million people affected worldwide (World Health Organization, 2024). Understanding which foods promote satiety may support improved dietary design and weight management strategies.

Previous research suggests a hierarchy of satiation: Protein > Carbohydrate > Fat, and highlights the importance of low energy density foods in promoting satiety.
However, less is known about perceived satiety (PS)—consumer expectations of fullness prior to consumption.

This study examines how macronutrient composition and energy density influence perceived satiety ratings.

## Study Design
312 foods representative of the UK diet were selected
Sampling used a ternary plot design
2,010 participants completed an online survey
Participants rated:
General satiety,
Portion satiety,
Food liking,
Hedonic overconsumption.
Ratings were measured using a 100-point Visual Analogue Scale (VAS).

## Dataset
### Variables used:
PS_mixmeans – General satiety

Por_mixmeans – Portion satiety

ProteinG – Protein content

CarbG – Carbohydrate content

FatG – Fat content

KCAL_100g – Energy density

## Packages Used
haven

psych

car

lmtest

sandwich

ggplot2

segmented

## Statistical Analyses
### Macronutrients
#### Correlation Analysis
Protein showed a weak positive correlation with satiety, while carbohydrate and fat showed moderate negative correlations. Overall, carbohydrate and fat demonstrated stronger inverse relationships with satiety than protein.

#### Simple Linear Regression
Protein was a weak positive predictor of satiety (R² = .016)
Carbohydrate was a moderate negative predictor (R² = .142)
Fat was a negative predictor (R² = .099)
Overall, carbohydrate showed the strongest predictive relationship, followed by fat, while protein showed a weak positive association.

#### Multiple Regression

Assumption checks included:

Multicollinearity (VIF)

Residual normality

Independence of errors (Durbin–Watson)

Heteroskedasticity (Breusch–Pagan test)

The overall model was significant:
F(3, 308) = 27.53, p < .001
R² = .211 (Adjusted R² = .204).
Carbohydrate and fat were significant negative predictors, while protein was not significant when controlling for other macronutrients.

### Energy Density
Energy density was significantly negatively associated with satiety:
r = −0.397, p < .001
R² = .157
A LOESS smoother suggested potential non-linearity in the relationship. A segmented regression identified a potential breakpoint at approximately 120 kcal/100g.

## Key Findings
Protein showed a weak positive relationship with satiety.
Carbohydrates and fat had a negative relationship with satiety.
Protein effects are not statistically significant in multivariate models.
Energy density showed a clear negative relationship with satiety.
Evidence suggests possible non-linear relationship with a breakpoint of ~120 kcal/100g.

## Reproducibility
This project is structured for reproducibility using relative file paths and a standard analysis workflow. All scripts can be run from the project root directory.

## Author
Molly Blakemore
