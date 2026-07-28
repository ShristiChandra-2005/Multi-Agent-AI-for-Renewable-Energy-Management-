# 🌍 Multi-Agent AI for Renewable Energy Management

An end-to-end **Multi-Agent Artificial Intelligence Framework** for intelligent renewable energy management using **Machine Learning, FastAPI, and Streamlit**.

This project combines multiple AI agents, each responsible for solving a specific energy-related problem, and integrates them through a Coordinator Agent and a Decision Support Layer to provide intelligent recommendations for sustainable energy management.

---

# 🚀 Project Overview

Renewable energy systems involve multiple interconnected tasks such as:

- Renewable energy prediction
- Electricity demand forecasting
- Grid stability monitoring
- Carbon emission estimation

Instead of building one large AI model, this project follows a **Multi-Agent Architecture**, where each AI agent specializes in one task.

The Coordinator Agent collects predictions from all agents, evaluates the overall system condition, and sends the results to the Decision Support Layer, which generates intelligent recommendations.

Finally, a Streamlit dashboard presents the complete system to the user.

---

# 🏗 System Architecture

```
                User
                  │
                  ▼
        Streamlit Dashboard
                  │
                  ▼
         Coordinator Agent
                  │
     ┌────────────┼────────────┐
     ▼            ▼            ▼
 Renewable   Energy Demand   Grid Stability
   Agent         Agent          Agent
                  │
                  ▼
        Emission Monitoring Agent
                  │
                  ▼
       Decision Support Layer
                  │
                  ▼
      Final Recommendation
```

---

# 🤖 AI Agents

## 1️⃣ Renewable Generation Agent

Predicts renewable energy generation using weather and environmental parameters.

### Inputs

- Solar Radiation
- Temperature
- Wind Speed
- Humidity

### Output

- Predicted Renewable Energy Generation

---

## 2️⃣ Energy Demand Agent

Predicts future electricity demand.

### Inputs

- Historical energy usage
- Weather
- Temperature

### Output

- Future Energy Demand

---

## 3️⃣ Grid Stability Agent

Predicts the stability of the electrical grid.

### Output

- Stable
- Moderate Risk
- High Risk

---

## 4️⃣ Emission Monitoring Agent

Predicts expected CO₂ emissions.

### Output

- Estimated Carbon Emissions

---

# 🧠 Coordinator Agent

The Coordinator Agent acts as the **brain of the system**.

It does **not perform machine learning**.

Instead, it:

- Calls every AI Agent API
- Collects predictions
- Validates responses
- Computes system health
- Sends all outputs to the Decision Support Layer

---

# ⚖ Decision Support Layer

This layer contains **business rules**, not machine learning.

Example rules:

- Renewable > Demand → Charge Battery
- Renewable < Demand → Discharge Battery
- High Grid Risk → Grid Alert
- High CO₂ → Reduce Fossil Fuel Usage

Finally, it generates the overall recommendation.

Example:

```
Recommendation:
Increase Renewable Generation

Battery:
Charge

Grid Status:
Stable

Carbon Policy:
Reduce Fossil Fuel Usage
```

---

# 📊 Streamlit Dashboard

The dashboard provides an interactive interface for users.

It displays:

- Renewable Generation
- Energy Demand
- Grid Stability
- Carbon Emissions
- System Health
- Final Recommendation
- Performance Metrics

---

# ⚙ Technology Stack

| Component | Technology |
|------------|------------|
| Programming Language | Python |
| Data Analysis | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-Learn, XGBoost, LightGBM |
| Model Storage | Joblib |
| Backend APIs | FastAPI |
| Dashboard | Streamlit |
| Development | Jupyter Notebook, VS Code |

---

# 📂 Project Structure

```
Multi-Agent-AI-for-Renewable-Energy-Management/

│── datasets/
│── reports/
│── outputs/
│── images/
│── shared/

│── 01_RENEWABLE_GENERATION_AGENT/
│── 02_ENERGY_DEMAND_AGENT/
│── 03_GRID_STABILITY_AGENT/
│── 04_EMISSION_MONITORING_AGENT/
│── 05_COORDINATOR_AGENT/
│── 06_DECISION_SUPPORT_LAYER/
│── 07_STREAMLIT_DASHBOARD/

│── README.md
│── requirements.txt
│── LICENSE
```

---

# 🔄 Project Workflow

### Phase 1

✔ Data Collection

✔ Data Cleaning

✔ Feature Engineering

✔ Model Training

✔ Hyperparameter Tuning

✔ Model Evaluation

✔ Save Best Model

---

### Phase 2

Develop FastAPI services for each trained model.

Each model becomes an independent AI service.

---

### Phase 3

Develop the Coordinator Agent.

The Coordinator communicates with every AI Agent.

---

### Phase 4

Implement the Decision Support Layer using rule-based logic.

---

### Phase 5

Build the Streamlit Dashboard.

The dashboard communicates only with the Coordinator Agent.

---

# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Multi-Agent-AI-for-Renewable-Energy-Management.git
```

Move into the project

```bash
cd Multi-Agent-AI-for-Renewable-Energy-Management
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# ▶ Running the Project

### Step 1

Run the Renewable Agent API

```bash
uvicorn renewable_api:app --reload
```

Repeat for all remaining agents.

---

### Step 2

Run the Coordinator API

```bash
uvicorn coordinator_api:app --reload
```

---

### Step 3

Run Streamlit

```bash
streamlit run app.py
```

---

# 📈 Future Improvements

- Deep Learning Models
- Reinforcement Learning for Energy Optimization
- Real-time IoT Integration
- Weather API Integration
- Docker Deployment
- Azure / AWS Deployment
- Kubernetes Microservices
- Explainable AI (XAI)

---

# 🎯 Key Features

✔ Multi-Agent AI Architecture

✔ Modular Design

✔ Machine Learning Prediction Models

✔ FastAPI Microservices

✔ Rule-Based Decision Support

✔ Interactive Streamlit Dashboard

✔ Easy Scalability

✔ Production-Ready Architecture

---

# 👩‍💻 Author

**Shristi Chandra**

B.Tech – Computer Science & Engineering (Artificial Intelligence)

Indira Gandhi Delhi Technical University for Women (IGDTUW)

---

# 📜 License

This project is licensed under the MIT License.
