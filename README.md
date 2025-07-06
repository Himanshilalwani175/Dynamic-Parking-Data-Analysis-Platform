# Dynamic-Parking-Data-Analysis-Platform
# 🚗 Dynamic Pricing for Urban Parking Lots  
**Capstone Project — Summer Analytics 2025 × Pathway**

---

## 📌 Project Overview

This project proposes a dynamic pricing strategy for urban parking lots using real-time data and predictive modeling.  
The system adapts parking prices based on lot occupancy, traffic conditions, special events, and nearby lot competition — optimizing both revenue and space utilization.

It integrates:
- Predictive Models (3-tiered)
- Real-time data streaming with Pathway
- Live interactive dashboard using Bokeh

---

## 🧰 Tech Stack

| Tool | Purpose |
|------|---------|
| **Python (Pandas, NumPy)** | Data processing and modeling |
| **Pathway** | Real-time data streaming and computation |
| **Bokeh** | Live dashboard visualization |
| **Google Colab / VS Code** | Development environment |
| **GitHub** | Version control and documentation |
| **Replit (optional)** | Online hosting for Bokeh dashboard |

---

## 🏗️ System Architecture

graph LR

    A[Raw Data (CSV)] --> B[Preprocessing in Colab]
    B --> C[Model 1: Linear Occupancy Pricing]
    B --> D[Model 2: Demand-Based Pricing]
    B --> E[Model 3: Competitive Pricing]

    E --> F[Streaming File: parking_stream.csv]
    F --> G[Real-Time Pricing via Pathway]
    G --> H[Output: pathway_output.csv]
    H --> I[Live Bokeh Dashboard (bokeh_dashboard.py)]

    
## Project Architecture & Workflow
1. Data Preprocessing
Merges occupancy, queue length, special day, and location data
Outputs parking_stream.csv for real-time use

2. Modeling
Model 1: Linear pricing based on past occupancy trends
Model 2: Uses a demand function including traffic, queue, and vehicle type
Model 3: Adds spatial logic — adjusts price based on nearby lot pricing (Haversine)

3. Real-Time Streaming with Pathway
Continuously consumes parking_stream.csv
Computes prices per lot in real time
Writes pathway_output.csv (used in visualization)

4. Live Visualization (Bokeh)
Auto-refreshing dashboard showing per-lot pricing over time
Supports dropdown filtering by lot_id


# Key Files
| File                       | Description                                 |
| -------------------------- | ------------------------------------------- |
| `bokeh_dashboard.py`       | Bokeh server for live pricing visualization |
| `pathway_model.py`         | Pathway model with Model 3 logic            |
| `parking_stream.csv`       | Real-time data for streaming                |
| `final_pricing_output.csv` | Combined pricing output                     |
| `README.md`                | Project documentation                       |

# Final Outcomes

![bokeh2](https://github.com/user-attachments/assets/707509db-1831-4071-be5a-e39c81ad7f91)
This is interface of dashboard, after uploading dataset csv we can see different dashboards

![bokeh3](https://github.com/user-attachments/assets/5850dd3a-7c69-4d7e-b16e-678d8fe2c2d5)
Navigation panel allows us to choose particular analysis (model) and understand the role.

![bokeh 9](https://github.com/user-attachments/assets/5d84228a-111e-4ff1-ab83-b4489ceb7686)
This is dashboard for occupancy distribution and Queue lenght distribution

![bokeh4](https://github.com/user-attachments/assets/1af1909f-2087-4e49-bcb5-acce82ebf154)

![bokeh 5](https://github.com/user-attachments/assets/4a7a6620-2f67-47f1-895c-1aa0511c5317)

![bokeh 6](https://github.com/user-attachments/assets/647bd18f-bdf5-43cf-920d-2cee2635fb51)

![bokeh 7](https://github.com/user-attachments/assets/4cccf68b-d6c8-4e6a-bb78-b4978838490d)

![bokeh 8](https://github.com/user-attachments/assets/d1b6c321-d1db-4981-9c8f-cfcf76702e0d)


👤 Author
Himanshi Lalwani
