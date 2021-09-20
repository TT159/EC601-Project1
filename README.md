# EC601_Project_1
ID: U68023245 </br>
Name: Tian, Tan </br>
This is a project of course EC601. 
I choose the topic: RSNA-MICCAI Brain Tumor Radiogenomic Classification.

## Problem Statement
### What does the topic cover?
This topic covers data science, intelligent systems and biomedical science. We need to use these technologies to solve a biomedical problem, named brain tumor. Malignant tumors of the brain are a life-threatening disease, and glioblastoma is the hardest of them all. From the relevant description in Kaggle, we can get some knowledge of biological sciences.
> Glioblastoma is the most common brain cancer in adults and the one with the worst prognosis, with a median survival time of less than one year. The presence of a specific gene sequence called MGMT promoter methylation in tumors has been shown to be a favorable prognostic factor and a powerful predictor of responsiveness to chemotherapy.</br>

In order to solve this problem, we are asked to use MRI (magnetic resonance imaging) scans to predict glioblastoma genotypes to train and test your model, so that we can detect the presence of MGMT promoter methylation. Therefore, how to classify and recognize the status of brain tumor images is the key point.

### Why it is important?
Glioblastoma (GBM), and diffuse astrocytic glioma with molecular features of GBM, are the most common and aggressive malignant primary tumor of the central nervous system (CNS) in adults, with extreme intrinsic heterogeneity in appearance, shape, and histology [1]. GBM patients have an average prognosis of 14 months, following standard of care treatment, and 4 months left untreated [2]. 
> Currently, genetic analysis of cancer requires surgery to extract tissue samples. It may then take several weeks to determine the genetic characteristics of the tumor. Depending on the outcome and the type of initial treatment selected, subsequent surgery may be required.

Therefore, I think there are several reasons for its importance.
- Time Consuming. For patients, the most important and precious thing is time. Even getting accurate medical diagnosis results just a little bit in advance is very valuable. Because it means that you can get the corresponding treatment as soon as possible. If we can get an accurate method to predict cancer genetics only through imaging (i.e. radiogenomics) with MRI (magnetic resonance imaging) scans, we can greatly reduce the time cost of pathological diagnosis.
- Labor Costs. At present, to diagnose the condition of cancer, we inevitably need medical staff to perform a surgery to determine if there is a tumor or not, and the patient also needs to experience more pain. However, if we can find a way, we only need one nuclear magnetic resonance instrument. Most importantly, patients can suffer less pain.
- Accurate and Objective. In a clinical process, the diagnosis is carried out by radiologists in a qualitative visual manner, and hence becomes subjective when dealing with numerous patients. Automated instrument diagnosis greatly reduces this risk and improves the type of treatment required.
- Classification. Manual detection and tracing of tumor sub-regions is mostly based on the clinical experience of medical staff. However, human experience is limited. If we develop the method to accurately identify the tumor sub-regions boundaries in MRI, we can train and test through hundreds of cases in a very short time, so as to gain a lot of 'experience'.

## Project Applications
From my perspective, this application can be widely used in the medical field. Although various experimental treatment options have been proposed during the past 20 years, there have not been any substantial differences in patient prognosis. Accurate identification of brain tumor in MRI is of profound importance in many clinical applications, such as surgical treatment planning, image-guided interventions, monitoring tumor growth, and the generation of radiotherapy maps[1]. If this diagnostic method with MRI can be successfully implemented, it will not only solve a medical problem, but also save all patients suffering from this cancer. MRI provides us an indirect method to investigate our brain to figure out the defects and treat them in order to extend a human life. If we can develop a method to increase the survival time by a little bit, it will be a huge spiritual treasure for patients and their families. 

## My interests
I think that under different training algorithms, the accuracy of recognition and prediction is different. Thus, I am curious how to improve the accuracy of image recognition. What excites me the most is that we humans are able to correct the natural course of our body by ourselves so as to extend life and exert our value.

## Literature Review
In this part, I read some diferent papers related to this field in research community and industry. 
- Research 1 [3]. In this paper, the process of radiomics starts with delineating the region of interest, that is, the tumor, in an imaging study and then extracting quantitative data from the segmented volumes and entering them, as well as other clinical and genomic data, into a database. This database is subsequently analyzed, with use of artificial intelligence, machine learning, and/or statistical analysis, to predict the diagnosis and outcome.

- Research 2 [4]. In this paper, the first step is: Image Selection and Annotation Processing. They drawn the Regions of interest (ROIs) corresponding to enhancing necrotic portions of tumor and peritumoral edema. Then, quantitative image features were derived from these ROIs. After getting the data, they performed a statistical analysis on the robustness of the image feature.  

