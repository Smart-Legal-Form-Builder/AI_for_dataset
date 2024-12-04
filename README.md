Here's the translated version, maintaining the original format and structure:

---

## 0. References

https://github.com/generative-model/script_generation_kr

https://github.com/gyunggyung/KoGPT2-FineTuning

https://github.com/sohyeon98720/KoGPT2-finetuning

## 1. Prerequisite Environment Setup

### 1. Install **`Anaconda 3.12`** and Set Up **`Python 3.8`** Virtual Environment

- To set up the virtual environment, use **`Anaconda 3.12`** to create a Python virtual environment.
    - **Anaconda** [Download](https://www.anaconda.com/download/success)
- Since **`KoGPT-2`** developed by SKT is relatively outdated, **`Python 3.8`** is used for compatibility reasons.
    - Run the Anaconda prompt and enter the following commands:

        ```bash
        conda create -n py38-env python=3.8 -y
        conda activate py38-env
        ```
        

### 2. Install Libraries in the Virtual Environment

- Install all necessary libraries to execute the code.

    ```bash
    # Install PyTorch (with GPU support)
    conda install pytorch==1.5.1 torchvision torchaudio cudatoolkit=10.2 -c pytorch
    
    # Install MXNet
    pip install mxnet
    
    # Install other packages
    pip install tqdm gluonnlp==0.8.3 sentencepiece==0.1.6 transformers==2.1.1 tensorboardX easydict
    ```
    
- During the installation of **`MXNet 1.6.0`**, an error occurred due to the requirement of **`numpy 1.16.6`**. Since **`numpy 1.16.6`** is not compatible with **`Python 3.8`**, MXNet was installed using the latest version instead.
