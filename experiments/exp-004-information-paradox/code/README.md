# Information Saturation Paradox Test - Code Repository

## Overview
This directory contains all code used for the Information Saturation Paradox experiment, including data collection tools, analysis scripts, and visualization code.

## Directory Structure
```
code/
├── README.md                    # This file
├── data_collection/            # Data collection and experiment management
│   ├── randomization.py        # Participant randomization script
│   ├── information_packages.py # Information package generation
│   └── survey_tools.py         # Survey deployment and management
├── analysis/                   # Statistical analysis and modeling
│   ├── primary_analysis.R      # Main factorial ANOVA analysis
│   ├── mediation_analysis.R    # Cognitive load mediation models
│   └── longitudinal_models.R   # Mixed-effects longitudinal analysis
├── visualization/              # Plots and figures generation
│   ├── descriptive_plots.py    # Descriptive statistics visualization
│   ├── effect_plots.R          # Treatment effect visualization
│   └── publication_figures.R   # Publication-ready figures
└── utilities/                  # Helper functions and tools
    ├── data_cleaning.py        # Data preprocessing and cleaning
    ├── effect_size_calc.R      # Effect size calculations
    └── sample_size_power.R     # Power analysis and sample size calculations
```

## Key Scripts

### Data Collection (`data_collection/`)

**`randomization.py`**: Stratified randomization of participants across 9 experimental conditions
- Ensures balanced assignment across demographic factors
- Generates condition assignment files for platform integration
- Includes randomization validation and balance checking

**`information_packages.py`**: Automated generation of information packages
- Creates minimal, moderate, and comprehensive information sets
- Formats content for text, visualization, and video conditions
- Ensures content accuracy and consistency across conditions

**`survey_tools.py`**: Survey deployment and response tracking
- Integrates with Qualtrics for survey administration
- Tracks completion rates and response timing
- Manages longitudinal follow-up scheduling

### Statistical Analysis (`analysis/`)

**`primary_analysis.R`**: Core statistical tests for the experiment
```r
# 3x3 factorial ANOVA with planned contrasts
# Tests for linear and quadratic information load effects
# Examines information format interaction effects
```

**`mediation_analysis.R`**: Tests cognitive load as mediator
```r
# Bootstrap mediation analysis using lavaan package
# Tests whether cognitive load mediates information load effects
# Calculates indirect effects and confidence intervals
```

**`longitudinal_models.R`**: Mixed-effects models for follow-up data
```r
# Growth curve models for satisfaction over time
# Random effects for individual differences
# Examines persistence of treatment effects
```

### Visualization (`visualization/`)

**`descriptive_plots.py`**: Basic descriptive visualizations
- Participant flow diagrams
- Demographic distribution plots  
- Treatment condition summaries

**`effect_plots.R`**: Treatment effect visualization
- Forest plots for effect sizes across conditions
- Interaction plots for information load × format
- Confidence interval visualizations

**`publication_figures.R`**: Manuscript-ready figures
- High-resolution plots with journal formatting
- Combined multi-panel figures
- Statistical annotation integration

## Reproducibility

### Environment Setup
```bash
# Python dependencies
pip install pandas numpy scipy matplotlib seaborn plotly

# R dependencies  
install.packages(c("tidyverse", "lme4", "lavaan", "ggplot2", "cowplot"))
```

### Execution Order
1. Run `randomization.py` to assign participants to conditions
2. Use `information_packages.py` to generate experimental materials
3. Deploy surveys using `survey_tools.py`
4. Clean data with `data_cleaning.py` 
5. Execute primary analysis with `primary_analysis.R`
6. Run mediation and longitudinal models
7. Generate visualizations and figures

### Data Security
- All participant data stored in encrypted databases
- Personal identifiers separated from research data
- IRB-approved data management protocols followed
- Automated backup and version control systems

## Key Results Generated

### Primary Outputs
- **Treatment effect estimates**: Effect sizes and confidence intervals for all comparisons
- **Mediation results**: Direct and indirect effects through cognitive load
- **Longitudinal trajectories**: Growth curves for satisfaction and academic outcomes
- **Publication figures**: Manuscript-ready visualizations

### Reproducible Reporting
All analyses use R Markdown and Jupyter notebooks for reproducible reporting. Results can be regenerated from raw data using the provided scripts.

### Version Control
Git repository tracks all code changes with detailed commit messages. Major analysis versions tagged for manuscript revisions.

## Contact and Support
For questions about code implementation or replication, contact the research team through the project repository issues system.