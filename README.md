#  MedSAM-2 on BRATS 2019 - Brain Tumor Segmentation

This project demonstrates the use of **MedSAM-2** for segmenting brain tumor subregions using the **BRATS 2019** dataset. The task reframes segmentation as a video tracking problem using **SAM2 architecture** and evaluates its performance through Dice and IoU scores.


##  Dataset

**BRATS 2019** is a publicly available dataset for brain tumor segmentation and includes:

* **Modalities**: `T1`, `T1ce`, `T2`, `FLAIR`
* **Segmentation Targets**:

  * Enhancing Tumor (ET)
  * Tumor Core (TC)
  * Whole Tumor (WT)

 Download it manually from [Kaggle BRATS 2019](https://www.kaggle.com/datasets/awsaf49/brats-2020-dataset-training-validation)


##  Model: MedSAM-2 Overview

* Based on **Segment Anything Model (SAM2)**
* Introduces **self-sorting memory bank** to preserve temporal coherence
* Performs **one-prompt segmentation** across sequences


##  How to Run

### 1. Open in Google Colab

```bash
Open `3d-mri-brats.ipynb` in Google Colab
```

### 2. Upload Your Data

Upload the BRATS volumes (`.nii.gz` for T1, T1ce, T2, FLAIR) to your Google Drive and set the correct path in the notebook.

### 3. Install Dependencies

```python
!pip install nibabel matplotlib scikit-image
```

### 4. Run Each Cell Step-by-Step

* Load and normalize MRI volumes
* Apply MedSAM-2 model
* Generate and visualize segmentation masks
* Evaluate with Dice & IoU scores

---

##  Evaluation

* **Dice Score**: Measures overlap between prediction and ground truth
* **IoU Score**: Intersection over Union

The notebook provides:

* Quantitative evaluation metrics
* Visual overlays of predicted masks



##  Deliverables

*  Kaggle Notebook (`3d-mri-brats.ipynb`)
*  Segmentation visualizations
*  Dice and IoU evaluations
*  README with instructions (this file)



##  Author

**Ayesha Tariq**


##  Requirements.txt


numpy
nibabel
matplotlib
scikit-image


You can install them in one command:

```bash
pip install -r requirements.txt
```

