# 🔋 Electro-Insight: Battery Life Prediction Dashboard

**Electro-Insight** is a battery intelligence platform designed to visualize and predict the remaining useful life (RUL) of Lithium-Ion batteries. It uses physics-based feature extraction—specifically the variance in discharge voltage curves ($\Delta Q(V)$)—to identify early signs of degradation before significant capacity fade occurs.

## 🚀 Features
* **Physics-Based Analysis:** Visualizes the "Delta V" variance ($V_{100} - V_{10}$) to fingerprint degradation.
* **Interactive Dashboard:** Built with Streamlit for real-time data exploration.
* **Synthetic Data Engine:** Includes a generator that simulates Severson/MIT-style battery datasets on the fly.

## 🛠️ Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/Electro-Insight.git](https://github.com/YOUR_USERNAME/Electro-Insight.git)
    cd Electro-Insight
    ```

2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the application:**
    ```bash
    streamlit run app.py
    ```
    *Note: On the first run, the app will automatically generate the synthetic dataset.*

## 📂 Project Structure
* `app.py`: Main Streamlit dashboard application.
* `data_generator.py`: Script to generate synthetic battery telemetry (Voltage vs. Capacity).
* `requirements.txt`: Python dependencies.

## 🧠 The Science
The core predictive feature is the variance of the discharge voltage difference between cycle 10 and cycle 100:
$$ \Delta V(Q) = V_{100}(Q) - V_{10}(Q) $$
High variance in this feature correlates strongly with lower cycle life, allowing for early classification of "Good" vs. "Bad" cells.