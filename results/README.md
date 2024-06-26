# Results Directory

## Summary

This directory contains the output of the analysis and preprocessing scripts for the DAB converter simulation data. The results include statistical summaries, visualizations, and comprehensive PDF reports generated from the simulation data.


### Figures

This subdirectory contains various plots generated during the analysis. Each plot provides visual insights into different aspects of the simulation data.

**Time Series Plot (Vlow)**

This plot shows the voltage (Vlow) of the converter. The voltage fluctuates over time, with a general upward trend and periodic fluctuations. These fluctuations could be caused by factors such as changes in load or switching events in the converter.

<div align="center">
  <img src="/results/figures/time_series_plot.png" alt="convertidor"/>
</div>

<div align="center"> Time Series (Vlow)  </div> 
<br>

**Area Chart (I_LK)**

This plot represents the current (I_LK) flowing through the inductor using an area chart. The area under the curve represents the total energy stored in the inductor. The current fluctuates over time, with periods of high and low current.

<div align="center">
  <img src="/results/figures/area_chart.png" alt="convertidor"/>
</div>

<div align="center"> Area Chart (I_LK)  </div> 
<br>

**Line Chart (VHigh)**

This plot shows the voltage (VHigh)of the converter. stabilizing the voltage at an average value of 36V.

The plots and the relationships between the variables, it appears that the data is separable to some extent. The time series plots of Vlow, I_LK, and VHigh each capture distinct aspects of the converter's behavior, and the relationships between these variables provide additional insights into the system dynamics.
However, it's important to note that the separability of the data may depend on the specific operating conditions and parameters of the DAB converter.

<div align="center">
  <img src="/results/figures/line_chart.png" alt="convertidor"/>
</div>

<div align="center"> Line Chart (VHigh)  </div> 
<br>

**Normalized Vlow Plot**

This plot shows the variable Vlow over time, with the data normalized to fit a scale between 0 and 1. The normalization has been done to allow easier comparison between different variables. This makes it easier to visualize patterns and trends in the time series, providing a clear perspective of how Vlow varies over the simulation period.
<div align="center">
  <img src="/results/figures/normalized_time_series_plot.png" alt="convertidor"/>
</div>

<div align="center"> Normalized time series Vlow  </div> 
<br>



#### Files

- *area_chart.png*: An area chart showing the leakage current over time.
- *line_chart.png*: A line chart showing the high voltage, low voltage, and leakage current over time.
- *time_series_plot.png*: A time series plot showing the low voltage over time.
- *normalized_time_series_plot.png*: A time series plot showing the normalized low voltage over time.

### Analysis_results.pdf

This PDF report compiles all the results from the analysis and preprocessing scripts. It includes:
<div align="center">
  <img src="/results/figures/pdf.png" alt="convertidor"/>
</div>

<div align="center"> Documento pdf  </div> 
<br>

- *Show data first 5 lines*: The first few rows of the DataFrame to provide a quick overview of the data structure.
  
- *Statistical Analysis*: Summary statistics for the filtered data within a specific time range.

  **Table 1: Statistics of Filtered Data**
  
    |       |   Time   |   I_LK   |  VHigh  |  Vlow   |   VLK   |
  |:-----:|:--------:|:--------:|:-------:|:-------:|:-------:|
  | count | 400.000000 | 400.000000 | 400.000000 | 400.000000 | 400.000000 |
  | mean  | 0.006998   | 0.501450   | 0.028634   | 7.515296   | 0.496700   |
  | std   | 0.000578   | 0.282367   | 0.003058   | 0.209851   | 0.309936   |
  | min   | 0.006000   | 0.015010   | 0.023220   | 6.931500   | 0.167117   |
  | 25%   | 0.006499   | 0.254926   | 0.025727   | 7.367886   | 0.186799   |
  | 50%   | 0.006998   | 0.501030   | 0.028683   | 7.558694   | 0.502576   |
  | 75%   | 0.007496   | 0.748246   | 0.031346   | 7.648890   | 0.806880   |
  | max   | 0.007995   | 0.983349   | 0.034242   | 7.810822   | 0.824580   |
  

  **Table 2: Preprocessing Results**

