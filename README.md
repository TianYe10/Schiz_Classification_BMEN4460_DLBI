# Schiz_Classification_BMEN4460_DLBI

### This repository is private, only sharing with students doing BMEN 4460 course final project in Spring 2023 at Columbia.
## Project name: Schizophrenia MRI Classification Using Deep Learning

All required source codes and commands are saved in this repositor, including:

**main_10fold.py**

**data_loader_10fold.py**

**GlobalLocalTransformer3D_multiscale.py**

**vgg3D_for_transformer.py**

**vgg.py**

**command.sh** (command instruction file, not code)

**Improving Across-Dataset Schizophrenia Classification with Structural Brain MRI Using Multi-scale Transformer.pdf** (the model raw abstract to help you understand the whole project, optional reading material) (Abstract is accepted by ISMRM 2023 and is going to be published in June)

If you are familiar with deep learning pipelines and have Python coding experience, you should have no trouble understanding the codes on your own. If you do need help implementing them, please see the instructions for each file below:


### Before we start: ###

All the codes are saved in .py format. If you are using online coding enviroment such as Colab and Kaggle, you probably run into the jupyter notebooks ending with .ipynb. To run the .py files on Colab, please see this  [quick tutorial](https://rafat-joy99.medium.com/how-to-run-py-files-on-google-colab-46af2831e166/) and more helpful instructions online.

The .py codes used to be runned on the server with a cuda GPU. If you are utilizing public available GPUs such as Colab GPU, you may need to set up your cuda, otherwise the codes may give you an error about cuda. See this [discussion](https://stackoverflow.com/questions/50560395/how-to-install-cuda-in-google-colab-gpus) as an example on how to check and set up your cuda. Hopefully it should be fast and straightforward to set up your cuda.

This kinds of GPU errors can pop up differently for different laptops and Google account situations. Please first try to solve it on your own, as this problem may happen all the time when you are running any machine learning codes, even beyond our course.

### main_10fold.py ###

The only .py file you need to run using the command in command.sh. It imports the dataloader and the model, runs the main functions (and saves the trained model).

Please change the data path to where you save all ten folds of your MRI data! (there is a upper-cased notice at where you need to change the path)

Please modify the 'device' variable based on how you set up / name your cuda!

Please take a thorough look into all the 'parser.add_argument' to have a basic idea of what arguments and parameters we have (and we can change).

You can loaded a pre-trained model, or train a new model. The models for option are:
1. 'GlobalLocalBrainAge', the transformer-based model, as default.  
2. VGG model, commented out for now.

### GlobalLocalTransformer3D_multiscale.py ###

The 3D Multi-scale Transformer (MST) model code.

To undersnad the Multi-Scale Transformer better, read the [abstract](https://github.com/TianYe10/Schiz_Classification_BMEN4460_DLBI/blob/main/Improving%20Across-Dataset%20Schizophrenia%20Classification%20with%20Structural%20Brain%20MRI%20Using%20Multi-scale%20Transformer.pdf)! Especially the figure 1!

All unnecessary codes are commented out to save your time. If you want to modify the structure, you may want to take a deep look at line [204](https://github.com/TianYe10/Schiz_Classification_BMEN4460_DLBI/blob/83ed0b675615844ab313e5f7bbc98bb37b8ef26d/GlobalLocalTransformer3D_multiscale.py#L204) ~ 381.

