
# Multi-Aperture Transformers for 3D (MAT3D) Segmentation of Clinical and Microscopic Images

🚀 **Official PyTorch Implementation**  


---

## 📜 Overview

MAT3D uses Multi-Aperture Transformers for accurate 3D segmentation in clinical and microscopic imaging

<div align="center" style="display: flex; flex-direction: row; justify-content: center; align-items: center; gap: 20px;">
  <div>
    <a href="gif/10a_day2_c.gif">
      <img src="gif/10a_day2_c.gif" alt="Video Preview 1" width="150px" />
    </a>
    <p style="text-align: center;">MCF10A Day 2</p>
  </div>
  <div>
    <a href="gif/10a_day5_c.gif">
      <img src="gif/10a_day5_c.gif" alt="Video Preview 2" width="150px" />
    </a>
    <p style="text-align: center;">MCF10A Day 5</p>
  </div>
  <div>
    <a href="gif/10a_day7.gif">
      <img src="gif/10a_day7.gif" alt="Video Preview 3" width="150px" />
    </a>
    <p style="text-align: center;">MCF10A Day 7</p>
  </div>
</div>




---
### 🌌  Framework
<div align="center">
  <img src="diagram/framework.png" alt="MAT3D Framework" style="width:80%;"/>
</div>

---

## 🛠️ Environment Setup

Set up the environment for MAT3D as follows:

```bash
python3.10 -m venv MAT3D_env 
source MAT3D_env/bin/activate 
pip install -r requirements.txt
```

---

## 📂 Dataset

### 🔗 Download Links:
- [Synapse Multi-Organ Dataset](https://www.synapse.org/#!Synapse:syn3193805/wiki/89480)  
- [ACDC Challenge Dataset](https://www.creatis.insa-lyon.fr/Challenge/acdc/)

### 🗂️ Folder Structure:
Organize your data as follows:

```
data/  
├── imagesTr/  
│   ├── img1.nii.gz  
│   ├── img2.nii.gz  
├── labelsTr/  
│   ├── label1.nii.gz  
│   ├── label2.nii.gz  
├── dataset.json  
```

---

## 🚀 Running the Code

This repository is built upon the foundational work provided in [Synapse](https://github.com/LeonidAlekseev/Swin-UNETR).

### Training

Before training, configure the hyperparameters in the `config.py` file:

#### 🔧 Hyperparameter Configuration:
- **`data_dir`**: Path to the dataset.  
- **`saved_model_dir`**: Directory to save trained models and checkpoints.  
- **`num_samples`**: Number of samples for training.  
- **`num_classes`**: Number of target classes + background.  
- **`input_size`**: Dimensions of input images/data.  
- **`input_channels`**: Number of input channels (e.g., grayscale=1, RGB=3).  
- **`feature_size`**: Size of feature vectors extracted by the model.  
- **`use_checkpoint`**: Enable/disable model checkpointing.  
- **`learning_rate`**: Initial learning rate.  
- **`weight_decay`**: L2 penalty rate for regularization.  
- **`max_iterations`**: Maximum number of training iterations.  
- **`eval_num`**: Frequency of evaluations during training.

#### Start Training:
```bash
python3.10 main.py  
```

---

## 📊 Results

### Quantitative Results (Microscopic data):
<div align="center">
  <img src="diagram/numeric_results.png" alt="Quantitative Results" style="width:80%;"/>
</div>

### Clinical data Visualization:
<div align="center">
  <img src="diagram/visual_res.png" alt="Visualization Results" style="width:80%;"/>
</div>

### Microscopic data Visualization:

<div align="center">
  <img src="diagram/visual_res2.png" alt="Visualization Results" style="width:80%;"/>
  
</div>


## 📣 Citation

If any part of this repository is helpful in your research, please consider citing our paper.

---
