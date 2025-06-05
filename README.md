# Descriptive-statistics
This repository contains an R script for performing descriptive statistical analysis on a dataset named WHEAT, which includes agro-morphological traits of wheat genotypes. The analysis covers both basic statistics (mean, median, minimum, maximum) and extended statistics (standard deviation, variance, skewness, kurtosis) using the pastecs package.The script is structured step-by-step, making it easy to follow and modify. Additionally, the results are exported to an Excel file using the writexl package for convenient sharing and reporting.
This project is useful for researchers, students, and data analysts working with crop datasets who want to understand trait variation and distribution within their data. It emphasizes reproducibility, clarity, and simplicity in statistical reporting.

# Load the dataset (assuming 'WHEAT' is already loaded in your environment)
# If not, you would typically load it using read.csv(), read_excel(), etc.

# 1. Basic descriptive summary (mean, median, min, max, etc.)
summary(WHEAT)

# 2. Load the 'pastecs' package which provides advanced descriptive statistics
library(pastecs)

# 3. Compute descriptive statistics: mean, standard deviation, skewness, kurtosis, etc.
stat.desc(WHEAT)

# 4. Prevent R from displaying scientific notation (e.g., 1.0e+05 becomes 100000)
options(scipen = 999)

# 5. Load 'writexl' package to export the result to an Excel file
library(writexl)

# 6. Write the output of stat.desc() into an Excel file named "wheat table.xlsx"
write_xlsx(stat.desc(WHEAT), "wheat table.xlsx")