|                                |                      |
|:------------------------------:|:--------------------:|
| **Mean of Vlow:**              | 6.014398864457081    |
| **Standard deviation of Vlow:**| 0.5885596907119182   |
| **Coefficient of variation of Vlow:** | 0.0978584400496104 |
| **Interquartile Range (IQR) of Vlow:** | 0.539257554651865  |
| **Skewness of Vlow:**          | 0.539257554651865    |

Vlow is moderately separable.

- *Normalization Results*: Statistical summaries and plots of the normalized data.

  **Table 3: Normalized Data - Statistics of Filtered Data**

|       |   Time   |   I_LK   |  VHigh  |  Vlow   |   VLK   |
|:-----:|:--------:|:--------:|:-------:|:-------:|:-------:|
| count | 400.000000 | 400.000000 | 400.000000 | 400.000000 | 400.000000 |
| mean  | 0.006998   | 0.501450   | 0.028634   | 0.935750   | 0.496700   |
| std   | 0.000578   | 0.282367   | 0.003058   | 0.026129   | 0.309936   |
| min   | 0.006000   | 0.015010   | 0.023220   | 0.863060   | 0.167117   |
| 25%   | 0.006499   | 0.254926   | 0.025727   | 0.917396   | 0.186799   |
| 50%   | 0.006998   | 0.501030   | 0.028683   | 0.941154   | 0.502576   |
| 75%   | 0.007496   | 0.748246   | 0.031346   | 0.952384   | 0.806880   |
| max   | 0.007995   | 0.983349   | 0.034242   | 0.972547   | 0.824580   |

    
- *Linear Regression Analysis*: Results of the regression model, including mean squared error (MSE) and coefficient of determination (R^2).

#### To analyze the results of separability where CV, IQR and Skewness are present, we explain as follows:

**Coefficient of variation (CV)**: A lower CV indicates a more clustered distribution and potentially higher separability, a CV below 0.1 is interpreted as “highly separable”, 0.1 to 0.2 as “moderately separable” and above 0.2 as “poorly separable”.

The CV value is approximately 0.098, lower than 0.1, indicating high separability. This suggests that the Vlow values are relatively stable with low relative variability compared to the mean.

**Interquartile range (IQR)**: represents the difference between the 75th and 25th percentiles of the data, indicating the dispersion of the median 50% of the data points. A non-zero IQR indicates some variability in the data, while a positive IQR indicates that there is variability in the middle 50% of the data.

**Skewness**: A skewness value close to 0 suggests a symmetric distribution, while a positive or negative skewness indicates a skewed distribution. A skewness value of approximately 0.793 indicates a distribution that is moderately skewed to the right. This means that there are more values at the lower end of the distribution and fewer at the upper end.

The Vlow variable demonstrates high consistency and stability, making it a good candidate for future analysis and possible control strategies in the simulation of the OBD converter. This provides a global understanding of the Vlow distribution.
 - With a cv of 0.0978584400496104, Vlow is highly separable, meaning that there is little relative dispersion in the Vlow values.

- An IQR of 0.539257554651865 and skewness of 0.7929962200966385 suggest that the variability and skewness are moderate, which could indicate moderate separability in certain contexts, depending on other factors such as the distribution of Vlow values.

#### The results of the MSE and R^2 are explained as follows: 

**Mean Squared Error (MSE)**:

The MSE obtained is 0.10163277151676858, which is a relatively low value. This indicates that the linear regression model performs well in terms of accuracy in predicting the value of "Vlow" from the independent variables ("Time", "I_LK", "VHigh", "VLK").

**Coefficient of Determination (R^2)**:

The R^2 obtained is 0.7097821756, which represents 71% of variance explained by the model. This means that 71% of the variations in "Vlow" can be explained by the independent variables. In general, an R^2 value greater than 0.5 is considered acceptable for a linear regression model.

Do the MSE and R^2 results suggest that the linear regression model has good predictive power and explains a significant amount of the variance in the target variable "Vlow". This indicates that the model may be useful for estimating the value of "Vlow" based on the values of the independent variables.
