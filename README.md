# kgn
---
## Introduction
KGN is a Nearest Neighbor Search algorithm, based on NSG  

The project is currently closed-source, and we will consider open sourcing it after the associated research paper has been accepted.

---

## Installation
### Step 1: Configure environment dependencies
```bash
sudo apt install -y git cmake g++ python3 python3-setuptools python3-pip libblas-dev liblapack-dev
pip3 install wheel pybind11 faiss-cpu
```
### Step 2: Clone the Repository
```bash
git clone https://github.com/Henry-yan/kgn.git
```
### Step 3: Install the package
```bash
pip3 install kgn/pykgn-1.0.0-cp310-cp310-linux_x86_64.whl
```
---
## Usage
```python
import pykgn
```


---
## Results
The test results from running [ann-benchmarks](https://github.com/erikbern/ann-benchmarks) on an Alibaba Cloud ECS r5.2xlarge instance are as follows:

### sift-128-euclidean

![image](results/sift-128-euclidean.png)

---

### fashion-mnist-784-euclidean

![image](results/fashion-mnist-784-euclidean.png)

---

### nytimes-256-angular

![image](results/nytimes-256-angular.png)

---