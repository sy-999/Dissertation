# Dissertation

# Autonomous Vehicle Routing Optimization using Q-Learning and FPGA Acceleration

This repository presents a research project on latency and performance optimization for autonomous vehicle (AV) routing. The experiments explore reinforcement learning-based dynamic routing, hardware acceleration using FPGA, and system communication across MEC nodes (Raspberry Pi, CPU, and PYNQ Z1 board). 

All experiments are based on real-world urban simulation using SUMO (Simulation of Urban Mobility) and are categorized into three parts.

##  Folder Structure

### `1_Qlearning_vs_Fixed_vs_Dijkstra`
- Comparison of routing strategies in SUMO:
  - Q-learning based dynamic routing
  - Fixed routing paths
  - Traditional Dijkstra algorithm
- Evaluation metrics:
  -  Average travel time
  -  Fuel consumption
  -  CO₂ emission

### `2_CPU_vs_FPGA`
- Performance comparison between CPU and FPGA execution of RL-based decision-making.
- Setup:
  - FPGA: PYNQ-Z1 board (Zynq-7000 SoC)
  - CPU: Intel Core i3 processor
- Metrics:
  - Latency (ms)


### `3_Communication_RaspberryPi_CPU_FPGA`
- Embedded system configuration for edge computing:
  - Raspberry Pi as edge coordinator
  - CPU node for traffic management
  - FPGA node for RL acceleration
- Communication protocols:
  - TCP socket (CPU ↔ Pi)
  - Secure Shell (Pi ↔ FPGA)

##  How to Run

Each folder contains its own `README.md` with instructions for running experiments. Please refer to them individually.

Basic Requirements:
- Python 3.8+
- SUMO 1.18+
- PYNQ SDK (for Zynq board)
- Raspberry Pi OS (Bullseye recommended)

##  Key Findings (Summary Table)

| Scenario    | Avg Travel Time ↓   | CO₂ Emission ↓          | Fuel Use ↓    | Latency ↓   |
|--------------|-------------------------|--------------------|---------------|--------------|
| Q-learning | ✅ Best                   | ✅                | ✅             |             |
| Fixed route | ✖ Worst              | ✖                   | ✖            | ✅             |
| SUMO(dijkstra) | ✅       	        | -                      | -               |           |
| CPU |- | - | - | ✖ Worst|
| FPGA |- | - | - |✅ Best|

##  License

This project is intended for academic research only. All code and content © Sooyeon Kim, 2024.
