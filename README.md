# Universal Approximation Constraints of Narrow ResNets: The Tunnel Effect

This code base provides the numerical experiments discussed in the paper 

It contains the training setup for various narrow/non-augmented ResNets including neural ODEs and MLPs.

## One-Dimensional ResNets
In the one-dimensional setting, we train models to approximate x^2 and analyze the present embedding restrictions

![running1](https://github.com/user-attachments/assets/77f83bcb-75fb-4a28-b889-64f9aa567a1f)

## Two-Dimensional ResNets

<img width="300" alt="2d_node_regime_pred" src="https://github.com/user-attachments/assets/2500cd81-a480-428a-ae84-3888badf0f87" />
<img width="300" alt="2d_node_regime_ls" src="https://github.com/user-attachments/assets/55c710d9-6398-4560-a6e7-fc60fb48124b" />

In the neural ODE regime, the narrow ResNet cannot express critical points. This topological constraint creates a "tunnel" in the prediction level sets, leading to unavoidable misclassifications on the 2D circle dataset. <p>

<img width="300" alt="2d_mlp_regime_pred" src="https://github.com/user-attachments/assets/0a0620c8-7471-498c-b76e-01ace7aedc30" />
<img width="300" alt="2d_mlp_regime6_ls" src="https://github.com/user-attachments/assets/fd44f754-9785-4d05-a663-99a368c14d7a" />

Similarly, in the standard MLP regime, the skip connection's influence vanishes and the architecture once again loses the ability to embed critical points. 
The resulting input-output map generates the exact same "tunnel effect", failing to capture the enclosed topology of the data.<p>

<img width="300"  alt="ff6_res_pred" src="https://github.com/user-attachments/assets/acb0d715-68c5-46a2-8ce6-4d58310770db" />
<img width="300"  alt="ff6_res_ls" src="https://github.com/user-attachments/assets/d5e0c553-8409-489d-930d-415959a6098b" />

Standard ResNets are able to embed critical points and as a result express the desired topology of the data accurately.
