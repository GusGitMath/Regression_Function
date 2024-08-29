# Function Fitting Utility

**Date Written:** September 2020

## Overview

This utility provides a convenient way to fit a user-defined function to a set of data points. The code performs the following tasks:

1. **Curve Fitting:** Uses non-linear least squares optimization to fit a function to the provided `xdata` and `ydata`.
2. **Error Estimation:** Computes the errors associated with the fitted parameters.
3. **Plotting:** Visualizes the fitted function alongside the original data points, including error bars.
4. **Chi-Squared Calculation:** Optionally calculates and displays the Chi-Squared and Reduced Chi-Squared values.
5. **Covariance Matrix:** Optionally displays the covariance matrix of the fitted parameters.

## Key Features

- **Custom Function Input:** The function to be fitted can be customized by the user.
- **Flexible Parameter Handling:** Supports fitting functions with 2 to 4 parameters.
- **Error Handling:** Automatically handles errors in both `xdata` and `ydata` if provided.
- **Plot Customization:** Allows for detailed customization of the plot appearance, including colors, labels, and titles.
- **Statistical Output:** Can display important statistical information like Chi-Squared values and the covariance matrix.

## Usage

1. Define the data to be fitted (`xdata`, `ydata`).
2. Define the function to be fitted.
3. Call the `fit_function` with the required parameters.

Example:
```python
xdata = np.linspace(0, 4, 50)
ydata = np.sin(xdata) + np.random.normal(0, 0.1, xdata.size)

def example_func(x, a, b, c):
    return a * np.sin(b * x + c)

params, params_error = fit_function(xdata, ydata, example_func, n=3)
```

## Dependencies

- `numpy`: For numerical operations and array handling.
- `matplotlib`: For plotting the fitted functions and data points.
- `scipy.optimize.curve_fit`: For performing the curve fitting.
- `IPython.display`: For displaying formatted output in Jupyter notebooks.
- `sympy`: For handling and displaying the covariance matrix.

## Installation

Ensure you have the required Python libraries installed:
```bash
pip install numpy matplotlib scipy sympy
```
