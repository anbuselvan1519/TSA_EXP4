## Developed by: Anbuselvan S
## Register No: 212223240008
## Date:

# Ex.No: 04   FIT ARMA MODEL FOR TIME SERIES

## AIM:
To implement ARMA model in python.

## ALGORITHM:
1. Import necessary libraries.
   
2. Set up matplotlib settings for figure size.
   
3. Define an ARMA(1,1) process with coefficients ar1 and ma1, and generate a sample of 1000
data points using the ArmaProcess class. Plot the generated time series and set the title and x-
axis limits.

4. Display the autocorrelation and partial autocorrelation plots for the ARMA(1,1) process using
plot_acf and plot_pacf.

5. Define an ARMA(2,2) process with coefficients ar2 and ma2, and generate a sample of 10000
data points using the ArmaProcess class. Plot the generated time series and set the title and x-
axis limits.

6. Display the autocorrelation and partial autocorrelation plots for the ARMA(2,2) process using
plot_acf and plot_pacf.

## PROGRAM:
```
import numpy as np
import matplotlib.pyplot as plt
from statsmodels.tsa.arima_process import ArmaProcess
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf

plt.rcParams['figure.figsize'] = [10, 7.5]

ARMA_1 = ArmaProcess([1, 0.33], [1, 0.9]).generate_sample(nsample=1000)
plt.plot(ARMA_1); plt.title('Simulated ARMA(1,1) Process'); plt.xlim([0, 200]); plt.show()
plot_acf(ARMA_1); plot_pacf(ARMA_1)

ARMA_2 = ArmaProcess([1, 0.33, 0.5], [1, 0.9, 0.3]).generate_sample(nsample=10000)
plt.plot(ARMA_2); plt.title('Simulated ARMA(2,2) Process'); plt.xlim([0, 200]); plt.show()
plot_acf(ARMA_2); plot_pacf(ARMA_2)

```

## OUTPUT:

### Simulated ARMA(1,1) Process:
![image](https://github.com/user-attachments/assets/f4f936e5-3021-4269-a262-6f77d1f379c7)

### Simulated ARMA(2,2) Process:
![image](https://github.com/user-attachments/assets/21b6bad4-bdd8-4d2e-83ce-307bf90d5233)

### Partial Autocorrelation:
![image](https://github.com/user-attachments/assets/454df7a2-0b08-4e74-bd96-e2e1fee72a2a)

### Autocorrelation:
![image](https://github.com/user-attachments/assets/6d57e8eb-397d-42eb-a359-957a22ac1b88)

## RESULT:
Thus, a python program is created to fir ARMA Model successfully.
