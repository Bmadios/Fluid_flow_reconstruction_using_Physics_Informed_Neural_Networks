# Fluid flow fields reconstruction using Physics Informed Neural Networks (PINNs)

Physics-Informed Neural Networks (PINNs) represent a novel approach to deep learning, marrying the predictive capabilities of artificial neural networks with the intrinsic structure of physical models. By utilizing a set of governing differential equations to encapsulate the physical behavior, PINNs weave these rules directly into the neural network's architecture. This enables PINNs to employ observed data for solving intricate tasks such as inverse inference or functional synthesis.

In contrast to conventional deep learning techniques, PINNs provide more stable and reliable results by explicitly incorporating physical constraints into the model's architecture. PINNs demonstrate a unique advantage in not requiring extensive training data; they leverage the generally known structure of the system under investigation. Furthermore, their ability to integrate explicit physical knowledge provides the potential not only to build a superior predictive model, but also to unveil previously undiscovered implicit mathematical properties of the system.

The current project revolves around developing a Physics-Informed Neural Network model to reconstruct fluid flow fields around a cylinder using limited data. The project's two primary objectives are as follows:

1. Acquiring data through numerical simulation to establish a reference solution to the problem.

2. Combining the understanding of physics with the learning prowess of neural networks to formulate a predictive model, which will then be evaluated using the acquired data.
   
The resulting model should be capable of predicting fluid flow attributes (such as velocity and pressure) based on the initial conditions and system parameters. This is expected to be achieved with minimal training data gathered through numerical simulation (CFD with OpenFOAM). The project aims to demonstrate the efficacy of PINNs as a tool for fluid dynamics studies with limited training data, opening doors to a multitude of practical applications.

## Collocation Points

![alt text](https://github.com/Bmadios/Fluid_flow_reconstruction_using_Physics_Informed_Neural_Networks/blob/main/project_report/Points_colloc.png "Collocation points sampling")

## PINN model architecture
![alt text](https://github.com/Bmadios/Fluid_flow_reconstruction_using_Physics_Informed_Neural_Networks/blob/main/project_report/pinn_architecture.png "PINN Architecture")


## Usage

To run `main.py` from `Navier_Stokes_2d_flow_past_cylinder` folder, use the following command:

```bash
python main.py --data_path /path/to/data --max_iter 1000


 You can run the script with a pretrained model:
 
 python main.py --data_path "your/data/path" --pretrained_model "path/to/pretrained/model.pth"

Or you can train a model from scratch:

python main.py --data_path "your/data/path"

