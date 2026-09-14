# Spatial Vulnerability and Emergency Response Modeling for Flood-Impacted Districts in Upper Assam

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Google Earth Engine](https://img.shields.io/badge/Google%20Earth%20Engine-SAR%20Analysis-green.svg)](https://earthengine.google.com/)
[![QGIS](https://img.shields.io/badge/QGIS-v3.14-blue.svg)](https://qgis.org/)

## Project Summary
This study addresses critical road network disruptions and rural community isolation caused by severe monsoon inundation during the 2026 Upper Assam floods across the Jorhat, Sivasagar, and Charaideo districts. 

Using Sentinel-1 Synthetic Aperture Radar (SAR) imagery in Google Earth Engine alongside OpenStreetMap infrastructure vectors in QGIS, the spatial analysis pipeline evaluates flood impacts through persistent monsoon cloud cover. The framework delineates surface flood extents, identifies submerged road links, and pinpoints isolated villages and cut-off healthcare facilities. Furthermore, unflooded educational facilities are identified outside risk zones to directly guide disaster response routing, emergency medical aid, and shelter staging.

---

## Methodology
The methodology combines radar-derived flood change detection with vector network analysis:

```mermaid
graph TD;
    A[Sentinel-1 SAR Data Acquisition] --> B[Dual-Thresholding Change Detection in GEE];
    B --> C[Flood Surface Water Polygons];
    D[OpenStreetMap Infrastructure Vectors] --> E[Spatial Intersect Analysis in QGIS];
    C --> E;
    E --> F[Submerged Road Link Identification];
    E --> G[2km Proximity Buffering for Isolated Villages & Healthcare];
    E --> H[Unflooded Educational Shelter Screening];

![image alt](https://github.com/Mykemccoy/ASSAM-FLOODS-PROJECT-2026/blob/a79b17e56e0c55259af0cd951b9a3672721ebe44/study_area.png)
