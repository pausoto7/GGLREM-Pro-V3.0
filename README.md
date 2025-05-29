# Geomorphic Grade Line (GGL) Tool – Relative Elevation Model Workflow

This repository provides instructions for generating **detrended river corridor maps** using the **Geomorphic Grade Line (GGL) tool**, a powerful method for creating relative elevation models (REMs) from digital elevation models (DEMs) to support stream and floodplain restoration planning and design.

Originally developed by **Matt Helstab and Paul Powers**, this tool helps identify areas of channel incision, floodplain reconnection opportunities, and suitable locations for process-based restoration (e.g., Stage-0 design, beaver dam analogues).

---

## Requirements

- **ArcGIS Pro** with Spatial Analyst extension  
- GGLREM Pro toolbox (Helstab & Hornby, 2024)  
- Basic knowledge of:
  - ArcGIS Pro (Catalog, Toolbox, Editor tools)
  - Microsoft Excel
- **System**:
  - 6+ GB RAM
  - 4-core CPU
  - 4 GB graphics memory
  - 32+ GB free disk space

---

## Input Data

- High-resolution **DEM** (preferably LiDAR-derived) clipped to the river corridor
- Clean DEMs: remove outliers/negatives, especially for tidal areas

---

## Workflow Summary

1. **Set up directories**:
   - Create a project folder, geodatabase, and import DEM

2. **Step 1 – Create Centerline**:
   - Use `Create a Centerline Feature Class` tool
   - Digitize centerline approximating the floodplain center
   - Set `RouteID` (e.g., `Tranquille_Fan`) and save

3. **Step 2 – Cross-Sections**:
   - Use `Create Cross-Sections and Routed Centerline`
   - Define spacing and buffer
   - Outputs: Routed centerline and cross-sections

4. **Step 3 – GGL Table**:
   - Use `Create GGL Table and Centerline Stations`
   - Outputs: CSV with fitted elevation data for REM development

5. **Step 4 – Generate REM**:
   - Open output CSV and follow instructions to build REM using provided tools

---

## Applications

- Identify channel incision
- Stage-0 restoration design
- Map historical floodplain habitat
- Locate floodplain reconnection opportunities
- Plan low-tech restoration (e.g., BDAs, PALS)
- Develop final grading designs

---

## 📜 Credits

Developed by **Matt Helstab** and **Paul Powers**  
Source code and documentation: [GGLREM GitHub Repository](https://github.com/helstab/GGLREM)

---