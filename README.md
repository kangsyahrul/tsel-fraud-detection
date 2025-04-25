# Problem Set 2

## 1. Setup Environemnt
This step assume that Conda is already installed.

### 1.1. Create Conda Environment
```
conda create -n tsel-fraud-det python=3.9
```

or 
```
conda env create -f environment.yml
```

### 1.2. Activate
```
conda activate tsel-fraud-det
```

### 1.3. Install Dependencies
```
conda install jupyter
python3 -m ipykernel install --user --name tsel-fraud-det --display-name "tsel-fraud-det"
```

```
pip3 install -r requirements.txt
```

### 1.4. Export 
```
conda env export > environment.yml
```

### 1.5. Update
```
conda env update -f environment.yml --prune
```

---

## 2. Setup Kaggle

### 2.1. Download Kaggle API Token
```
mkdir -p ~/.kaggle
cp ./kaggle.json ~/.kaggle/
chmod 600 ~/.kaggle/kaggle.json
```

### 2.2. Download Datasets
To download dataset, we can download using this CLI.

```
kaggle competitions download -c ieee-fraud-detection
```

### 2.3. Unzip Datasets
```
mkdir datasets/
unzip ieee-fraud-detection.zip -d datasets/
rm ieee-fraud-detection.zip
```

---

## 3. Experiment Tracking with [MLFlow](https://github.com/aimhubio/aim)

### 3.1 Install
```
pip3 install mlflow
```

### 3.2 Run
```
mlflow server --host 127.0.0.1 --port 5000
```

---

## 4. Methodology and Result
*Will be available on [Github Page](https://github.com/kangsyahrul/tsel-fraud-detection) soon*