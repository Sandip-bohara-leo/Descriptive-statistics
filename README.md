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

# Analysis and result
 # 1. Basic descriptive summary (mean, median, min, max, etc.)
> summary(KHEM_DATA)
 Accession name          DTE             DTH             DTF             DOM       
 Length:116         Min.   :14.00   Min.   : 99.0   Min.   :102.0   Min.   :132.0  
 Class :character   1st Qu.:15.00   1st Qu.:104.0   1st Qu.:110.0   1st Qu.:140.0  
 Mode  :character   Median :18.00   Median :106.0   Median :112.0   Median :144.0  
                    Mean   :18.61   Mean   :108.1   Mean   :113.6   Mean   :144.4  
                    3rd Qu.:20.25   3rd Qu.:110.0   3rd Qu.:114.0   3rd Qu.:146.0  
                    Max.   :27.00   Max.   :132.0   Max.   :145.0   Max.   :171.0  
       PH               SE             SPL              FLL             FLW       
 Min.   : 34.80   Min.   : 2.70   Min.   : 6.200   Min.   : 8.08   Min.   :0.560  
 1st Qu.: 83.05   1st Qu.:10.80   1st Qu.: 8.100   1st Qu.:10.90   1st Qu.:0.900  
 Median : 95.89   Median :15.95   Median : 8.800   Median :12.00   Median :1.020  
 Mean   : 92.33   Mean   :15.20   Mean   : 9.102   Mean   :12.31   Mean   :1.041  
 3rd Qu.:101.42   3rd Qu.:18.97   3rd Qu.:10.055   3rd Qu.:13.42   3rd Qu.:1.180  
 Max.   :129.50   Max.   :31.30   Max.   :13.140   Max.   :20.00   Max.   :1.580  
      NOT              SPPS             SPSP           SPS              SL       
 Min.   : 3.000   Min.   : 7.000   Min.   :2.00   Min.   :16.80   Min.   :5.122  
 1st Qu.: 6.000   1st Qu.: 9.000   1st Qu.:2.80   1st Qu.:37.00   1st Qu.:5.640  
 Median : 7.200   Median : 9.400   Median :3.00   Median :40.80   Median :5.940  
 Mean   : 8.286   Mean   : 9.445   Mean   :2.91   Mean   :40.96   Mean   :5.964  
 3rd Qu.: 9.150   3rd Qu.:10.000   3rd Qu.:3.00   3rd Qu.:45.00   3rd Qu.:6.269  
 Max.   :23.800   Max.   :12.000   Max.   :4.00   Max.   :65.80   Max.   :6.996  
       SW              ST             THSW             TY        
 Min.   :2.394   Min.   :2.014   Min.   :17.60   Min.   :0.4584  
 1st Qu.:3.029   1st Qu.:2.544   1st Qu.:31.50   1st Qu.:1.1050  
 Median :3.285   Median :2.704   Median :35.80   Median :1.3750  
 Mean   :3.230   Mean   :2.708   Mean   :36.41   Mean   :1.4238  
 3rd Qu.:3.462   3rd Qu.:2.862   3rd Qu.:41.55   3rd Qu.:1.7184  
 Max.   :3.740   Max.   :3.322   Max.   :53.10   Max.   :2.5437  
> # 2. Load the 'pastecs' package which provides advanced descriptive statistics
> library(pastecs)
> # 3. Compute descriptive statistics: mean, standard deviation, skewness, kurtosis, etc.
> stat.desc(KHEM_DATA)
         Accession name          DTE            DTH            DTF            DOM
nbr.val              NA  116.0000000   116.00000000   116.00000000   116.00000000
nbr.null             NA    0.0000000     0.00000000     0.00000000     0.00000000
nbr.na               NA    0.0000000     0.00000000     0.00000000     0.00000000
min                  NA   14.0000000    99.00000000   102.00000000   132.00000000
max                  NA   27.0000000   132.00000000   145.00000000   171.00000000
range                NA   13.0000000    33.00000000    43.00000000    39.00000000
sum                  NA 2159.0000000 12541.00000000 13179.00000000 16748.00000000
median               NA   18.0000000   106.00000000   112.00000000   144.00000000
mean                 NA   18.6120690   108.11206897   113.61206897   144.37931034
SE.mean              NA    0.3938758     0.57506555     0.69779816     0.65968226
CI.mean              NA    0.7801922     1.13909417     1.38220386     1.30670360
var                  NA   17.9960270    38.36124438    56.48298351    50.48095952
std.dev              NA    4.2421724     6.19364548     7.51551618     7.10499539
coef.var             NA    0.2279259     0.05728912     0.06615068     0.04921062
                    PH           SE          SPL          FLL          FLW         NOT
