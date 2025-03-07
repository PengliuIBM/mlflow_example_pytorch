# mlflow_example_pytorch

https://gitee.com/yichaoyyds/mlflow-ex-pytorch

# mlFlow PyTorch Examples

## 1 关于 MLFlow

[MLFlow](https://mlflow.org/docs/latest/index.html)是一个能够覆盖机器学习全流程（从数据准备到模型训练到最终部署）的新平台。它一共有四大模块（如下为官网的原文以及翻译）：

- MLflow Tracking：如何通过API的形式管理实验的参数、代码、结果，并且通过UI的形式做对比。
- MLflow Projects：以可重用、可复制的形式打包ML代码，以便与其他数据科学家共享或部署到生产环境（MLflow项目）。
- MLflow Models：管理和部署从各种ML库到各种模型服务和推理平台（MLflow模型）的模型。
- MLflow Model Registry：提供一个中央模型存储，以协同管理MLflow模型的整个生命周期，包括模型版本控制、阶段转换和注释（MLflow模型注册表）。

在这个系列的前半部分，我们对MLFlow做了详细的介绍，以及每一个模块的案例讲解，这里不再赘述。

## 2 关于如何在PyTorch中使用MLFlow

[`mlflow.pytorch`](https://www.mlflow.org/docs/latest/python_api/mlflow.pytorch.html)模块提供了一个用于记录和加载 PyTorch 模型的 API。

需要注意的是，MLFlow 无法直接和PyTorch一起使用，我们需要先装一下[pytorch_lightning](https://pytorch-lightning.readthedocs.io/en/latest/)，当我们调用 `pytorch_lightning.Trainer()` 的 `fit` 方法时会执行自动记录（`mlflow.pytorch.autolog`）。

## 3 关于代码的运行

参见每一个文件夹内的README文件。
