# CD-CCA
This repository contains the official code from "Resolving the Stability-Plasticity Dilemma in Reinforcement Learning via Complementary Continual Critics".
- [2026/2/20]: CD-CCA is accepted by CVPR 2026.
## 📷 Abstract
This paper proposes the Continual Dual-Critic with Cross-Attention (CD-CCA) framework for visual reinforcement learning to address the plasticity-stability conflict. Our method introduces continual learning techniques into the visual RL architecture, constructing two complementary critics using Continual Backpropagation (CBP) and Elastic Weight Consolidation (EWC) -- one for maintaining representational plasticity for rapid environmental adaptation, and the other for preserving knowledge stability to prevent catastrophic forgetting. Furthermore, we design a cross-attention based fusion mechanism that balances the value estimates from the dual critics according to observation characteristics. Experimental results on DeepMind Control and CARLA benchmarks show that CD-CCA effective mitigates issues of representation drift and policy degradation. Compared to existing visual RL methods, our approach exhibits enhanced robustness and adaptability in non-stationary environments and long-horizon decision-making tasks, providing a new architectural paradigm for the advancement of continual reinforcement learning.

- **The overview of TransACO framework:**
<div align="center">
<table>
<tr>
    <td align="left" width="10%">
        Taking TSP as an example, the method calculates the distance matrix and node coordinates based on the problem instance. The results are then input to the Transformer, which generates the HM and PM. ACO constructs the initial solution and optimizes it using optional local search techniques. Finally, the method samples from the obtained solution and calculates the reward as feedback.
        <br/>   <br/>
        In modified Transformer, we depart from the standard query–key–value formulation and adopt a query–key-only variant that is tailored to constructing the PM and HM. 
For each city $i$ in a TSP instance, the Transformer encoder outputs a shared query vector $q_i \in \mathbb{R}^d$ and two type-specific key vectors $k^{\text{p}}_i, k^{\text{h}}_i \in \mathbb{R}^d$ after linear projection and a ReLU nonlinearity.
        <br/>   <br/>
        In ACO, we generate the transition probability by leveraging the cooperation between the HM and PM. After constructing a solution, we further apply a candidate-solution perturbation mechanism to perform local search. 
    </td>
    <td align="center" width="10%"><img src="https://github.com/sunbo5202/TransACO/blob/main/Fig/Framework.png" 
        alt="motivation"/>
    </td>
</tr>
</table>
</div>
