# International Trade and Child Labour

An econometric analysis examining the cross-country relationship between international trade openness and child labour rates.

## Overview

This repository contains a comprehensive econometric study that investigates whether international trade has a significant impact on child labour rates across countries. The analysis uses cross-sectional data from 88 countries to test the relationship between trade openness, national income, and child labour participation.

**Authors:**
- Chandrasekhar N (HS12H014)
- Hitesh Khandelwal (MM13B017)
- Nantakumar (MM13B026)
- Pruthvi (NA12B016)
- Sandeep Shaw (EE11B073)
- Varun Ananth Murthy (HS12H045)

## Key Findings

The econometric analysis reveals that:

- **Trade openness alone has limited explanatory power** for child labour rates (R² = 0.0608)
- **Per capita income is a much stronger predictor** of child labour rates than trade openness
- **Higher income levels significantly reduce child labour** - every percentage increase in per capita income decreases child labour by approximately 6.21%
- **The role of increasing per capita incomes in reducing child labour overshadows the effect of international trade**
- Trade openness shows a negative but statistically insignificant relationship with child labour

## Repository Contents

### 📊 Data Files

- **`Dataset.xlsx`** - Primary dataset containing cross-country data for 88 nations including:
  - Child labour rates (source: ILO Data Library)
  - Export and import values (source: World Bank)
  - GDP and GDP per capita (source: World Bank)

- **`Metrics project.dta`** - Stata format data file for statistical analysis

### 📄 Documentation

- **`ChildLabour_Trade_Report.pdf`** - Complete research report (9 pages) containing:
  - Introduction and literature review
  - Research questions and hypotheses
  - Detailed methodology
  - Statistical analysis and regression results
  - Tests for heteroskedasticity and multicollinearity
  - Conclusions and policy implications
  - References

- **`Metrics Presentation Child Labour Final.pdf`** - Presentation slides summarizing the key findings and methodology

**Note:** For those interested in a detailed understanding of the methodology, statistical tests, and theoretical framework, please refer to the full report (`ChildLabour_Trade_Report.pdf`) and presentation (`Metrics Presentation Child Labour Final.pdf`) included in this repository.

## Methodology

### Research Questions

The study tests three regression models:

**Model 1: Basic Relationship**
```
child_i = α + β₁(openness_i) + μ_i
```
- Tests the direct relationship between trade openness and child labour

**Model 2: Including Income**
```
child_i = α + β₁(openness_i) + β₂(login_i) + μ_i
```
- Adds log of GDP per capita as an explanatory variable
- Significantly improves model fit (R² = 0.2677)

**Model 3: Non-linear Income Effects**
```
child_i = α + β₁(openness_i) + β₂(login_i) + β₃(squarelogin_i) + μ_i
```
- Tests for non-linear relationship between income and child labour
- Based on methodology from Edmonds & Pavcnik (2006)

### Variables Defined

- **`child`**: Percentage of children (ages 5-14) engaged in child labour
- **`openness`**: Trade openness = (Exports + Imports) / GDP
- **`login`**: Log of GDP per capita (used as proxy for national income)
- **`squarelogin`**: Squared term of login (for testing non-linear effects)

### Statistical Analysis

The study employs:
- **Ordinary Least Squares (OLS) regression**
- **t-tests** for individual coefficient significance
- **F-tests** for overall model significance
- **White's test** for heteroskedasticity
- **Variance Inflation Factor (VIF)** for multicollinearity
- **Robust standard errors** to account for heteroskedasticity

## Background Context

### What is Child Labour?

Child labour refers to the employment of children in work that:
- Deprives children of their childhood
- Interferes with ability to attend regular school
- Is mentally, physically, socially, or morally dangerous and harmful

### Global Statistics

- **60%** of child labour occurs in agricultural activities (farming, dairy, fisheries, forestry)
- **25%** in service activities (retail, restaurants, domestic help, etc.)
- **15%** in assembly and manufacturing
- **70%** occurs in rural areas, **26%** in informal urban sectors
- **22%** of workforce in Asia, **32%** in Africa, **17%** in Latin America

According to the International Labour Organisation (ILO), **poverty is the greatest single cause** behind child labour, compounded by lack of affordable education and quality schools.

## How to Use This Repository

### For Researchers and Students

1. **Start with the report**: Read `ChildLabour_Trade_Report.pdf` for comprehensive understanding of the methodology and findings

2. **Review the presentation**: Check `Metrics Presentation Child Labour Final.pdf` for a visual summary

3. **Analyze the data**:
   - Open `Dataset.xlsx` to explore the raw data
   - Use `Metrics project.dta` if working with Stata

4. **Reproduce the analysis**:
   - Variables are clearly defined in the report
   - Regression specifications are provided for all three models
   - Statistical tests are documented with results

### For Policy Makers

This research is relevant for:
- Understanding the limited role of trade sanctions in combating child labour
- Recognizing the importance of income growth and poverty reduction
- Designing policies that focus on economic development rather than trade restrictions

### For Economists

The study provides:
- Cross-country empirical evidence on trade-child labour relationship
- Comparison with existing literature (Edmonds & Pavcnik, 2006)
- Robust statistical testing for model validity
- Discussion of omitted variable bias and model limitations

## Data Sources

- **Child Labour Data**: ILO (International Labour Organisation) Data Library
- **Trade Data**: World Bank - Exports and Imports
- **Economic Data**: World Bank - GDP and GDP per capita
- **Sample**: 88 countries (after accounting for data inconsistencies)

## Key References

- Edmonds, E.V. & Pavcnik, N. (2006). International trade and child labor: Cross-country evidence. *Journal of International Economics* 68, 115-140.
- Basu, K. & Van, P.H. (1998). The economics of child labor. *American Economic Review* 88, 412-427.
- Frankel, J.A. & Romer, D. (1999). Does trade cause growth? *American Economic Review* 89, 279-399.

For the complete list of references, see the report.

## Statistical Software

The analysis was conducted using **Stata**, as evidenced by the `.dta` data file and regression outputs in the report.

## Limitations

As noted in the report:
- The model may suffer from omitted variable bias (e.g., income inequality, education access, cultural factors)
- Cross-sectional data cannot establish causation, only correlation
- Heteroskedasticity was detected in Model 2 (addressed using robust standard errors)
- Trade openness may affect child labour through indirect channels not captured in the models

## Policy Implications

The findings suggest that:

1. **Trade sanctions are unlikely to be effective** tools for reducing child labour
2. **Economic development and income growth** should be the primary focus of anti-child labour policies
3. **Poverty alleviation** is more important than trade restrictions
4. International efforts should focus on improving **access to quality education** and raising household incomes

## License

This is an academic research project. Please cite appropriately if using this data or methodology.

## Questions or Feedback?

For questions about the methodology, data, or findings, please refer to the detailed report (`ChildLabour_Trade_Report.pdf`) which contains comprehensive explanations of all analytical procedures and results.

---

*This econometric study challenges conventional assumptions about trade's role in child labour and provides evidence-based insights for policy development.*
