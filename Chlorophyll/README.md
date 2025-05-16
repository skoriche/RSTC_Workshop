# Chlorophyll-a Mapping in Alaska Using Google Earth Engine and Sentinel-2

**Google Colab Notebook for Workshop Participants**

**Notebook URL:**  
🔗 https://colab.research.google.com/drive/1TP40wS1sdRlRLhD9tlERNn31Dsaa-E7K

---

## 📘 Overview

This Colab notebook guides you through:

- Accessing Sentinel-2 imagery from **Google Earth Engine (GEE)**.
- Exporting the imagery to **Google Drive**.
- Analyzing the exported **GeoTIFF** file using `rasterio`, `numpy`, and `OpenCV`.
- Calculating **Chlorophyll-a concentrations** using the NDCI index (Mishra & Mishra, 2012).
- Visualizing and outlining high chlorophyll regions.

Area of Interest: **Kodiak Island, Alaska**  
Time Range: **May 2024 (typical HAB season)**

---

## How to Use This Notebook

### Step 1: Open the Notebook

Click this link to launch the notebook in Google Colab:

👉 [https://colab.research.google.com/drive/1Tmflpxw5pAWfW3OQaXHoauGtwZ-2RrFx](https://colab.research.google.com/drive/1Tmflpxw5pAWfW3OQaXHoauGtwZ-2RrFx)

---

### Step 2: Sign in and Run Cells

1. Sign in with your **Google account**.
2. From the Colab menu, go to **Runtime → Run all**, or run each cell manually using `Shift + Enter`.

---

### Step 3: Authenticate Earth Engine and Drive

You will be prompted to authorize access:

- **Google Earth Engine (GEE)**:
  - Click the URL provided in the cell output.
  - Sign in with your Google account.
  - Copy the token and paste it into the notebook.

- **Google Drive**:
  - You will be asked to mount your Drive.
  - Allow the necessary permissions to access your Drive.

---

### Step 4: Install Required Libraries

The following libraries will be installed automatically:
- `rasterio`
- `opencv-python`
- `earthengine-api`
- `matplotlib`, `numpy`

If prompted with errors, rerun the installation cells.

---

### Step 5: Output Location

The exported image will be saved to your **Google Drive** at:  
📁 `My Drive/EarthEngineExports/`

The filename format includes:
- Sentinel-2 acquisition date
- MGRS tile ID
- Cloud cover percentage

Example:  
`S2_20240528_05VME_4.7pctCloud.tif`

---

## What You’ll Learn

- Working with Earth Engine in Python.
- Exporting and processing multi-band GeoTIFF imagery.
- Calculating NDWI and NDCI.
- Estimating **Chlorophyll-a concentration**.
- Visualizing and mapping contours of algal bloom hotspots.

---

## Notes

- You can adjust the **Area of Interest (AOI)** and **date range** in the notebook.
- Make sure the selected image has **low cloud cover** (default is <10%).
- This notebook uses **Sentinel-2 Level-2A Surface Reflectance** product:  
  [`COPERNICUS/S2_SR_HARMONIZED`](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED)

---

## Reference

Mishra, S., & Mishra, D. R. (2012). Normalized difference chlorophyll index: A novel model for remote estimation of chlorophyll-a concentration in turbid productive waters. *Remote Sensing of Environment*, 117, 394–406. https://doi.org/10.1016/j.rse.2011.10.016

---

## Bonus Tips

- To improve visualization, adjust the `chl_thresh` percentile in the notebook.
- You may also adapt this workflow to **other aquatic environments** or **other seasons**.

---
