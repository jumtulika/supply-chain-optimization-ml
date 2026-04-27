# supply-chain-optimization-ml

# AI-Driven Supply Chain Optimization under Demand Uncertainty

## Overview
This project develops a predictive–prescriptive analytics framework to optimize logistics planning under uncertain demand in a multi-echelon supply chain network.

The solution integrates machine learning with mathematical optimization to improve transportation cost efficiency and service performance.

## Business Problem
Logistics networks must make shipment and capacity decisions before actual demand is known. Poor decisions lead to:
- High transportation costs (over-allocation)
- Service failures (underestimation of demand)

This project addresses how to make **optimal decisions under demand uncertainty**.

## Approach

### 1. Predictive Modeling
- Demand uncertainty modeled using:
  - k-Nearest Neighbors (kNN)
  - Decision Trees
- Models capture local demand patterns and variability

### 2. Optimization Model
- Multi-commodity network flow model implemented in Pyomo
- Three-level logistics network:
  - Origin Centers → Distribution Centers → Demand Nodes
- Objective:
  - Minimize transportation cost + shortage penalties

### 3. Decision Frameworks Compared
- Expected Value (EV)
- Sample Average Approximation (SAA)
- Predict-Then-Optimize (PTO)
- Predictive–Prescriptive (PP)

## Key Results

| Method | Avg Cost | Avg Shortage |
|--------|--------|-------------|
| EV | 3686.82 | 35.0 |
| SAA | 3533.58 | 34.5 |
| PTO (Decision Tree) | 1402.95 | 13.0 |
| PTO (kNN) | 1451.15 | 13.42 |
| **PP (kNN)** | **282.84** | **2.67** |

 Predictive–Prescriptive models achieved **over 90% cost reduction** compared to baseline methods.

## Key Insights
- Integrating ML with optimization significantly improves decision quality  
- Ignoring uncertainty leads to poor performance  
- Local demand patterns (kNN) outperform global averages  
- Structural constraints (capacity, network design) limit performance  

## Business Impact
This framework demonstrates how AI can:
- Reduce logistics costs significantly  
- Improve service levels under uncertainty  
- Support real-world supply chain decision-making  

## Dataset
The project uses multiple datasets, including:
- Orders data  
- SKU details  
- Delivery and routing data  
- Distance matrix between logistics centers  

## Repository Structure
```text
supply-chain-optimization-ml/
│
├── data/
├── notebooks/
├── report/
├── README.md
└── requirements.txt
