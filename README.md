# Chocolate Chip Cookie Analysis
**This project performs a data analysis of ingredient data for chocolate chip cookie recipes to determine whether changing the amount of fat or sugar impacts the rating of a chocolate chip cookie recipe:**
* Prepared data for analysis using dplyr functions to remove duplicate information, categorize ingredients, convert to standard measurements, and summarize volume by category.
* Identified and removed outliers using the 1.5(IQR) rule
* Analyzed the distribution of each variable by plotting histograms in ggplot2
* Explored the relationship between variables by plotting scatterplots in ggplot2
* Computed and analyzed descriptive statistics in R
* Created three linear regression models and compared them using adjusted R-squared and Akaike information criterion (AIC) values

## Authors
[@databymir] (https://github.com/databymir)

## Installation
### Codes and Resources Used
Editor Used: RStudio
R Version: R-4.3.3

### R Packages Used
#### General Purpose
tidyverse

#### Data Manipulation
dplyr (installed as part of tidyverse))
janitor

#### Data Visualization
ggplot2 (installed as part of tidyverse)

## Data
### Source Data
The dataset is composed of information about chocolate chip cookie recipes. The data was provided by Elle O'Brien in a GitHub repository.

### Data Acquisition
The data was acquired by downloading the .csv file from O'Brien's GitHub repository at https://github.com/the-pudding/data/tree/master/cookies.

### Data Preprocessing
The column names meet syntax requirements for R, with the exception of the first column. The first column has no header and the values are index numbers starting with 1 and providing a row index for all 1,990 observations. My analysis changes the columns to snake_case out of personal preference but this is not required. Additionally, only columns relevant to the flour-fat-sugar analysis were retained in my analysis dataset.

There are missing values in the Rating variable, so data imputation and NA removal should be considered. After summarizing the flour, fat, and sugar amounts, I deleted NA values, as spot-checking determined that these values were appearing for recipes that use cake and cookie mixes.

In order to summarize information for flour-fat-sugar ratio analysis, I categorized ingredients, converted them to one unit of measurement, and summarized by flour, fat, and sugar category. Then, the amounts were converted to a standard unit "parts" where each recipe use three parts flour.

The summarized information was pivoted and merged with a tibble that summarized rating by recipe index to obtain the dataset used in the project's analysis.

## Code
├── choc_chip_cookie_ingredients.csv

├── cookie_analysis.qmd

├── LICENSE

├── README.md

└── .gitignore

## Results
Based on the visualizations, descriptive statistics, and models generated, changing the ratio of fat or sugar does not impact the overall rating of a cookie recipe.

## References
The Culinary Pro. (n.d.). *Cookies.* https://www.theculinarypro.com/cookies 

O'Brien, Elle. (2018, May 10). *cookies.* GitHub. https://github.com/the-pudding/data/tree/master/cookies

## License
For this github repository, the License used is [MIT License](https://opensource.org/license/mit/).
