# Vegetation Highlighting and Timelapse Analysis Using the Copernicus Data Space Browser
## NDVI-Based Green City Script and Multi-Year Greenness Assessment

## 1. Introduction

This repository documents a workflow conducted in the Copernicus Data Space Browser to visualise vegetation patterns and analyse multi-year greenness dynamics. The work applies a custom NDVI-based script (the “Green City Script”) and uses Sentinel-2 L2A imagery to highlight vegetated areas and produce a timelapse animation showing seasonal change.

The workflow demonstrates how simple custom scripts and time-series exploration tools within the browser can support rapid environmental assessment.

## 2. Green City Script

The Green City Script, originally created by Carlos Bentes, is designed to emphasise vegetation by computing the Normalized Difference Vegetation Index (NDVI) and recolouring high-NDVI pixels. The process is summarised as follows, based on the description in the project report :contentReference[oaicite:1]{index=1}:

- NDVI is calculated using Sentinel-2 near-infrared (B08) and red (B04) bands.  
- A vegetation threshold of **NDVI ≥ 0.4** is applied.  
- The underlying image is first transformed into a grayscale representation using weighted RGB values.  
- Pixels meeting the NDVI threshold are recoloured in green, while all other areas remain grayscale.  

This produces an output where vegetation stands out clearly relative to built-up areas, bare soil, and infrastructure.

The script included in the report (page 2) computes NDVI, applies the threshold, and recolours vegetation accordingly.

## 3. Workflow in the Copernicus Data Space Browser

### 3.1 Logging into the Browser

The workflow begins by accessing the Copernicus Data Space Browser and navigating to the search interface where satellite scenes can be queried 

### 3.2 Date Selection and True-Colour Layer

A date range is selected, and a Sentinel-2 L2A true-colour image is added to the map for context . This forms the base layer against which the outputs of the custom script can be compared.

### 3.3 Running the Custom Script

The Green City Script is pasted into the custom script editor  and executed.  
The browser processes the script and displays the NDVI-highlighted vegetation map.

### 3.4 Final Output

The resulting visualization shows the grayscale background with bright green vegetation areas. This provides a clear delineation of vegetated surfaces within the selected AOI.

## 4. Timelapse Greenness Analysis (2018–2025)

To evaluate longer-term vegetation change, a timelapse animation was created within the browser’s time-series tool 

The configuration used:

- Years: **2018–2025**  
- Month selected: **October**  
- Imagery: Sentinel-2 L2A  
- One image per year, filtered by cloud cover  

The timelapse visually demonstrates how greenness varies across the selected years, supporting environmental monitoring and temporal analysis.

## 5. Applications and Relevance

This workflow illustrates how NDVI-based visualization and time-series analysis can be applied to:

- Vegetation mapping  
- Urban greenness assessment  
- Seasonal and interannual change detection  
- Preliminary environmental reporting  
- Introductory Earth observation analysis for teaching or demonstration

The approach is computationally lightweight and requires no external coding environment beyond the browser interface.

## 6. Script Reference

The Green City Script by Carlos Bentes

Script can be accessed here- https://custom-scripts.sentinel-hub.com/custom-scripts/sentinel-2/green_city/

