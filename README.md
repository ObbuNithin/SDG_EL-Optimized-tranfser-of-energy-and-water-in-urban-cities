# CityResource AI

CityResource AI is an intelligent, multi-objective framework for the resilient optimization of urban energy and water resources. It leverages a hybrid of AI and mathematical programming to create a robust decision support system for smart cities.

---

## 📜 Description

[cite_start]Modern cities face increasing stress on their critical energy and water systems due to rapid urban growth, climate change, and unexpected disruptions[cite: 389, 390]. [cite_start]Most existing resource management solutions operate in isolation and are reactive rather than predictive[cite: 407, 408].

[cite_start]**CityResource AI** addresses this challenge by providing an integrated, AI-driven platform that intelligently allocates both energy and water[cite: 391]. [cite_start]The system uses a combination of **Reinforcement Learning (RL)**, **Machine Learning (ML)** forecasting, and **Linear/Nonlinear Programming (LP/NLP)** to adapt to real-time conditions, predict future demand, and optimize resource distribution for sustainability and resilience[cite: 392]. [cite_start]It also includes a full-stack simulation platform to model and visualize resource dynamics in a smart city environment[cite: 398].

---

## ✨ Core Features

The framework is built around five key optimization modules and a full-stack simulation interface.

* [cite_start]**⚡ RL-Based Energy Scheduling**: A Reinforcement Learning agent dynamically schedules energy storage (charging/discharging) and load shedding to minimize unmet demand, learning adaptive strategies for handling energy shortfalls[cite: 393, 418, 419, 420].
* [cite_start]**Forecasting-Driven Energy Allocation**: Employs **XGBoost** and **LightGBM** models to forecast energy demand and solar generation, feeding these predictions into a Linear Programming model to minimize costs and preemptively allocate resources[cite: 394, 421, 422].
* [cite_start]**Disruption-Aware Energy Optimization**: Uses **Random Forest** and **Gradient Boosting** models to predict the likelihood and severity of grid outages or solar dips, allowing the system to adjust energy allocation in real-time to enhance resilience[cite: 395, 424, 425].
* [cite_start]**💧 Hybrid Water Allocation Engine**: Utilizes both Linear and Nonlinear Programming to perform optimal water allocation across municipal, agricultural, and industrial sectors while respecting source constraints and sectoral priorities[cite: 396, 432].
* [cite_start]**Sustainable Groundwater Management**: An optimization module that determines the ideal daily groundwater extraction volume, balancing the immediate need for supply with the long-term sustainability of the aquifer, even factoring in the energy cost of pumping[cite: 397, 440, 441].
* **🏙️ Full-Stack City Simulation**: A complete simulation platform with a **Python (Flask)** backend and a **React.js** frontend. [cite_start]It simulates city demographics, automatically calculates water demand, and displays results on interactive dashboards[cite: 398, 399, 444].

---

## 🏗️ System Architecture

[cite_start]CityResource AI is designed as a modular, full-stack platform that integrates advanced optimization with real-time simulation and visualization[cite: 512].

1.  [cite_start]**Data Layer**: Consumes real-world time-series data for energy and water, sourced from platforms like NITI Aayog and the Central Ground Water Board (CGWB)[cite: 489, 490].
2.  [cite_start]**Backend Engine**: Implemented in **Python** using **Flask**, the backend handles all data processing, manages the **SQLite** database, and runs the core optimization and machine learning models[cite: 445, 515].
3.  [cite_start]**Frontend Interface**: Developed using **React.js**, the user interface provides interactive dashboards to visualize building-wise and city-wide water demand, allocation trends, and optimization results[cite: 446, 516].


---

## 🛠️ Tech Stack

* **Backend**: Python, Flask
* **Frontend**: React.js
* **Database**: SQLite
* **Machine Learning / RL**: scikit-learn (Random Forest, Gradient Boosting), XGBoost, LightGBM
* **Optimization**: SciPy (for LP/NLP solving)
* **Data Handling**: pandas, NumPy

---

## 📖 Usage & Simulation Flow

The system is designed as a decision support and simulation tool. The typical workflow is automated:

1.  [cite_start]**Initialization**: A city layout is initialized in the database, with a randomized number of buildings, houses, and residents to ensure variability[cite: 789, 790, 791].
2.  **Demand Calculation**: Water and energy demand are calculated automatically based on the simulated population and historical patterns. [cite_start]For example, daily water requirements are calculated at 175 liters per person[cite: 793, 795, 819].
3.  **Optimization Run**: The backend runs the suite of energy and water optimization modules, which make decisions on resource allocation, storage, and extraction based on the current state and forecasts.
4.  **Visualization**: The results are sent to the React frontend via REST APIs. [cite_start]Users can then explore the interactive dashboards to see city-wide demand, per-building allocations, unmet demand analysis, and other key performance metrics[cite: 815, 817].
