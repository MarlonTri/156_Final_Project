# 156_Final_Project

[`notebooks/generator.ipnyb`](https://github.com/MarlonTri/156_Final_Project/blob/master/notebooks/generator.ipynb)
is the file that generates/searches for models that are accurate.

[`notebooks/accuracy_check.ipnyb`](https://github.com/MarlonTri/156_Final_Project/blob/master/notebooks/accuracy_check.ipynb)
checks accuracy of models that are saved to disk, compared to linear regression.

[`notebooks/big_train.ipnyb`](https://github.com/MarlonTri/156_Final_Project/blob/master/notebooks/big_train.ipynb)
trains 4 models, one for each location. Will take all night to run even with GPU acceleration.

The `container` folder is for setting up the nvidia-docker container that runs the Jupyter Notebook server. You don't need to worry about that unless you want to run this project. To run project, install and run nvidia-docker. Run `build.sh`, then edit the volume argument in `run.sh` to match your directory then run `run.sh`.
