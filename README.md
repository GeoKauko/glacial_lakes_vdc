# MorphEO

Personal repository of MorphEO project.

---

## Contents

- [Study Areas](#study-areas)
  - [🇮🇸 Iceland](#-iceland)
- [Workflow](#workflow)  
- [Scripts](#scripts)
- [Data](#data)

---

## Study Areas

---

### 🇮🇸 Iceland

#### Fagradalsfjall Lava Flow

##### Datasets

- [Fagradalsfjall DEMs, ortho, and lava outlines](https://zenodo.org/records/7871187) -> DEMs, 5 aerial surveys (Aug 2022), 1 satellite survey (Aug 2022), 1 aerial survey of eruption sites (Sep 2022), and lava area outlines for the August 2022 eruption at Fagradalsfjall
- [Fagradalsfjall DEMs, ortho, GCPs, video, time-lapse](https://arizona.figshare.com/collections/Fagradalsfjall_Iceland_Eruption/6175633/4) -> DEMs and UAV orthophotos, Ground control point locations, UAS nadir video of lava flow, Time-lapse image sequences of the eruption
- [ÍslandsDEM útgáfa 1.0](https://gatt.lmi.is/geonetwork/srv/eng/catalog.search#/metadata/e6712430-a63c-4ae5-9158-c89d16da6361) -> Iceland DEM
- [ArcticDEM](https://fridge.pgc.umn.edu/) -> DEM covering the Arctic, including Iceland
- [Fagradalsfjall eruption photogrammetry](https://sketchfab.com/natturufraedistofnun/collections/fagradalsfjall-volcanic-eruption-3911d686287848f9b2cb4d04d2fbba22) -> 3D models of the eruption
- [Fagradalsfjall UAV 2021](https://arizona.figshare.com/articles/dataset/Fagradalsfjall_Iceland_2021_Eruption_Unoccupied_Aircraft_Systems_UAS_Data_Surveys/21071140?backTo=/collections/Fagradalsfjall_Iceland_Eruption/6175633) -> UAV orthomosaics and DEMs (2021)
- [VERITAS UAV surveys](https://arizona.figshare.com/articles/dataset/VERITAS_Unoccupied_Aircraft_System_UAS_Surveys/26035837?backTo=/collections/Fagradalsfjall_Iceland_Eruption/6175633) -> Survey locations include the 2021 Fagradalsfjall lava flow-field
- [Fagradalsfjall UAV 2024](https://arizona.figshare.com/articles/dataset/Photogrammetry_Experiment_at_Fagradalsfjall_Iceland/26741719?backTo=/collections/Fagradalsfjall_Iceland_Eruption/6175633) -> UAV orthomosaic, DEMs, pointcloud, and original UAV images (2024)

##### References

- [Lava Flow Mapping Using Sentinel-1 SAR Data at the Fagradalsfjall Volcano, Iceland](https://www.researchgate.net/publication/376628001_Lava_Flow_Mapping_Using_Sentinel-1_SAR_Data_at_the_Fagradalsfjall_Volcano_Iceland)

---

#### Jökulsárlón Glacial Lake

##### Datasets

- [Jökulsárlón lake outlines over time](https://islenskirjoklar.is/#/page/map) -> Glacier web portal visualizes lake outlines (1890-2025)
- [HMA glacial lake inventory](https://nsidc.org/data/hma_gli/versions/1) -> High Mountain Asia Near-Global Multi-Decadal Glacial Lake Inventory, V1 (1990-2018)
- [ÍslandsDEM útgáfa 1.0](https://gatt.lmi.is/geonetwork/srv/eng/catalog.search#/metadata/e6712430-a63c-4ae5-9158-c89d16da6361) -> Iceland DEM
- [ArcticDEM](https://fridge.pgc.umn.edu/) -> DEM covering the Arctic, including Iceland
- [Historical aerial archive](https://loftmyndasja.gis.is/mapview/?application=loftmyndasja) -> Historical aerial survey archive. Includes images of the lake from 1980-1994

##### References

- [Proglacial lake development and outburst flood hazard at Fjallsjökull glacier, southeast Iceland](https://nhess.copernicus.org/articles/25/1913/2025/)

---

## Workflow

---

1. Detect glacial lake outlines from Sentinel-1 and Sentinel-2 data (2016-2025) using OBIA
2. Detect glacial lake outlines from Landsat data (1985-2015) using OBIA
3. Build a vector data cube using the glacial lake outlines

---

## Scripts

The contents of the scripts folder including scripts and environment.

---

### [`1_OBIA_lakes_S1S2.ipynb`](1_OBIA_lakes_S1S2.ipynb): Glacial Lake Mapping with Sentinel-1 and Sentinel-2 (2016–2025)

Script to create lake outlines of the Jökulsárlón glacial lake (2016-2025) based on the method by [Dabiri et al 2021](moz-extension://bc18e54e-46b5-47f8-9750-d48b8835d745/enhanced-reader.html?openApp&pdf=https%3A%2F%2Faustriaca.at%2F0xc1aa5576%25200x003c9b50.pdf). The script uses Sentinel-1 and Sentinel-2.

### [`2_OBIA_lakes_LS.ipynb`](2_OBIA_lakes_LS.ipynb): Glacial Lake Mapping with Landsat via Google Earth Engine (1985–2015)

Script to create lake outlines of the Jökulsárlón glacial lake (1985-2015) based on the method by [Dabiri et al 2021](moz-extension://bc18e54e-46b5-47f8-9750-d48b8835d745/enhanced-reader.html?openApp&pdf=https%3A%2F%2Faustriaca.at%2F0xc1aa5576%25200x003c9b50.pdf). The script uses Landsat 5-8 and ArcticDEM V4.

### [`3_glacial_lakes_VDC_comparisons.ipynb`](3_glacial_lakes_VDC_comparisons.ipynb): Glacial Lake Vector Data Cube Construction, Feature Grouping and Summary Geometries

Notebook to create a vector data cube with the glacial lake outlines obtained with OBIA.

### [`4_glacial_lakes_VDC_querying.ipynb`](4_glacial_lakes_VDC_querying.ipynb)

Loading the created VDC and using it for querying and zonal statistics.

### [`MorphEO_WP1.3.ipynb`](MorphEO_WP1.3.ipynb): Trial Script

**not important**
A script from the beginning of the project.

### [`VDC_py.ipynb`](VDC_py.ipynb): Vector data cube for evolving features

Python translation of the [original computational notebook](https://github.com/loreabad6/vdc-space-time-feats/blob/main/notebook/vdc-showcase.md) created by Lorena Abad.

### [`xvec_intro.ipynb`](xvec_intro.ipynb): Getting to know xvec package

### [`zonal_st.ipynb`](zonal_st.ipynb): Computing zonal statistics on xvec

---

## Data

Preliminary data required for the scripts, and their output data (large files such as outlines and TIFs are not loaded here)

---

## Setup

### 1. Install the environment
```bash
conda env create -f env.yaml
```

### 2. Activate the environment
```bash
conda activate glacial_lakes
```

### 3. Register as a Jupyter kernel
```bash
python -m ipykernel install --user --name glacial_lakes --display-name "glacial_lakes"
```

### 4. Configure local paths
Copy the template and set your local project root:
```bash
cp config_template.py config.py
```
Then open `config.py` and set `ROOT_DIR` to your local project path.

### 5. Run the notebooks in order
> **Important:** Manually review the lake outlines produced by notebooks 1 and 2 before running notebook 3.

---
