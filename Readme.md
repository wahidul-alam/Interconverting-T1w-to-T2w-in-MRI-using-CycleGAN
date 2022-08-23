# T1-T2 weighted synthetic image generation using CycleGAN
### project description: 
T2 is comparatively slower to acquire than T1 but, contains more features useful for classification/ segmentation. In this project, we implement [CycleGAN](https://junyanz.github.io/CycleGAN/) to generate synthetic T2 images from T1 weighted images without compromising speed and image quality. For demonstration, tow datasets are used: inhouse airway dataset, [Brats](https://www.med.upenn.edu/sbia/brats2018/data.html) (open-sourced) dataset

### Dataset:
A sample dataset is provided with this code in data folder. The sample data contain T2 and T1 examples from brain MRI dataset.
The dataset directory is provided in `/configuration/config.py`.

### Preprocessing:
The Raw data we have is in Dicom format. So it needs to be sliced and staked on different set of folders. The preprocessing code is indipendently used to slice and store the images.Convert the raw dicom file using `/preprocessing/readDicomImages.ipynb`. The code have essesntial steps to convert the Dicom to images and to save them into specific folders.

### Model Training:
The model can be trained using `demo.ipynb`. On running the code the data is extracted and converted into a numpy file.
Later this data is loaded into the GAN model for training.

### Results:
the results and the model get automatically generated into the root folder.
