# Anti-politics

This replication package accompanies the article in *The Economist* on anti-politics and negative partisanship. It includes the necessary scripts to reproduce the data, charts, and key analyses referenced in the article.

## Overview

The package contains three R scripts located in the `scripts` folder:
1. **data-generation.R**
2. **chart-replication.R**
3. **analysis-replication.R**

To fully replicate the analysis, you should run these scripts **in order**:

1. **data-generation.R**  
   This script processes and constructs the datasets used in the analysis. It pulls together various data sources on partisanship, electoral systems, government effectiveness, military spending, migration, and other variables relevant to the study.

2. **chart-replication.R**  
   After generating the data, this script replicates the visualizations featured in the article. It reproduces the key figures related to partisanship sentiment, affection gaps, and political attitudes over time across different countries. 

3. **analysis-replication.R**  
   This final script performs the main statistical analyses described in the article. It includes regressions and stress-tests that explore relationships between negative partisanship, military spending, migration, economic growth, and other variables.  
   **Note:** As we stress in the article - the analysis does not establish causality.

## Running the scripts

To replicate the analysis, you should execute the scripts in the following order:

1. **data-generation.R**: Prepares the data for analysis.
2. **chart-replication.R**: Produces the charts and figures used in the article.
3. **analysis-replication.R**: Replicates the regression analysis and other statistical results.

### Dependencies

Before running the scripts, ensure that the following R packages are installed:

- `tidyverse`
- `ggplot2`
- `QuickCoefPlot`
- `countrycode`
- `haven`
- `WDI`
- `cshapes`
- `sp`
- `rgeos`
- `dplyr`
- `vdemdata`
- `cli`
- `readstata13`
- `readxl`
- `progress` (used for displaying progress bars in the data-generation process)

You can install all the required packages using the following R command:

```R
install.packages(c('tidyverse', 'ggplot2', 'QuickCoefPlot', 'countrycode', 'haven', 'readstata13', 'readxl', 'progress', 'WDI', 'cshapes', 'sp', 'rgeos', 'dplyr', 'cli'))
```

## Variables

The key variables used in the analysis include:

- **INPARTY**: Measures the positive feelings respondents have towards their in-party (0-10 scale).
- **OUTPARTY**: Measures the positive feelings respondents have towards their out-party (0-10 scale).
- **negative_partisanship**: Calculated as the difference between in-party and out-party affection (INPARTY - OUTPARTY).

Each script builds on these variables to create visualizations or conduct statistical analysis. For more details on the variables and how they are constructed, refer to the data-generation script.

## Sources

This project uses various publicly available data sources, including but not limited to:

- **World Bank** for government effectiveness and economic indicators.
- **V-Dem Institute** for electoral system data and political polarization measures.
- **CSES** (Comparative Study of Electoral Systems) for in-party and out-party affection data. 
- **SIPRI** (Stockholm International Peace Research Institute) for military expenditure data.
- **United Nations** for population and migration data.
- **Edelman Trust Barometer**, **World Values Survey**, and **Gallup** for public sentiment data.

These sources have been combined and processed to allow us to conduct our analysis..

## Suggested citation
> The Economist (2024). The anti-politics eating the West. *The Economist*.

## Acknowledgments

We would like to extend our thanks to the following academics for valuable conversations and assistance.

- **Diego Garzia** (University of Lausanne)
- **Frederico Ferreira da Silva** (University of Lausanne)
- **Noam Gidreon** (Hebrew University of Jerusalem)
- **Will Horne** (Clemenson University)
- **Markus Wagner** (University of Vienna)
- **Sean J. Westwood** (Dartmouth College)
- **Nikita Melnikov** (Nova School of Business and Economics)

## Contact and further information

If you encounter any issues or have questions about the replication package, feel free to reach out via the GitHub issue tracker.

---
