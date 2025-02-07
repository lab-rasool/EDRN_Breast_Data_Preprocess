# **EDRN - Preprocessing Mammograms for AI**  
### **Standardizing Breast Screening Data for Deep Learning**  

This repository provides a comprehensive preprocessing pipeline for 2D mammogram images, ensuring standardization, consistency, and usability for deep learning applications in breast cancer screening. The pipeline converts raw DICOM images into AI-ready datasets, including structured metadata and statistical visualizations.  

## **Overview**  

Deep learning models require well-structured and preprocessed datasets for reliable training and evaluation. This repository introduces a robust preprocessing framework to prepare mammogram data for AI-driven analysis. The dataset comprises three matched case-control studies (N=349, 318, 180 matched case-controls), with each patient having at least four DICOM images:  

- **L-CC (Left Craniocaudal)**  
- **R-CC (Right Craniocaudal)**  
- **L-MLO (Left Mediolateral Oblique)**  
- **R-MLO (Right Mediolateral Oblique)**  

Additionally, clinical metadata—including BI-RADS classifications, study logs, and hormonal replacement therapy usage history—is integrated into structured JSON files for ease of use in deep learning models.  

## **Key Features**  

✅ **DICOM Processing**  
- Converts DICOM images to PNG format for better compatibility and storage efficiency.  
- Resizes images to **1664×2048** pixels.  
- Aligns images to a common coordinate space.  
- Normalizes images to **zero mean and unit variance**.  

✅ **Data Augmentation**  
- Applies **random horizontal/vertical flips, rotations (up to 20°), affine transformations, and color jitter** to enhance model generalizability.  

✅ **Metadata Extraction & Organization**  
- Extracts **DICOM headers** and integrates them with clinical study logs, BI-RADS classifications, and hormonal history.  
- Saves metadata in structured **JSON files** for streamlined analysis.  

✅ **Dataset Splitting**  
- Partitions data into **training-validation (80%) and test (20%)** sets.  
- Further splits the **training-validation set into 80%-20%** partitions for robust model evaluation.  

✅ **Statistical Visualizations**  
- Provides insights into **age distribution, image count, laterality, view type, density, BI-RADS classification, cancer prevalence, and implant presence**.  

✅ **Reproducibility & Open-Source Availability**  
- The entire pipeline is available as a **Jupyter Notebook**, enabling easy integration into deep learning workflows.  

## **Getting Started**  

### **1. Clone the Repository**  
```bash  
git clone https://github.com/lab-rasool/EDRN_Breast_Data_Preprocess.git
cd EDRN_Breast_Data_Preprocess  
```

### **2. Install Dependencies**  
Ensure you have Python installed. You can install the required packages using:  
```bash  
pip install -r requirements.txt  
```

### **3. Run the Preprocessing Notebook**  
Open the Jupyter Notebook and execute the preprocessing steps:  
```bash  
jupyter notebook Process_mammograms.ipynb  
```

### **4. Output Files**  
- **Processed PNG images** (aligned, normalized, and augmented).  
- **JSON metadata** files containing clinical and imaging information.  
- **Data splits** (training-validation-test).  
- **Visualizations** for exploratory analysis.  

## **Contributing**  
Contributions are welcome! Feel free to fork the repository, submit issues, or create pull requests.  

## **License**  
This project is released under the **MIT License**.  

## **Acknowledgments**  
Special thanks to the research community advancing AI applications in breast cancer screening.  

