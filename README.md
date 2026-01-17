# YOLO-MEyes
Yolo training for MEyes app.

## Setup
I'm developing this on a mac and using Conda, you're free to use anything else.
All is documented in Jupyter notebooks (installation is on your hands mate).
Here are the instructions to create the dev env.

### Create it
```
conda create --name yolo-meyes
```

### Jupyter notebook kernel
```
conda install -y ipykernel
python -m ipykernel install --user --name yolo-meyes --display-name "YOLO for MEyes"
```

### Install PyTorch and Ultralytics
```
python -m pip install -U pip                                                                                  
python -m pip install torch torchvision torchaudio lxml requests pillow pyyaml matplotlib
python -m pip install -U ultralytics

```

## Datasets
### Bus
#### OpenImageV7
Don't forget to disable all Options.

https://storage.googleapis.com/openimages/web/visualizer/index.html?type=detection&set=valtest&c=%2Fm%2F01bjv
https://storage.googleapis.com/openimages/web/visualizer/index.html?type=detection&set=train&c=%2Fm%2F01bjv

##### Get Bus dataset
Loaded the entire page, navigated till the end and made sure all images got loaded correctly along the way.
On chrome, inspected first image, navigated to a top level div that contains all the dataset and copy pasted into `Datasets/openImagesV7-Bus.md`. Did this for both URIs.
Now lets process it so it matches YOLO requirements, follow along 


#### Cityscapes
Sounds like an amazing dataset, gonna try and gain access to it https://www.cityscapes-dataset.com