- Research 3 [5]. The purpose of the research is to evaluate the association of magnetic resonance (MR) imaging features with key molecular characteristics in patients with newly diagnosed glioblastoma. Similarly, at first, the researcher was approved by the local ethics committee to get the data set. Then, they processed the data. Finally, univariate analyses and machine learning models were applied to study the strength of association and discriminative value of MR imaging features for predicting underlying molecular characteristics.

Thus, from above all, I found that there are several steps to complete the work. First, we need to find a way to get the relevant data set, such as the MRI images of a brain tumor. Then, we need to preprocess the data. For example, we need to segment the image to extract key features or reduce noise to make them more clear. After this, we use different machine learning algorithms to train the data and get the model. In the fourth step, we use some known samples to evaluate and optimize the model. In the end, when we get a suitable model, we use this model to predict and analyze real cases.

## Open Source
- Data set. On kaggle, it provides us the data set, named Brain Tumor Segmentation (BraTS). 
- Data processing. After reading some open source research, I find a way to create animations for data [6,7]. In another research [8], the author performs some basic EDA and use Weights and Biases to visualize the data interactively. I think this is the best way to understand the idea and present the data to make it more intuitive for everyone. Weights & Biases (W&B) [9] is a set of machine learning tools that helps you build better models faster. 
- Frameworks. For the part of processing data (i.e. classification, training), I found that different people use different machine learning frameworks, such as tensorflow, pytorch, keras [10-12]. 
- Algorithm. As for training algorithm, I found that most people use the convolutional neural network (CNN) algorithm [13,14]. 
- Physical device. In additoin, I found that some people use GPU to train the data, some people use TPU to complete this work.


## Duplicate the Results
I have not yet started the duplication stage. However, I found a tutorial with similar steps to our project on GitHub [15]. The goal of this tutorial is to build a deep learning classifier to accurately distinguish chest and abdomen x-rays. The model uses 75 images obtained from Open-i to recognize images for training. I am reading this tutorial and trying to understand it. I will search more information related to our project.  

## References
[1] [The RSNA-ASNR-MICCAI BraTS 2021 Benchmark on Brain Tumor Segmentation and Radiogenomic Classification](https://arxiv.org/abs/2107.02314)</br>
[2] [Overall survival prediction in glioblastoma patients using structural magnetic resonance imaging (MRI): advanced radiomic features may compensate for lack of advanced MRI modalities](https://www.spiedigitallibrary.org/journals/journal-of-medical-imaging/volume-7/issue-3/031505/Overall-survival-prediction-in-glioblastoma-patients-using-structural-magnetic-resonance/10.1117/1.JMI.7.3.031505.full?SSO=1)</br>
[3] [Pediatric Brain Tumor Genetics: What Radiologists Need to Know](https://pubs.rsna.org/doi/full/10.1148/rg.2018180109)</br>
[4] [Glioblastoma Multiforme: Exploratory Radiogenomic Analysis by Using Quantitative Image Features](https://pubs.rsna.org/doi/full/10.1148/radiol.14131731)</br>
[5] [Radiogenomics of Glioblastoma: Machine Learning–based Classification of Molecular Characteristics by Using Multiparametric and Multiregional MR Imaging Features](https://pubs.rsna.org/doi/full/10.1148/radiol.2016161382)</br>
[6] [Brain Tumor - EDA with Animations and Modeling](https://www.kaggle.com/ihelon/brain-tumor-eda-with-animations-and-modeling)</br>
[7] [EDA with Animation](https://www.kaggle.com/avloss/eda-with-animation)</br>
[8] [Brain Tumor EDA and Interactive Viz with W&B](https://www.kaggle.com/ayuraj/brain-tumor-eda-and-interactive-viz-with-w-b)</br>
[9] [Weights and Biases](https://wandb.ai/site)</br>
[10] [Dataset to Model with Tensorflow](https://www.kaggle.com/ohbewise/dataset-to-model-with-tensorflow)</br>
[11] [RSNA Keras 3D CNN Voxel Train](https://www.kaggle.com/sreevishnudamodaran/tpu-rsna-keras-3d-cnn-voxel-train)</br>
[12] [MRI Classification Data Pipeline [Pytorch]](https://www.kaggle.com/pranav2109/mri-classification-data-pipeline-pytorch)</br>
[13] [EDA+Data processing+Basic CNN-Tumor classification](https://www.kaggle.com/arunamenon/eda-data-processing-basic-cnn-tumor-classification)</br>
[14] [[TF] Simple Prediction with 3DCNN](https://www.kaggle.com/masatomurakawamm/tf-simple-prediction-with-3dcnn)</br>
[15] [2019 SIIM-ACR Pneumothorax Segmentation Challenge](https://github.com/ImagingInformatics/machine-learning/tree/master/2019_Pneumothorax_Challenge)</br>





