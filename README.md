# dp-BREATH: source dataset

Source feature data extracted from CT lung scans and employed in [Cazzolato et al. 2019].

## License and Citation Request

dp-BREATH source dataset is available for researchers and data scientists under the GNU General Public license.
In case of publication and/or public use of the available data, as well as any dataset derived from it, one should acknowledge its creators by citing the following paper.

> [Cazzolato et al. 2019] dp-BREATH: Heat maps and probabilistic classification assisting the analysis of abnormal lung regions. DOI: https://doi.org/10.1016/j.cmpb.2019.01.014. In Computer Methods and Programs in Biomedicine, 2019.

## Nomenclature and Data Overview

Adopted nomenclature:
 - CH stands for Color Histogram 
 - LBP stands for Local Binary Patterns features
 - PDF stands for Probability Density function
 - PCA stands for Principal Component Analysis

The class numbering adopted in the files refer to the following lung findings:
 - **1**: Normal (healthy tissue)
 - **2**: Consolidation
 - **3**: Emphysema
 - **4**: Thickening
 - **5**: Honeycombing
 - **6**: Ground Glass

The following data is available:
 - CH and LBP feature vectors extracted from 246 CT lung images
 - LBP feature vectors extracted from 3,258 Regions of Interest of lung CT images
 - LBP, PDF and PCA feature vectors extracted from 573 superpixels, which were generated from the lung CT images

For any further information, please refer to [Cazzolato et al. 2019].

## Full Images

 - **Color Histogram features** for each lung CT image, with:
	 - Class Number (class)
	 - Image Name (imgName)
	 - 8 features (fv_001, ..., fv_008)

 - **LBP features** for each lung CT image, with:
	 - Class Number (class)
	 - Image Name (imgName)
	 - 256 features (fv_001, ..., fv_256)

## Regions of Interest (ROIs)

- **Color Histogram features** for each region of interest of lung scans, with:
	- Image Name (ROI)
	- 8 features (fv_001, ..., fv_008)
	- Class Number (class)

- **LBP features** for each region of interest of lung scans, with:
	- Image Name (ROI)
	- 256 features (fv_001, ..., fv_256)
	- Class Number (class)

## Superpixels

 - **LBP features** of superpixels extracted from the full images:
	 - Class Number (class)
	 - Image Name (imgName)
	 - Superpixel Number (superpixelNumber)
	 - 256 features (fv_001, ..., fv_256)

 - Two first **PCA features** of superpixels extracted from the full images:
	 - Class Number (class)
	 - Image Name (imgName)
	 - Superpixel Number (superpixelNumber)
	 - 2 features (pca_1, pca_2)

 - Six **PDF features**, each corresponding to each class label, computed for the superpixels extracted from the full images:
	 - Class Number (class)
	 - Image Name (imgName)
	 - Superpixel Number (superpixelNumber)
	 - 6 features (pdf_1, ..., pdf_6)

## Repository Organization

The files available for download are organized in this repository as follows:
 - **full_images/**
	 - ct_images_CH.csv
	 - ct_images_LBP.csv
 - **regions_of_interest/**
	 - rois_CH.csv
	 - rois_LBP.csv
 - **superpixel_images/**
	 - superpixel_images_LBP.csv
	 - superpixel_images_PCA.csv
	 - superpixel_images_PDF.csv
