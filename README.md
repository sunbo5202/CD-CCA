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
        CD-CCA framework. The visual encoder first extracts latent representations from observations, followed by three fully connected layers that produce feature projections $\mathit{z}$, $\mathit{z}_{1}$, and $\mathit{z}_{2}$. The shared embedding $\mathit{z}$ serves as the policy query, while $\mathit{z}_{1}$ and $\mathit{z}_{2}$ act as critic-specific keys in the cross-attention fusion module. Two critics—enhanced by CBP and EWC, respectively—estimate $Q_{1}$ and $Q_{2}$. The cross-attention mechanism adaptively fuses the two $Q$-values into a unified value $Q$, which guides actor training and exploration. The policy decoder outputs the action to interact with the environment.
    </td>
    <td align="center" width="10%"><img src="https://github.com/sunbo5202/CD-CCA/figframework.png" 
        alt="motivation"/>
    </td>
</tr>
</table>
</div>
