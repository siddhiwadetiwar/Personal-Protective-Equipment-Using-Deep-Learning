# **Personal Protective Equipment Using Deep Learning**

This Repository consist Personal Protective Equipment (PPE) detection systems using Python involves developing algorithms to identify and ensure the proper usage of safety gear in various environments, prioritizing workplace safety and accident prevention.

# Table Of Contents 📜

- Introduction
- Features
- Installation
- File Hierarchy
- Results
- License

## Introduction 🧑‍🔧

Multiple accidents have occurred at construction sites because workers didn't have proper safety gear. This project's goal was to identify personal protective equipment (PPE) worn by workers. This information could then be utilized for future safety monitoring, including tracking and activating alarms when necessary.

The dataset consists of 2801 image samples with labels in YoloV8 format. These images are split into `train: 2605`, `valid: 114` and `test: 82` sets. Each folder consists of `images` and `labels` folders.

There are 10 classes to detect from the dataset:

**'Hardhat', 'Mask', 'NO-Hardhat', 'NO-Mask', 'NO-Safety Vest', 'Person', 'Safety Cone', 'Safety Vest', 'machinery', 'vehicle'**

## Features 🤖

1. **Object Detection:** Utilizes computer vision to identify and locate specific PPE items within images or video feeds.
2. **Real-time Monitoring:** Offers continuous surveillance to ensure ongoing adherence to safety protocols.
3. **Scalability:** Adaptable for various industries, from construction sites to healthcare, enhancing safety across different sectors.
4.  **Customization Options:** Allows flexibility in tailoring the system to detect specific types of PPE or adapt to diverse working conditions and environments.

## Setup 🖱️

### **1. Install Python:**

- Ensure Python is installed on your system. You can download it from the official [Python website](https://www.python.org/downloads/).

### **2. Install Jupyter Notebook:**

- Open your terminal or command prompt and install Jupyter Notebook using pip (Python's package manager) :
    
    ```
    
    pip install jupyterlab
    
    ```
    

### **3. Install Required Libraries:**

- Install essential libraries such as OpenCV, TensorFlow, or PyTorch for computer vision tasks. For instance:
    
    ```
    
    pip install opencv-python
    pip install tensorflow
    pip install ultralytics
    
    ```
    

### **4. Launch Jupyter Notebook:**

- Open your terminal or command prompt and navigate to  project directory.
- Type **`jupyter notebook`** and press Enter. This will open Jupyter Notebook in your default web browser.

### **5.  Open a Notebook:**

- open **for_train.ipynb** notebook for training of model.
- open **yolov8-safety-helmet-detection.ipynb** for running the model and outputs.

## File Hierarchy 📝

1. `data` folder consists of the yaml file required for training. It also contains 3 folders `train`, `valid` and `test`. Each of these folders have 2 subfolders `images` (with .jpg files) and `labels` (with .txt annotations).
2. `results` folder consists of the prediction results of the model, confusion matrix plot, visualizations of the train and valid batches and PR curves.
3. `models` folder consists of 2 models, `yolov8n.pt` which is the pre-trained model on COCO128.yaml and `best.pt` which is the custom trained yolov8n model on our dataset.
4. `source_files` folder consists of videos and images for evaluation of our custom trained model.
5. `output` folder consists of output produced by our custom object detection model after 100 epochs of training.

## Code ⌨️

```
├───.ipynb_checkpoints
├───assets
├───data
├───├──data.yaml
├───├──ppe_data.yaml
│   ├───test
│   │   ├───images
│   │   └───labels
│   ├───train
│   │   ├───images
│   │   └───labels
│   └───valid
│       ├───images
│       └───labels
├───models
├───output
│   └───output_yolov8
├───results
└───source

```

## Results 🎯

The training of YoloV8n model was done for 100 epochs and was completed in 4.719 hours. After training, we get the following results:

## License 🖼️

This project is licensed under the **[MIT License](https://chat.openai.com/c/LICENSE)**. Feel free to modify, distribute, or use the codebase according to the terms of the license.

👉 **Have a question?** Click the `?` at the bottom right for more guides, or to send us a message.
