### Prerequisites

```
conda install pytorch torchvision

```
Install torch-scatter according to your pytorch version following instructions in this url: https://github.com/rusty1s/pytorch_scatter

To install other dependencies: 
```
pip3 install --user opencv-python
pip3 install --user open3d-python==0.7.0.0
pip3 install --user scikit-learn
pip3 install --user tqdm
pip3 install --user shapely
```

### KITTI Dataset

We use the KITTI 3D Object Detection dataset. Please download the dataset from the KITTI website and also download the 3DOP train/val split [here](https://xiaozhichen.github.io/files/mv3d/imagesets.tar.gz). We provide extra split files for seperated classes in [splits/](splits). We recommand the following file structure:

    DATASET_ROOT_DIR
    ├── image                    #  Left color images
    │   ├── training
    |   |   └── image_2            
    │   └── testing
    |       └── image_2 
    ├── velodyne                 # Velodyne point cloud files
    │   ├── training
    |   |   └── velodyne            
    │   └── testing
    |       └── velodyne 
    ├── calib                    # Calibration files
    │   ├── training
    |   |   └──calib            
    │   └── testing
    |       └── calib 
    ├── labels                   # Training labels
    │   └── training
    |       └── label_2
    └── 3DOP_splits              # split files.
        ├── train.txt
        ├── train_car.txt
        └── ...

### Training
```
bash train.sh

# computational-symmetry-in-AI-Robotics
