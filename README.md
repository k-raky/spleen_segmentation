# spleen_segmentation
Spleen segmentation from 3D CT images using Monai Library

### 3D Spleen Segmentation from CT Scans

Spleen segmentation in CT scans is an important task in medical image analysis, supporting applications such as organ volume measurement, surgical planning, and disease monitoring. Automating this process reduces manual effort and improves consistency.

### Project Overview

This project provides an automated pipeline for segmenting the spleen from 3D CT volumes using the MONAI framework and a 3D U-Net architecture:
	•	Preprocessing: Loads CT scans, reorients them to RAS, resamples voxel spacing, normalizes intensities, and crops the foreground region.
	•	3D U-Net Model: Processes full volumetric data to produce voxel-level spleen masks.
	•	Inference Pipeline: Uses sliding window inference to handle large 3D volumes, post-processes predictions, and saves results as .nii.gz segmentation files.

### File Summaries

**- spleen_3dunet.ipynb** : Implements the preprocessing pipeline, defines the 3D U-Net model, and prepares it for training on the dataset.

**- infer.ipynb** : Loads the trained model, applies the same preprocessing to new CT scans, runs sliding window inference, and saves the predicted spleen segmentation masks in nifti or dicom images for visualization.



<img width="981" height="547" alt="image" src="https://github.com/user-attachments/assets/3f313a35-d809-436f-919e-c3537bbb8f24" />

<img width="1360" height="528" alt="image" src="https://github.com/user-attachments/assets/55674546-e9a5-4834-b657-2f2265372f70" />

<img width="1196" height="562" alt="Capture d’écran 2025-08-14 à 23 02 16" src="https://github.com/user-attachments/assets/2d340254-6c5a-4b93-a797-2e37052bc666" />
