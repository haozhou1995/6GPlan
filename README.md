# 6GPlan

This repo includes the 6GPlan dataset, which is used for evaluating LLM's capabilities in handling complicated 6G network management problems.
It contains 110 complicated planning/management tasks distributed across 11 core 6G themes: Reconfigurable Intelligent Surfaces (RIS), Integrated Sensing and Communication (ISAC), mmWave and Terahertz (THz) Communications, Non-Terrestrial Networks (NTN), Cell-Free Massive MIMO, Artificial Intelligence (AI)-Driven Network Optimization, Semantic Communications, Open Radio Access Network (O-RAN), Quantum Communication for 6G Blockchain for Secure Wireless Networks,
6G-Enabled Digital Twin Network.

Each question is paired with a set of gold-standard technical keywords (around 5000 total) that serve as our reference for evaluation. The following figure shows the main procedures of creating the dataset:

<p align="center">
<img src=Asset/fig-data2.jpg width=60%  />
</p>

Firstly, we selected 11 topics regarding 6G networks, e.g., integrated sensing and communication, mmWave and Terahertz Communications, non-terrestrial networks, cell-free massive MIMO, etc. 
For each category, we asked an LLM to generate related questions, focusing on complex network management and optimization tasks. 

After that, we consider a multi-LLM question-answering approach: asking multiple LLMs to generate solutions for a given question, and then extracting related technical keywords from their replies.

Here we use these keywords to represent the key elements that should be covered in a high-quality solution. 
At the end, we will merge the keywords from these LLMs, and implement human verification and correction, guaranteeing the dataset quality. 

Here is a sample question and answer: 

```json
{
 "question0":{ "question": "How to dynamically optimize reconfigurable intelligent surfaces phase shifts in real-time under time-varying channel conditions?",
                 "Answer": "Reconfigurable intelligent surfaces (RIS), phase shift optimization, time-varying channels, Doppler spread, Channel State Information (CSI), statistical channel modeling, adaptive channel estimation, pilot sequences, compressed sensing, matrix completion, Time-Division Duplexing (TDD), Frequency-Division Duplexing (FDD), channel estimation algorithms, Kalman filtering, spectral efficiency, SNR maximization, data rate maximization, energy efficiency, weighted sum rate maximization, real-time optimization, non-convex optimization, online convex optimization, robust optimization, alternating optimization, gradient-based optimization, stochastic gradient descent, metaheuristic algorithms, reinforcement learning, model predictive control, low-complexity heuristic algorithms, hardware acceleration, control signal implementation, pre-calculated solutions, hardware calibration, feedback loops, latency constraints, mobility adaptation, edge computing, federated learning, parallel processing, fast-switching RIS, synchronization protocols, optimization objectives, FPGA acceleration, codebook-based solutions, dynamic parameter estimation.",
                 "Category": "reconfigurable intelligent surfaces"
    },

 "question2":{ "question": "How to design scalable RIS configuration protocols for massive IoT deployments with heterogeneous QoS requirements?",
                 "Answer": "Reconfigurable Intelligent Surfaces, RIS, Scalable Configuration Protocols, Heterogeneous QoS, Massive IoT, Deployment Scenario, Spatial Distribution, Traffic Patterns, Quality of Service, Latency, Throughput, Reliability, Energy Efficiency, System Model, Channel Model, Channel State Information, Reflection Characteristics, Scalability Challenges, Problem Decomposition, Centralized Configuration, Distributed Configuration, Dynamic Configuration, Resource Allocation, Resource Management, Joint Optimization, Decoupled Optimization, QoS-Aware, Signaling Overhead, Control Protocols, Performance Evaluation, Experimental Validation, Phase-shift Optimization, Deep Reinforcement Learning, Interference Mitigation, Non-orthogonal Multiple Access, Mixed-integer Nonlinear Programming, Federated Learning, Game Theory, Energy Harvesting, Digital Twin, Adversarial Testing, Lyapunov Optimization, Spectral Clustering, Service-level Agreements, SNR Targets, Gradient-based Algorithms, MAC Layer, Regret Analysis, Pareto-optimal Beamforming, Network Slicing, Clustering Algorithms",
                  "Category": "reconfigurable intelligent surfaces"
    }
  }
```
