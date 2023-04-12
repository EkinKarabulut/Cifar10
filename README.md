# Run:ai & WandB Demo - Cifar10 Classification

Kubernetes is a widely used open-source orchestraction system for automating deployment, scaling, and management of containerized applications. Due to the high adoption rate of Kubernetes, data scientists are getting more exposed to it. However, in the development stage, the complexity and unknowns of this system leads to unproductivity and neglecting their data science tasks of data science teams. 

In this Demo, we will demonstrate how data scientists can accelarate their workflows and experiment tracking using WandB integration of Run:ai. This integration offers them not to be a specialist in infrastructure while leveraging all capabilities (and many more) of Kubernetes.

## Setup without Run:ai

We assume that there is an existing Kubernetes cluster that we have access to. Our next steps without Run:ai would look like following;

* Create a Dockerfile that includes: 
  * Wandb installation
  * Training script (Copy path)
  * Other installations (e.g. VSCode, Jupyter, Pytorch etc.)
  * Networking details of the tools (e.g. exposed port for Jupyter Lab to run)
* Build the image
* Push the image to a private Docker repository
* Configure the deployment yaml file of Kubernetes with WandB secret
  * Container configurations for this deployment (including the image that is created)
  * Resource specifics for the container (GPU, CPU memory)
  * WandB API key as environment variable
* Deploy the secret
* Run the deployment with your container that you created.

For more information and details, please check out [this documentation](https://wandb.ai/site/articles/model-explorations-and-hyperparameter-search-with-w-b-and-kubernetes)

## Setup with Run:ai

Here we assume that there is an existing Kubernetes cluster and Run:ai is installed on top of it. 

* We first login to our account on the UI

* Then we head to workspaces




