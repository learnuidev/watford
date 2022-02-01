<h1 id="top" align="center"> Edd Webster Watford Data Science Submission </h1>

This repository is the code and analysis submitted by [Edd Webster](https://twitter.com/eddwebster) for the [Watford Data Scientist](https://www.watfordfc.com/news/club/careers-data-scientist-first-team) technical challenge.

<p align="center">
  <a href="https://statsbomb.com/"><img src="img/club_badges/premier_league/watford_fc_logo_small.png" alt="Watford F.C." width="10%" style="vertical-align:middle"></a>
  <a href="https://www.uefa.com/uefaeuro-2020/"><img src="img/logos/second_spectrum_logo.jpeg" alt="Second Spectrum" width="45%" style="vertical-align:middle"></a>
  <a href="https://www.uefa.com/uefaeuro-2020/"><img src="img/logos/opta_sports_logo_small.png" alt="Opta" width="20%" style="vertical-align:middle"></a>
</p>

[![Personal Website Badge](https://img.shields.io/badge/eddwebster.com-019FD9?style=flat&logo=web&logoColor=white)](https://www.eddwebster.com/)
[![Email Badge](https://img.shields.io/badge/-Gmail-D14836?style=flat&logo=gmail&logoColor=white)](mailto:edd.j.webster@gmail.com)
[![Twitter Badge](https://img.shields.io/badge/Twitter-1DA1F2?style=flat&logo=twitter&logoColor=white)](https://twitter.com/eddwebster)
[![LinkedIn Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/eddwebster)
[![GitHub Badge](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/eddwebster)
[![Tableau Badge](https://img.shields.io/badge/Tableau-E97627?style=flat&logo=tableau&logoColor=white)](https://public.tableau.com/profile/edd.webster)
![Visitors](https://visitor-badge.glitch.me/badge?page_id=eddwebster.watford)

Check out my <a href="https://github.com/eddwebster/football_analytics" target="_blank">`football_analytics`</a> GitHub repo for the full collection of football analytics projects, data, and analysis that I have created.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- TABLE OF CONTENTS -->
<h2 id="table-of-contents"> :book: Table of Contents</h2>

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#table-of-contents">Table of Contents</a></li>
    <li><a href="#prerequisites">Prerequisites</a></li>
    <li><a href="#repository-structure">Repository Structure</a></li>
    <li><a href="#notebooks">Notebooks</a></li>
    <li><a href="#data-sources">Data Sources</a></li>
    <li><a href="#references">References</a></li>
  </ol>
</details>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- PREREQUISITES -->
<h2 id="prerequisites"> :fork_and_knife: Prerequisites</h2>

![Python Badge](https://img.shields.io/badge/-python-3f7dae?style=flat&logo=python&logoColor=fff)
[![Jupyter Badge](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=flat&logo=Jupyter)](https://jupyter.org/try)


<!--This project is written in Python programming language. <br>-->
The code in this repository uses the following libraries:

*    [NumPy](https://numpy.org/doc/stable/contents.html)
*    [pandas](http://pandas.pydata.org/)
*    [matplotlib](https://matplotlib.org/contents.html?v=20200411155018)
*    [Seaborn](https://seaborn.pydata.org/)
*    [SciPy](https://www.scipy.org/)

<a href="#table-of-contents">Back to Contents</a>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- REPOSITORY STRUCTURE -->
<h2 id="repository-structure"> :cactus: Repository Structure</h2>

The contents of this GitHub repository is organised as the following:

    watford github repository
    │
    ├── data
    │   │
    │   ├── opta
    │   │   ├── raw
    │   │   │   │
    │   │   │   ├── F7
    │   │   │   │   ├── srml-8-2021-f2210324-matchresults-players.csv
    │   │   │   │   ├── srml-8-2021-f2210324-matchresults-bookings.csv
    │   │   │   │   ├── srml-8-2021-f2210334-matchresults-bookings.csv
    │   │   │   │   ├── srml-8-2021-f2210324-matchresults-goals.csv
    │   │   │   │   ├── srml-8-2021-f2210324-matchresults-gamedata.csv
    │   │   │   │   ├── srml-8-2021-f2210334-matchresults-gamedata.csv
    │   │   │   │   ├── srml-8-2021-f2210334-matchresults-goals.csv
    │   │   │   │   ├── srml-8-2021-f2210334-matchresults-players.csv
    │   │   │   │   ├── srml-8-2021-f2210324-matchresults.xml
    │   │   │   │   └── srml-8-2021-f2210334-matchresults.xml
    │   │   │   │   
    │   │   │   └── F24
    │   │   │       ├── f24-8-2021-2210324-eventdetails.csv
    │   │   │       ├── f24-8-2021-2210324-eventdetails.xml
    │   │   │       ├── f24-8-2021-2210334-eventdetails.csv
    │   │   │       └── f24-8-2021-2210334-eventdetails.xml
    │   │   │
    │   │   ├── epl_shots_data.csv
    │   │   │
    │   │   ├── engineered
    │   │   │   │
    │   │   │   ├── F7
    │   │   │   │   ├── srml-8-2021-f2210324-matchresults-players.csv
    │   │   │   │   ├── srml-8-2021-f2210324-matchresults-bookings.csv
    │   │   │   │   ├── srml-8-2021-f2210334-matchresults-bookings.csv
    │   │   │   │   ├── srml-8-2021-f2210324-matchresults-goals.csv
    │   │   │   │   ├── srml-8-2021-f2210324-matchresults-gamedata.csv
    │   │   │   │   ├── srml-8-2021-f2210334-matchresults-gamedata.csv
    │   │   │   │   ├── srml-8-2021-f2210334-matchresults-goals.csv
    │   │   │   │   ├── srml-8-2021-f2210334-matchresults-players.csv
    │   │   │   │   ├── srml-8-2021-f2210324-matchresults.xml
    │   │   │   │   └── srml-8-2021-f2210334-matchresults.xml
    │   │   │   │   
    │   │   │   └── F24
    │   │   │       ├── f24-8-2021-2210324-eventdetails.csv
    │   │   │       ├── f24-8-2021-2210324-eventdetails.xml
    │   │   │       ├── f24-8-2021-2210334-eventdetails.csv
    │   │   │       └── f24-8-2021-2210334-eventdetails.xml
    │   │   │
    │   │   ├── opta_event_types.csv
    │   │   └── opta_qualifier_types.csv
    │   │
    │   ├── second_spectrum
    │   │   ├── raw
    │   │   │   │
    │   │   │   ├── data
    │   │   │   │   ├── g2210324_SecondSpectrum_Metadata_Players.csv
    │   │   │   │   ├── g2210324_SecondSpectrum_Data.jsonl
    │   │   │   │   ├── g2210324_SecondSpectrum_Data.xml
    │   │   │   │   ├── g2210334_SecondSpectrum_Data.csv
    │   │   │   │   ├── g2210334_SecondSpectrum_Data.jsonl
    │   │   │   │   └── g2210334_SecondSpectrum_Data.xml
    │   │   │   │   
    │   │   │   └── metadata
    │   │   │       ├── g2210324_SecondSpectrum_Metadata_Players.csv
    │   │   │       ├── g2210324_SecondSpectrum_Metadata.json
    │   │   │       ├── g2210324_SecondSpectrum_Metadata.xml
    │   │   │       ├── g2210334_SecondSpectrum_Metadata_Players.csv
    │   │   │       ├── g2210334_SecondSpectrum_Metadata.json
    │   │   │       └── g2210334_SecondSpectrum_Metadata.xml
    │   │   │
    │   │   └── engineered
    │   │       │
    │   │       ├── data
    │   │       │   ├── g2210324_SecondSpectrum_Trackingdata_Away.csv
    │   │       │   ├── g2210324_SecondSpectrum_Trackingdata_Home.csv
    │   │       │   ├── g2210334_SecondSpectrum_Trackingdata_Away.csv
    │   │       │   └── g2210334_SecondSpectrum_Trackingdata_Home.csv
    │   │       │   
    │   │       └── physical
    │   │           ├── physical_report_data_merged.csv
    │   │           ├── physical_report_data_crystal_palace_leicester_city_Home.csv
    │   │           └── physical_report_data_crystal_palace_brighton_and_hove_albion_Home.csv
    │   │
    │   ├── physical
    │   │   │
    │   │   ├── raw
    │   │   │   └── Physical Output.csv
    │   │   │
    │   │   └── engineered
    │   │       ├── Physical Output Pivoted.csv
    │   │       └── Physical Output.csv
    │   │ 
    │   └── reference
    │       │
    │       └── epv
    │           └── EPV_grid.csv
    │
    ├── docs
    │   ├── 1
    │   └── 2
    │
    ├── gif
    │   └── fig
    │
    ├── img
    │   ├── eddwebster
    │   ├── fig
    │   └── logos
    │ 
    ├── notebooks
    │   ├── 1
    │   └── 2
    │
    ├── scripts
    │   └── 1.py
    │
    └── videos
        └── 1


<a href="#table-of-contents">Back to Contents</a>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- NOTEBOOKS -->
<h2 id="notebooks"> :notebook_with_decorative_cover: Notebooks</h2>

For code used to produce the analysis of this technical challenge, see the [`notebooks`](https://github.com/eddwebster/watford/tree/main/notebooks) subfolder, in which the workflow is divided into the following:
*    [Data Parsing]()
*    [Data Engineering]()
*    [Data Modeling]()
*    [Data Analysis]()

<a href="#table-of-contents">Back to Contents</a>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- DATA SOURCES -->
<h2 id="data-sources"> :floppy_disk: Data Sources</h2>

Due to the 100mb file size limitation in GitHub, all datasets used in this analysis have been exported and made publicly available to view and download in Google Drive at the following [[link](https://drive.google.com/drive/folders/1FJLvtQFNUF-SaQc1_VwNsB26cGRplqGf?usp=sharing)]. Some of the files, including the OBV values provided, are available in the [`data`](https://github.com/eddwebster/watford/tree/main/data) folder of this repository.


<a href="#table-of-contents">Back to Contents</a>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- DOCUMENTATION -->
<h2 id="documentation"> :page_facing_up: Documentation</h2>

All documentation saved locally in the [`docs`]() subfolder, including:
*    1
*    2
*    3


<a href="#table-of-contents">Back to Contents</a>
