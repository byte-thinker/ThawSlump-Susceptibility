



# Thaw Slump Susceptibility Maps

Permafrost degradation on the Qinghai–Tibet Plateau (QTP) has accelerated under ongoing climate warming, triggering the formation of thaw slumps that can significantly impact infrastructure and local ecosystems. 

Assessing the spatial distribution of thaw slump susceptibility is therefore critical for understanding permafrost dynamics and supporting hazard-informed planning. 

To better assess these hazards, this study proposes a novel assessment framework that integrates **SBAS-InSAR–derived surface deformation** and **spatial-neighborhood information** to evaluate thaw slump susceptibility. 

The maps illustrate the spatial distribution of thaw slump susceptibility based on different CNN model configurations.

## Dataset Overview

Four model configurations are included:

| File Name             | Model  | Factors | InSAR Deformation | Notes                         |
| --------------------- | ------ | ------- | ----------------- | ----------------------------- |
| CNN1D_11f_noInSAR.tif | 1D-CNN | 11      | No                | Pixel-wise susceptibility     |
| CNN1D_12f_InSAR.tif   | 1D-CNN | 12      | Yes               | Pixel-wise susceptibility     |
| CNN2D_11f_noInSAR.tif | 2D-CNN | 11      | No                | Spatial neighborhood included |
| CNN2D_12f_InSAR.tif   | 2D-CNN | 12      | Yes               | Spatial neighborhood included |

All susceptibility maps were classified into **five levels** using the natural breaks (Jenks) method:

- Very low
- Low
- Moderate
- High
- Very high

## Color Scheme

A pre-defined ArcGIS layer file (`.lyr`) is provided to visualize the five susceptibility levels consistently:

- This layer corresponds to the five classes listed above.
- To use, load the corresponding `.tif` file in ArcGIS and apply the `.lyr` file for consistent symbology.

## Usage Notes

- These datasets are provided for **visual inspection and comparative analysis only**.
- The `.tif` files are compatible with common GIS software such as ArcGIS and QGIS.
- The `.lyr` file is intended for use in ArcGIS to replicate the color scheme used in the publication.