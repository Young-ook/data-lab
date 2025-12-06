# ML (Machine Learning) Lab

## Table of Contents
- [Apache Airflow](#apache-airflow)
- [Jupyter](#jupyter)
- [MLflow](#mlflow)
- [LLM (Large Language Model)](#llm)
- [Other Examples](#other-examples)

## Apache Airflow
Apache Airflow is an open-source workflow management platform for data engineering and MLOps pipelines. To learn more details of machine learning lifecycle management with Airflow, follow the [airflow.md](airflow/airflow.md).

## Jupyter
Jupyter is the web-based notebook application for interactive computing, computational documents sharing. It offers a simple, streamlined, document-centric experience. Open the [jupyter.md](jupyter/jupyter.md) and follow the instructions.

## MLflow
MLflow is an open-source developer platform to build AI/ML applications with end-to-end experiment tracking, observability, and evaluations, all in one integrated platform. To learn about MLflow, open the [mlflow.md](mlflow/mlflow.md) and follow the instructions.

For more MLflow examples and advanced guide, please checkou out [the official MLflow repository](https://github.com/mlflow/mlflow). Clone the mlflow into the *data-lab/labs/extra* directory and run examples by following the intructions of each jupyter notebooks under the example directory. You should make a *extra* directory where to clone the mlflow examples if you don't have it on your workspace.

```bash
git clone https://github.com/mlflow/mlflow.git
```

## LLM
### Simple LLM
Open the `simple-llm-student-guide.ipynb` notebook in *llm* directory and follow the instructions.

## Other Examples
### PyTorch for Deep Learning Bootcamp
Clone the repository into the *data-lab/labs/extra* directory. If you have the *extra* directory you can create before you clone the repository using `mkdir -p extra`. To run hands-on labs, open each notebooks and follow the tutorials for pytorch deep learning course. For more details, please check out the [PyTorch for Deep Learning Bootcamp](https://github.com/mrdbourke/pytorch-deep-learning).

> [!NOTE]
> Make sure to clone the repository via SSH, not HTTP. Due to the large file size, you might see a gRPC error when you try to download the project over HTTP.
> ```
> git clone git@github.com:mrdbourke/pytorch-deep-learning.git
> ```

> [!NOTE]
> This example requires some packages such as *pytorch*. Please make sure to install these packages using PyPI or conda if you don't have before you run examples. For more details, please refer to the [PyTorch website](https://pytorch.org).
> ```
> pip3 install torch torchvision torchaudio
> ```

![pytorch-bootcamp](../images/pytorch-bootcamp.png)

### Randy Olson's Data Analysis and Machine Learning projects
This is a good project for learning data analysis and machine learning with hand-on. To run examples, clone the repository under the *data-lab/labs/extra* directory. Please create *extra* directory if you don't have. Open and follow the instructions of each notebooks. For more details, please check out the [Data Analysis and Machine Learning Projects](https://github.com/rhiever/Data-Analysis-and-Machine-Learning-Projects).

```
git clone https://github.com/rhiever/Data-Analysis-and-Machine-Learning-Projects.git
```

> [!NOTE]
> This example requires some packages such as *numpy, pandas, scikit-learn, matplotlib, seaborn, watermark*. Please make sure to install these packages using pip or conda if you don't have before you run examples.
> ```
> pip install numpy pandas scikit-learn matplotlib seaborn watermark
> ```

![ml-randy](../images/ml-randy.png)

# Additional Resources
- [Linux Foundation AI/Data Projects](https://lfaidata.foundation/projects/)
- [PyTorch Tutorials](https://pytorch.org/tutorials/)
- [Tensorflow Tutorials](https://www.tensorflow.org/tutorials)

