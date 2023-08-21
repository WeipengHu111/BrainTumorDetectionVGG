# BrainTumorDetectionVGG
Brain tumors can be classified as either benign or malignant, and early detection is crucial for improved patient outcomes. Deep Neural Networks (DNNs), specifically Convolutional Neural Networks (CNNs), have shown promising results in detecting brain tumors through Magnetic Resonance Imaging (MRI) images. We propose a novel approach that combines feature extraction techniques with VGG-16 CNN to improve tumor detection accuracy. We evaluate network performance using Sensitivity, Specificity, and Precision, in addition to the accuracy criterion. Our results show that the SoftMax classifier has the highest accuracy in the CNN based on the testing images. Our proposed method achieved a remarkable accuracy of 100% on the small scale of test data, which highlights the potential of DNNs in improving the accuracy of tumor diagnosis. This method has important implications for clinical practice, as it can assist physicians in making more informed diagnoses and devising appropriate treatment plans for patients with brain tumors. By utilizing the power of VGG-16 CNN in analyzing medical imaging data, we can obtain valuable information about the location, size, and type of the tumor. Ultimately, this can lead to more precise and effective treatment plans, resulting in improved patient outcomes.

1.algorithm and baseline implementation-VGG16

This work is to do image classification task for tumor detection. The main model on this task is VGG-16.
The baseline is DenseNet which being tested on the same dataset. 
The algorithm and basline implementation 
are all in the source code file which is called detectingbraintumors-densenet121-vgg16. 
The baseline (DenseNet) is the first model output after running in the source code. 
VGG-16 is the second model output after runs the code. 

2.Datasets

The data set images used in this paper include brain MRI images of 245 (images) patients, 
including normal and brain tumors patients who referred to imaging centers because of headaches 
After examination and diagnosis of the doctor, 
the collected images included brain images of 155 healthy patients Include 245 images which has 16 images 
for testing data and 123 images for the train data. 90 patient tumors have 9 images for test data and 73 images
for the train data. The collected images originally had an initial size of 512 × 512.
Datasets are in the zip file "597_VGG\archive" location. It is splitted to no and yes mannually for labelling.
Yes represents the tumor image and No for the non-tumor image as fact. They are the total input images for
the models. Test, Train, and Validation datasets will be divided in the algorithm from the source codes.
For the TEST, TRAIN, and VAL files, they are output datasets after I run the source code. The total number 
of the datasets images is 245, which is a relatively small scale as a dataset.

3.Outcome

For VGG-16

accuracy
	training         	 (min:    0.617, max:    1.000, cur:    1.000)
	validation       	 (min:    0.500, max:    1.000, cur:    1.000)
f1_score
	training         	 (min:    0.612, max:    1.000, cur:    1.000)
	validation       	 (min:    0.333, max:    1.000, cur:    1.000)
Loss
	training         	 (min:    0.000, max:    0.698, cur:    0.001)
	validation       	 (min:    0.020, max:    0.681, cur:    0.028)
precision_6
	training         	 (min:    0.707, max:    1.000, cur:    1.000)
	validation       	 (min:    0.789, max:    1.000, cur:    1.000)
recall_6
	training         	 (min:    0.553, max:    1.000, cur:    1.000)
	validation       	 (min:    0.200, max:    1.000, cur:    1.000)


For DenseNet(baseline)

accuracy
	training         	 (min:    0.755, max:    1.000, cur:    0.995)
	validation       	 (min:    0.375, max:    0.833, cur:    0.792)
f1_score
	training         	 (min:    0.778, max:    1.000, cur:    0.997)
	validation       	 (min:    0.000, max:    0.875, cur:    0.839)
Loss
	training         	 (min:    0.023, max:    0.534, cur:    0.027)
	validation       	 (min:    0.431, max:    3.522, cur:    0.838)
precision_2
	training         	 (min:    0.851, max:    1.000, cur:    1.000)
	validation       	 (min:    0.000, max:    1.000, cur:    0.812)
recall_2
	training         	 (min:    0.659, max:    1.000, cur:    0.992)
	validation       	 (min:    0.000, max:    1.000, cur:    0.867)

Since the dataset is relatively small, the outcome of VGG-16 models on classification task is really outstanding.
Based on the evaluation metrics for tumor detection in image classification, 
VGG-16 has demonstrated superior performance. As a point of comparison, the DenseNet model, 
which serves as the baseline, is outperformed by VGG-16 in all evaluation metrics.
