# Gradient Descent Implementation for Linear Regression

This repository contains a Jupyter Notebook (`gradient-descent-implementation.ipynb`) that demonstrates a basic implementation of the gradient descent algorithm for optimizing a simple linear regression model.  It's designed to be educational, showing the key steps and visualizing the process.

## Overview

The notebook does the following:

1.  **Imports Libraries:**  Uses `numpy` for numerical computation, `matplotlib` and `seaborn` for plotting, and `mpl_toolkits.mplot3d` for 3D visualization.  No external data is needed; a simple dataset is created within the notebook.

2.  **Defines `gradientDescent` Function:**
    *   Takes input data (`x`, `y`), number of iterations, and learning rate as arguments.
    *   Initializes the slope (`m`) and y-intercept (`b`) to 0.
    *   Iteratively updates `m` and `b` using the gradient descent update rule:
        *   Calculates the predicted y values (`y_pred`).
        *   Calculates the cost (Mean Squared Error).
        *   Calculates the gradients of the cost function with respect to `m` and `b`.
        *   Updates `m` and `b` by subtracting the learning rate times their respective gradients.
    *   Tracks the cost, `m`, and `b` values over each iteration in lists (`cost_history`, `m_history`, `b_history`).
    *   Returns the final `m`, `b`, and the history lists.

3.  **Defines `plotResults` Function:**
    *   Creates a series of plots to visualize the results:
        *   **Data & Regression Line:** Shows the original data points and the final regression line fitted by the algorithm.
        *   **Cost Function History:** Plots the cost (MSE) over each iteration, demonstrating the convergence of the algorithm.  The y-axis is on a log scale to better show the decrease in cost.
        *   **Parameter Trajectory:**  Shows the path of the `m` (slope) and `b` (intercept) values during the optimization process.  This visualizes how the parameters converge to their optimal values.
        *   **3D Cost Surface:**  Plots the cost function as a 3D surface, with `m` and `b` on the x and y axes, and the cost on the z-axis. The path of the gradient descent is overlaid on this surface.

4.  **Main Execution Block (`if __name__ == '__main__':`)**:
    *   Creates a simple linear dataset: `x = [1, 2, 3, 4, 5]` and `y = [5, 7, 9, 11, 13]`.  This represents a line with a slope of 2 and a y-intercept of 3, plus some noise.
    *   Calls the `gradientDescent` function with the data, 1000 iterations, and a learning rate of 0.08.
    *   Calls the `plotResults` function to generate the visualizations.

## Key Concepts Illustrated

*   **Gradient Descent:** The core algorithm for minimizing the cost function.
*   **Linear Regression:**  Fitting a straight line to data.
*   **Cost Function (Mean Squared Error):**  A measure of how well the regression line fits the data.
*   **Learning Rate:** A hyperparameter that controls the step size during gradient descent.
*   **Convergence:**  The process of the algorithm approaching the optimal solution.
*   **Data Visualization:** Using plots to understand the algorithm's behavior.

## How to Run

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/kunalPisolkar24/gradientDescent.git
    ```
2.  **Navigate to the directory:**
    ```bash
    cd gradientDescent
    ```
3.  **Open the Jupyter Notebook:**
    ```bash
    jupyter notebook gradient-descent-implementation.ipynb
    ```
4.  **Run all cells** in the notebook.  The plots will be displayed within the notebook.

## Dependencies

*   `numpy`
*   `matplotlib`
*   `seaborn`
*   `mpl_toolkits` (specifically, `mplot3d`)

These can typically be installed via `pip`:

```bash
pip install numpy matplotlib seaborn
```

