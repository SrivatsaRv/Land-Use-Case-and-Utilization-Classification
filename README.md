## Labeling Land: Land Use Classification using Convolutional Neural Networks

### Problem Statement:
This helps a variety of stakeholders, including conservationists, urban planners, and environmental scientists, survey and identify patterns in land use to see which natural areas are under threat or which areas are best for urban development. This specific project helps the agriculture company. Imagery companies can use land use classification models to categorize what’s in each image and optimize their efforts towards the parts of land that are important to them. For example, an agriculture company will only want to be concerned with land that’s labelled as pasture, annual crop, or permanent crop. If a satellite is constantly taking images, this project would help save hours of time manually sorting through imagery.

In addition to sorting imagery, land use classification is important for identifying the parts of an image to which certain analyses are applied. For example, if the company has different crop stress algorithms for fields that are next to urban areas versus fields that are next to rivers, this project would help them to automate the process of applying these specialized algorithms and more effectively solve environmental problems.

### Dataset Description:
For this project the dataset can be downloaded locally [here](http://madm.dfki.de/downloads). The dataset consists of 27,000 labeled images of 10 different land use classes:
- Annual Crop
- Forest
- Herbaceous Vegetation
- Highway
- Industrial
- Pasture
- Permanent Crop
- Residential
- River
- Sea / Lake

Each multispectral image consists of 13 different color bands that represent different wavelengths of light/color and different resolutions. These different light bands help distinguish parts of the landscape that reflect certain types of light in particular ways. Since most images don’t include special bands like Vegetation Red Edge, Coastal aerosol, or SWIR, for this project I chose to only use the red, green, and blue bands in an effort to make my model generalizable to most images.

### Project Plan
This project includes notebooks for all stages in the process: 
1. [Data preparation](https://github.com/SrivatsaRv/Land-Use-Case-and-Utilization-Classification/blob/main/0_build_rgb_dataset.ipynb)
2. [Exploratory data analysis](https://github.com/sophy26/land-use-classification/1_exploratory_data_analysis.ipynb)
3. [CNN with model tuning](https://github.com/sophy26/land-use-classification/3_cnn_tuned.ipynb)

Using keras as the main machine learning library for this project, I crafted a RGB jpeg dataset from thousands of thirteen-band tif files, and used transfer learning, data augmentation, and regularization to build three different models with increasing performance.