nbr.val    116.0000000  116.0000000  116.0000000  116.0000000 116.00000000 116.0000000
nbr.null     0.0000000    0.0000000    0.0000000    0.0000000   0.00000000   0.0000000
nbr.na       0.0000000    0.0000000    0.0000000    0.0000000   0.00000000   0.0000000
min         34.8000000    2.7000000    6.2000000    8.0800000   0.56000000   3.0000000
max        129.5000000   31.3000000   13.1400000   20.0000000   1.58000000  23.8000000
range       94.7000000   28.6000000    6.9400000   11.9200000   1.02000000  20.8000000
sum      10709.9420000 1763.6800000 1055.8800000 1427.6800000 120.80000000 961.2000000
median      95.8900000   15.9500000    8.8000000   12.0000000   1.02000000   7.2000000
mean        92.3270862   15.2041379    9.1024138   12.3075862   1.04137931   8.2862069
SE.mean      1.3933791    0.5126852    0.1419264    0.1983912   0.01946931   0.3361233
CI.mean      2.7600158    1.0155307    0.2811288    0.3929748   0.03856495   0.6657955
var        225.2146130   30.4901479    2.3365993    4.5656533   0.04397025  13.1055472
std.dev     15.0071521    5.5217885    1.5285939    2.1367389   0.20969086   3.6201585
coef.var     0.1625433    0.3631767    0.1679328    0.1736115   0.20135877   0.4368897
                  SPPS         SPSP          SPS           SL           SW           ST
nbr.val   116.00000000 116.00000000  116.0000000 116.00000000 116.00000000 116.00000000
nbr.null    0.00000000   0.00000000    0.0000000   0.00000000   0.00000000   0.00000000
nbr.na      0.00000000   0.00000000    0.0000000   0.00000000   0.00000000   0.00000000
min         7.00000000   2.00000000   16.8000000   5.12200000   2.39400000   2.01400000
max        12.00000000   4.00000000   65.8000000   6.99600000   3.74000000   3.32200000
range       5.00000000   2.00000000   49.0000000   1.87400000   1.34600000   1.30800000
sum      1095.60000000 337.60000000 4751.8000000 691.84200000 374.65200000 314.09800000
median      9.40000000   3.00000000   40.8000000   5.94000000   3.28500000   2.70400000
mean        9.44482759   2.91034483   40.9637931   5.96415517   3.22975862   2.70774138
SE.mean     0.08455142   0.03618583    0.6221046   0.04340052   0.02751174   0.02443631
CI.mean     0.16748009   0.07167716    1.2322694   0.08596807   0.05449547   0.04840362
var         0.82927736   0.15189205   44.8936342   0.21849817   0.08779994   0.06926745
std.dev     0.91064667   0.38973331    6.7002712   0.46743788   0.29631055   0.26318709
coef.var    0.09641750   0.13391310    0.1635657   0.07837453   0.09174387   0.09719802
                 THSW           TY
nbr.val   116.0000000 116.00000000
nbr.null    0.0000000   0.00000000
nbr.na      0.0000000   0.00000000
min        17.6000000   0.45838150
max        53.1000000   2.54366089
range      35.5000000   2.08527938
sum      4223.8600000 165.15608735
median     35.8000000   1.37502248
mean       36.4125862   1.42375937
SE.mean     0.7272779   0.04371056
CI.mean     1.4405975   0.08658221
var        61.3562402   0.22163113
std.dev     7.8330224   0.47077715
coef.var    0.2151185   0.33065781
> # 4. Prevent R from displaying scientific notation (e.g., 1.0e+05 becomes 100000)
> options(scipen = 999)
> # 5. Load 'writexl' package to export the result to an Excel file
> library(writexl)
> # 6. Write the output of stat.desc() into an Excel file named "wheat table.xlsx"
> write_xlsx(stat.desc(KHEM_DATA), "wheat table.xlsx")
> # 7. know the directory of of stat.desc() into an Excel file named "wheat table.xlsx"
> getwd()
[1] "C:/Users/Pc/OneDrive/Documents"
