# Simulated Annealing for Ackley Function Optimization in MATLAB

**Prof. Aboud BARSEKH-ONJI (D.Sc.)**

**Email: aboud.barsekh@anahuac.mx**

**https://orcid.org/0009-0004-5440-8092**

**Universidad Anáhuac México Sur - Facultad de Ingeniería**

This repository contains a **MATLAB** script that implements the **Simulated Annealing** optimization algorithm to find the global minimum of the **Ackley Function**, a complex and multimodal mathematical function commonly used for testing optimization algorithms.

The code was developed by **Prof. Aboud BARSEKH-ONJI (D.Sc.)** from the Faculty of Engineering at Universidad Anáhuac México Sur.

---

## Script Description

The script performs the following main actions:

1.  **Defines the Ackley Function**: A non-convex function with a global minimum at `(0, 0)` surrounded by numerous local minima, which makes it a challenging benchmark for optimization algorithms. The function is defined as:
    $$f(x, y) = -20 \exp\left(-0.2 \sqrt{0.5(x^2 + y^2)}\right) - \exp\left(0.5(\cos(2\pi x) + \cos(2\pi y))\right) + 20 + e$$

2.  **Implements the Simulated Annealing Algorithm**:
    * It starts at a random solution (point) within the function's domain.
    * In each iteration, it generates a new neighboring solution.
    * If the new solution is better (has a lower cost), it is accepted.
    * If it is worse, it can still be accepted with a certain **probability**, which depends on a "temperature" `T` that gradually decreases. This feature allows the algorithm to escape local minima.

3.  **Visualizes the Process**: The script generates three key visualizations to understand the algorithm's behavior:
    * A **3D surface plot** of the Ackley Function.
    * A **real-time animation** showing the points explored by the algorithm across the function's surface, starting from the initial point.
    * A **convergence plot** that shows how the cost (the function's value) decreases over the iterations.



---

## Algorithm Parameters

The key parameters of the Simulated Annealing algorithm can be adjusted within the script:

* `T`: **Initial Temperature** (2000). A high temperature allows for a wider exploration of the solution space at the beginning.
* `T_min`: **Minimum Temperature** (1). The stopping criterion for the algorithm.
* `alpha`: **Cooling Factor** (0.99). Controls the rate at which the temperature decreases. A value close to 1 results in slower cooling and a more thorough search.
* `max_iter`: **Maximum number of iterations** (700). A limit on the number of steps to terminate the search.

---

## How to Run the Script

1.  Ensure you have **MATLAB** installed.
2.  Save the code in a file with a `.m` extension (e.g., `simulated_annealing_ackley.m`).
3.  Open MATLAB and navigate to the directory where you saved the file.
4.  Type the name of the file in the Command Window and press **Enter**:
    ```matlab
    SimulatedAnnealingAckley
    ```

---

## Expected Output

Upon running the script, you will observe the following:

1.  A first window will open showing the **3D surface** of the Ackley Function.
2.  A second window will open, displaying a **blue point (start)** followed by a series of **red points** that trace the algorithm's search path in real-time.
3.  After the execution finishes, the MATLAB console will print the **best solution found** (`x`, `y` coordinates) and its corresponding **cost**. Ideally, the values will be very close to `(0, 0)` and the cost will be close to `0`.
4.  Finally, a third figure will appear showing the **convergence graph**, which illustrates how the algorithm found progressively better solutions over time.

This set of visualizations provides a clear and educational demonstration of how Simulated Annealing explores a complex solution space to find a global optimum.
