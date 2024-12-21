# Analysis of Photovoltaic (PV) Output Stability and Predictive Factors

## **Overview**
This report investigates the stability and predictability of photovoltaic (PV) output and its linkage to solar radiation. The findings confirm that PV output is stable and closely tied to solar radiation, with no significant trends or fluctuations over time. While cloudy days reduce output, high UV index days compensate, ensuring reliable performance. Using seasonal decomposition and Granger causality tests, we confirm solar radiation's predictive influence on PV output. Based on these findings, **expanding the PV array is recommended**.

---

## **Univariate Analysis**

### **Seasonality in PV Output**
- **Figure 1:** Daily PV output shows visible seasonality, with higher outputs during specific periods of the year.
- A red smoothing line highlights seasonal patterns by filtering daily fluctuations.
- Enhanced visualization is achieved through contrasting colors, customized axis labels, and titles.

### **Annual Variability**
- **Figure 2:** Box plot of mean annual PV output shows an average of **2.045 kWh per year**.
- Notable variability exists, particularly during the years **2019–2021**, with significant differences in both mean and variance.

### **Periodic Autocorrelation**
- **Figure 3:** Autocorrelation Function (ACF) plot shows a sinusoidal pattern, reflecting a strong annual cycle with diminishing correlation over time.
- Peak size variation may result from changing seasonal intensity, nonlinear effects, or anomalies.

### **Partial Autocorrelation**
- **Figure 4:** Partial Autocorrelation Function (PACF) plot reveals the non-persistent nature of daily autocorrelation. 
- Rapid decline in correlation strength is observed at subsequent lags, with meaningful correlations truncated to lags between 1 and 180.

### **Spectral Analysis**
- Using the **Augmented Dickey-Fuller (ADF) test**, the data was identified as non-stationary (p-value: 0.5442).
- A **Fast Fourier Transform** revealed a significant annual cycle in solar energy generation.
- **Figure 5:** Spectral density plot confirms seasonality, with logarithmic scaling improving visibility of relevant frequencies.

---

## **Multivariate Analysis**

### **Correlation Matrix**
- **Figure 6:** Heatmap reveals strong correlations between PV output and:
  - Solar radiation (**0.93**)
  - UV index (**0.89**)
  - Maximum temperature (**0.74**, positively correlated)
  - Humidity (**-0.77**, negatively correlated)
- Solar radiation and UV index are nearly perfectly correlated (**0.95**), reflecting shared reliance on sunlight intensity.

### **Regression and Predictive Insights**
- Regression analysis confirms the strong linear relationship between solar radiation and PV output.
- Granger causality tests show:
  - Solar radiation and cloud cover significantly predict future PV output.
  - Past values of these variables carry distinct predictive signals, with extremely low p-values confirming statistical significance.

### **Scatter Plot Analysis**
- Strong negative correlation between cloud cover and PV output at higher UV index levels.
- Lower UV index categories display flatter trends, suggesting other influencing factors.
- Variability around trend lines implies additional variables may affect PV efficiency.

---

## **Conclusions**
1. **PV Output Stability:** PV output is stable and closely tied to solar radiation.
2. **Seasonal Influence:** A strong annual cycle exists, confirmed through spectral analysis.
3. **Predictive Relationships:** Solar radiation and cloud cover are significant predictors of PV output, as confirmed by Granger causality tests.
4. **Recommendation:** Expand the PV array based on the reliable and predictable performance demonstrated in this analysis.
