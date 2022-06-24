# Prostate_Cancer_Prediction_and_Classification
A collection of code and information pertaining to our prostate cancer prediction and classification project at GW.

Prostate Cancer (PCA) is the second most frequent cancer malignancy affected men and accounts for a  large portion of male cancer deaths. It's a huge burden for both patients and their families and amounts to losses of billions of dollars in productivity for those managing the disease. Rates of PCA are only projected to increase, making the identification of effective methods for management and treatment of paramount importance. 

The gold standard for diagnosis and risk quantification of PCA severity is transrectal ultrasound scan (TRUS) guided biopsy. This procedure is invasive and requires a surgical procedure. As such non-invasive measures such as prostate MRI have become increasingly popular as a method to improve diagnosis, treatment, and quantification of PCA. 

Treatment for PCA typically involves surgery (radical prostatectomy - removal of the prostate), radiation therapy, or in cases of advanced PCA - chemotherapy. Not all patients with PCA require treatment. In fact most cases are low-risk and can be monitored. This makes stratification of which cases of PCA are low risk and which are high risk even more important. 

This project utilized an open source dataset, the SPIE ProstateX (PX) challenge. It is available for download here: https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=23691656 In addition to local data where lesions were identified from radiologist tracings. 

This project utilized 2-Dimensional data (Single MRI DICOM slices from the PX dataset (T2W + ADC) data and corresponding BMP files - lesions were identified by i,j,k coordinates provided with the data) from the PX dataset in addition to local dataset (Single MRI DICOM slices (T2W + ADC) where lesions were identified by radiologist tracing). 

Code and details are provided here to assist others interested in building models on Prostate MRI. In particular due to the popularity of the ProstateX data, code is provided here to assist others utilizing this data. 

Included code files:
**Binary_Classification_ResNet_for_csPCA**
Creates a ResNet classification model for clinically significant (csPCA) vs not clinically significant PCA. This is just the training and testing component. 

**Identify_Lesion_From_Tracing**
This creates a "slice mask" of the pixels corresponding to a lesion identified by radiologist tracing. This code also includes code to draw a box around the lesion and plot just the area contained in the tracing on a new file.

**Organize_ProstateX_Data_BMP_Files 
**
This code organizes the ProstateX T2W BMP files into Cancer (csPCA) vs not cancer directories for an easy model build. This is included to assist others interested in an easy start model without doing the full DICOM digging, or to use the BMP files with the DICOM files to make a full model. 

**If you find this project or code helpful and would like to use any of it, please cite the following study:
**

Provenzano D, Melnyk O, Whalen M, Loew M, Haji-Momenian S. Performance of a highly accurate prostate cancer machine learning algorithm on MR image data from a different institution: do the results hold up? ARRS. Presented May 2022. 
