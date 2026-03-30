# MorphEO

Personal repository of MorphEO project.

---

## Contents

- [Study Areas](#study-areas)
  - [🇮🇸 Iceland](#-iceland)
- [WP1](#wp1)
  - [WP1.3 Reference data collection](#wp13-reference-data-collection)
  - [Vector data cube for evolving features](#vector-data-cube-for-evolving-features)
  - [OBIA lake outlines](#obia-lake-outlines)
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

## Scripts

---

### WP1.3 Reference data collection

MorphEO_WP1.3.ipynb located in the scripts folder.

### Vector data cube for evolving features

Python translation of the [original computational notebook](https://github.com/loreabad6/vdc-space-time-feats/blob/main/notebook/vdc-showcase.md) created by Lorena Abad.
Located in the scripts folder.

### OBIA lake outlines

Script to create lake outlines of the Jökulsárlón glacial lake based on the method by [Dabiri et al 2021](moz-extension://bc18e54e-46b5-47f8-9750-d48b8835d745/enhanced-reader.html?openApp&pdf=https%3A%2F%2Faustriaca.at%2F0xc1aa5576%25200x003c9b50.pdf)

