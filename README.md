# 🎲 Monolith Analysis App with OpenTelemetry

## 📌 Overview

This is a Flask-based web application that simulates a dice roll and demonstrates observability using **OpenTelemetry**. The application exports **tracing and metrics data** to **SigNoz** via OTLP over HTTP for monitoring and debugging.

---

## 🚀 Features

- 🎯 **Dice Roll Simulation** via `/` or `/rolldice` endpoint
- 📈 **OpenTelemetry Tracing & Metrics** integration
- ⚠️ **Error Logging** for exception simulation
- 📡 **SigNoz Integration** using OTLP HTTP exporter

---

## 🛠️ Prerequisites

- Python **3.12+**
- [SigNoz](https://signoz.io) running locally (default OTLP endpoint: `http://localhost:4318`)
- Python packages:
  - `flask`
  - `opentelemetry-api`
  - `opentelemetry-sdk`
  - `opentelemetry-exporter-otlp`

---

## 📦 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Durlabh8972/Monitoring-and-Logging-lnclass3.git
   cd Monitoring-and-Logging-lnclass3
Install dependencies:

bash
Copy
Edit
pip install flask opentelemetry-api opentelemetry-sdk opentelemetry-exporter-otlp
Start SigNoz:

Use Docker or follow the SigNoz installation guide

Run the application:

bash
Copy
Edit
python app.py
🌐 Usage
Visit: http://localhost:3000/

Optional: Add query parameter ?player=YourName to simulate a player roll:

ruby
Copy
Edit
http://localhost:3000/?player=Durlabh
Check SigNoz UI to view traces and metrics in real-time.

🧪 Testing Exceptions (Optional)
To simulate and test error tracking:

Modify the roll() function in app.py:

python
Copy
Edit
def roll():
    raise Exception("Simulated dice roll failure!")
Access the endpoint to trigger an exception.

Check SigNoz for the captured error trace.
