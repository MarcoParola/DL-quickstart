## **Logging**

Logging is a crucial aspect of any deep learning project as it helps in monitoring the progress, tracking the performance metrics, debugging issues, and maintaining a record of experiments for future reference. In this section, we'll discuss the importance of logging and how to implement it effectively in your deep learning project.

# **Why Logging is Important**
**Tracking Experimentation**: Deep learning projects often involve numerous experiments with different hyperparameters, architectures, and datasets. Logging allows you to keep track of these experiments, including the configurations used and their outcomes, facilitating reproducibility and comparison.

**Monitoring Model Performance**: During training, it's essential to monitor various performance metrics such as loss, accuracy, and validation scores. Logging these metrics enables you to visualize the training progress, identify overfitting or underfitting, and make informed decisions for model improvement. As example, observing loss curves logged during a training it's possible to infer how to correct the learning rate for the next experiment

**Debugging and Troubleshooting**: When encountering errors or unexpected behaviors, logs serve as valuable debugging tools. They provide insights into the model's behavior, enabling you to pinpoint issues and refine your code effectively.

Two main alternatives for logging are Tensorboard and Wandb.

# **Tensorboard**:
TensorBoard, developed by TensorFlow, is a powerful visualization tool designed specifically for deep learning projects. It allows you to monitor various aspects of your model's training process, including:

**Scalar Metrics**: Track metrics such as loss, accuracy, learning rates, and custom metrics over time.

**Graph Visualization**: Visualize the computational graph of your model, aiding in understanding its architecture and flow of data.

**Histograms and Distributions**: Explore the distribution of weights, biases, and activations throughout the network layers.

# **How to use Tensorboard**
import in your project
```sh
from pytorch_lightning.loggers import TensorBoardLogger
```
instantiate the logger 
```sh
tensorboard_logger = TensorBoardLogger(log_path, name="name")
```

In order to visualize logs of an experiments is necessary to run a tensorboard server and to specify in the option "--logdir" the folder in which log data are saved: 
```sh
python -m tensorboard.main --logdir=log_path
```

open http://localhost:6006/ to visualize the page of Tensorboard running on the server just created

# **Weights & Biases (WandB)**:
Weights & Biases, often abbreviated as WandB, is a collaborative platform for machine learning experiments. It provides logging, visualization, and experiment tracking functionalities, enabling seamless collaboration and reproducibility across teams. Key features of WandB include:

**Experiment Tracking**: Log hyperparameters, metrics, and model artifacts, allowing for easy comparison and reproducibility of experiments.

**Visualization**: Visualize training metrics, model performance, and system resources in real-time dashboards.

**Artifact Management**: Store and version control model checkpoints, datasets, and other experiment artifacts for easy retrieval and sharing.

By integrating WandB into your training pipeline, you can leverage its collaborative features to streamline experimentation and share insights with your team.

To exploit wandb you have to create a new project on [Weights & Biases](https://wandb.ai/site).  
Log in 
```sh
wandb login 
```
and paste your API key when prompted.
