# GraphDexDeform

`This is a final project for CS598 [Deep Learning with Graphs](https://ulab-uiuc.github.io/CS598/#schedule) Fall 2024 at UIUC.` 

GraphDexDeform is a course project focused on manipulating deformable objects using a dexterous hand, leveraging Graph Neural Network-based dynamics models.

## Installation
```shell
conda env create -f environment.yml
conda activate gbnd 
```

## Data
We generate our data based on [DexDeform](https://github.com/sizhe-li/DexDeform). We share our processed dataset in the [Googld Drive](https://drive.google.com/drive/folders/1r23vL5sVJQIcIiRu4xNZwSbk7rReAnY_?usp=sharing).


## GNN-based Dynamics Model
To train and evaluate the GNN-based dynamics model, please run the following command:
```shell
cd src
# preprocessing
python dynamics/preprocess.py --config ./config/folding.yaml

# training
python dynamics/train.py --config ./config/folding.yaml

# evaluate
python dynamics/evaluate.py --config ./config/folding.yaml
```

## Trajectory Optimization
We provide the model-based trajectory optimization implementation on the folding task, it should be put into the [DexDeform](https://github.com/sizhe-li/DexDeform) directory due to the simluation compiling issue. Please run the following command with the trained model:
```shell
cd src
python planning/planning.py 
```
