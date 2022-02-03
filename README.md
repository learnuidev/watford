<h1 id="top" align="center"> Edd Webster Watford Data Science Submission </h1>

This repository is the code and analysis submitted by [Edd Webster](https://twitter.com/eddwebster) for the [Watford Data Scientist](https://www.watfordfc.com/news/club/careers-data-scientist-first-team) technical challenge.

<p align="center">
  <a href="https://statsbomb.com/"><img src="img/club_badges/premier_league/watford_fc_logo_small.png" alt="Watford F.C." width="10%" style="vertical-align:middle"></a>
  <a href="https://www.uefa.com/uefaeuro-2020/"><img src="img/logos/second_spectrum_logo.jpeg" alt="Second Spectrum" width="45%" style="vertical-align:middle"></a>
  <a href="https://www.uefa.com/uefaeuro-2020/"><img src="img/logos/opta_sports_logo_small.png" alt="Opta" width="17.5%" style="vertical-align:middle"></a>
</p>

<p align="center">
  <a href="https://statsbomb.com/"><img src="gif/fig/second_spectrum/combined_pitch_control_video_clip_first_goal_cry_lei_46055_46305.gif" alt="Pitch Control Video" width="50%" style="vertical-align:middle"></a>
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
    <li><a href="#data-visualisation-and-tableau-dashboards">Data Visualisation and Tableau Dashboards</a></li>
    <li><a href="#data-sources">Data Sources</a></li>
    <li><a href="#resources">Resources</a></li>
  </ol>
</details>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- PREREQUISITES -->
<h2 id="prerequisites"> :fork_and_knife: Prerequisites</h2>

![Python Badge](https://img.shields.io/badge/-python-3f7dae?style=flat&logo=python&logoColor=fff)
[![Jupyter Badge](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=flat&logo=Jupyter)](https://jupyter.org/try)


<!--This project is written in Python programming language. <br>-->
The code in this repository uses the following Python libraries:

*    [`NumPy`](https://numpy.org/doc/stable/contents.html) for multidimensional array computing;
*    [`pandas`](http://pandas.pydata.org/) for data analysis and manipulation;
*    [`matplotlib`](https://matplotlib.org/contents.html?v=20200411155018) and [`Seaborn`](https://seaborn.pydata.org/) for data visualisation; and
*    [`scitkit-learn`](https://scikit-learn.org/stable/index.html) and [`SciPy`](https://www.scipy.org/) for Machine Learning.


The following football analytics libraries (Python and R) were also used for the specific use-case of football analytics:
*    [`FCrSTATS`](https://github.com/FCrSTATS/fc.rstats) by [FC rSTATS](https://twitter.com/FC_rstats) - a package with various functions that help people working with OPTA and ChyronHego data, used in this analysis to parse the Opta F7 and F24 data (see [[link](https://github.com/eddwebster/watford/blob/main/notebooks/1_data_parsing/Opta/Parse%20Opta%20F24.R)] (F7) and [[link](https://github.com/eddwebster/watford/blob/main/notebooks/1_data_parsing/Opta/Parse%20Opta%20F24.R)] (F24))
*    [`kloppy`](https://github.com/PySport/kloppy) by [Koen Vossen](https://twitter.com/mr_le_fox) (and contributors) - a Python package for standardising tracking and event data, used in this analysis to parse the Second Spectrum tracking data (see [[link](https://github.com/eddwebster/watford/blob/main/notebooks/2_data_engineering/Second%20Spectrum%20Data%20Engineering.ipynb)])

<a href="#table-of-contents">Back to Contents</a>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- REPOSITORY STRUCTURE -->
<h2 id="repository-structure"> :cactus: Repository Structure</h2>

The contents of this GitHub repository is organised as the following:

    watford github repository
    │
    ├── dashboards
    │   ├── Edd Webster Watford F.C. - Crystal Palace Analysis and Dashboard.twbx
    │   └── Edd Webster Watford F.C. - Physical Data Analysis and Dashboards.twbx
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
    │   └── opta
    │       ├── F24 documentation - Opta Playground.docx
    │       ├── f24_appendices.docx
    │       └── F24_appendices.pdf
    │
    ├── gif
    │   └── fig
    │       └── second_spectrum
    │           ├── pitch_control_clip_first_goal_cry_lei_46055_46305.gif
    │           ├── pitch_control_clip_forth_goal_cry_lei_109630_110030.gif
    │           ├── pitch_control_clip_second_goal_cry_lei_55125_55375.gif
    │           ├── pitch_control_clip_third_goal_cry_lei_93980_94280.gif
    │           ├── tracking_clip_first_goal_cry_lei_46055_46305.gif
    │           ├── tracking_clip_forth_goal_cry_lei_109630_110080.gif
    │           ├── tracking_clip_second_goal_cry_lei_55125_55375.gif
    │           └── tracking_clip_third_goal_cry_lei_93980_94280.gif
    │
    ├── img
    │   │
    │   ├── club_badges
    │   │   └── premier_league
    │   │       ├── brighton_and_hove_albion_fc_logo.png
    │   │       ├── crystal_palace_fc_logo.png
    │   │       ├── leicester_city_fc_logo.png
    │   │       ├── watford_fc_logo_small.png
    │   │       └── watford_fc_logo.png
    │   │
    │   ├── fig
    │   │
    │   ├── logos
    │   │
    │   └── pitches
    │ 
    ├── notebooks
    │   │
    │   ├── 1_data_parsing
    │   │   └── opta
    │   │       ├── Parse Opta F7.R
    │   │       └── Parse Opta F24.R
    │   │
    │   ├── 2_data_engineering
    │   │   ├── Opta Data Engineering.ipynb
    │   │   ├── Physical Data Engineering.ipynb
    │   │   └── Second Spectrum Data Engineering.ipynb
    │   │
    │   ├── 3_data_modeling
    │   │   └── Training of an Expected Goals Model from Opta Event Data.ipynb
    │   │
    │   └── 4_data_analysis
    │       └── Second Spectrum Data Visualisation.ipynb
    │
    ├── models
    │   └── expected_goals_model_lr.sav
    │
    ├── scripts
    │   └── second_spectrum
    │       ├── Second_Spectrum_EPV.py
    │       ├── Second_Spectrum_IO.py
    │       ├── Second_Spectrum_PitchControl.py
    │       ├── Second_Spectrum_Velocities.py
    │       └── Second_Spectrum_Viz.py
    │
    ├── slides
    │   ├── Edd Webster - Watford Football Club Data Science Pack.pptx
    │   └── Edd Webster - Watford Data Task.pptx
    │
    └── videos
            │ 
            ├─── match_highlights
            │    ├── 03102021 - Crystal Palace (2) vs. (2) Leicester City.mp4
            │    └── 27092021 - Crystal Palace (1) vs. (1) Brighton & Hove Albion.mp4
            │   
            └── second_spectrum
                 ├── combined_pitch_control_video_first_goal_cry_lei.mp4
                 ├── combined_pitch_control_video_forth_goal_cry_lei.mp4
                 ├── combined_pitch_control_video_second_goal_cry_lei.mp4
                 ├── combined_pitch_control_video_third_goal_cry_lei.mp4
                 ├── pitch_control_clip_first_goal_cry_lei_46055_46305.mp4
                 ├── pitch_control_clip_forth_goal_cry_lei_109630_110030.mp4
                 ├── pitch_control_clip_second_goal_cry_lei_55125_55375.mp4
                 ├── pitch_control_clip_third_goal_cry_lei_93980_94280.mp4
                 ├── tracking_clip_first_goal_cry_lei_46055_46305.mp4
                 ├── tracking_clip_forth_goal_cry_lei_109630_110080.mp4
                 ├── tracking_clip_second_goal_cry_lei_55125_55375.mp4
                 └── tracking_clip_third_goal_cry_lei_93980_94280.mp4   


<a href="#table-of-contents">Back to Contents</a>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- NOTEBOOKS -->
<h2 id="notebooks"> :notebook_with_decorative_cover: Notebooks</h2>

For code used to produce the analysis of this technical challenge, see the [`notebooks`](https://github.com/eddwebster/watford/tree/main/notebooks) subfolder, in which the workflow is divided into the following:
*    [Data Parsing](https://github.com/eddwebster/watford/tree/main/notebooks/1_data_parsing)
*    [Data Engineering](https://github.com/eddwebster/watford/tree/main/notebooks/2_data_engineering)
*    [Data Modeling](https://github.com/eddwebster/watford/tree/main/notebooks/3_data_modeling)
*    [Data Analysis](https://github.com/eddwebster/watford/tree/main/notebooks/4_data_analysis)

<a href="#table-of-contents">Back to Contents</a>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- DATA VISUALISATION AND TABLEAU DASHBOARDS -->
<h2 id="data-visualisation-and-tableau-dashboards"> :bar_chart: Data Visualisation and Tableau Dashboards</h2>

For Tableau dashboards produced using the data engineered in the notebooks in this repository, please see my Tableau Public profile: [public.tableau.com/profile/edd.webster](https://public.tableau.com/profile/edd.webster).

The two workbooks created for this analysis:
*    [Edd Webster Watford F.C. - Crystal Palace Analysis and Dashboard](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/SquadListDashboard-BarCharts)
*    [Edd Webster Watford F.C. - Physical Data Analysis and Dashboards](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-PhysicalDataAnalysisandDashboards/PhysicalDataAnalysisOff-the-BallTotalDistancePlayerLevelDashboard)

Links to all the individual dashboards, within these two workbooks are:


*Crystal Palace Opposition Analysis:*
*    [Form Guide](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/FormGuideDashboard?publish=yes)
*    [Squad List](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/SquadListDashboard)
*    [xG Analysis Dashboard](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/xGAnalysisDashboard)
*    [Player Chance Creation Analysis](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/PlayerChanceCreationAnalysisDashboard)
*    [Team Chance Creation Analysis](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/TeamChanceCreationAnalysisDashboard)
*    [Average Player Position](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/AveragePlayerPositionDashboard)
*    [xT Analysis](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/xTAnalysisDashboard)
*    [Touch Heat Map](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/TouchMapDashboard)
*    [Passing Network](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/PassingNetworkDashboard)
*    [Passing Analysis](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/PassingAnalysisDashboard)
*    [Formation Analysis](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/FormationAnalysisDashboard)
*    Crystal Palace Physical Reports:
     +    [Total Distance](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/PhysicalReportTotalDistanceDashboard)
     +    [Run Types](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/PhysicalReportRunTypesDashboard)
     +    [Run Types per Minute](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/PhysicalReportRunTypesPerMinuteDashboard)
     +    [Top Speed](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-CrystalPalaceAnalysisandDashboard/PhysicalReportTopSpeedDashboard)

*Physical Data Analysis:*
*    [Player Overview](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-PhysicalDataAnalysisandDashboards/PlayerOverviewDashboard)
*    [Quickest Player](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-PhysicalDataAnalysisandDashboards/QuickestPlayerDashboard)
*    [Player Run Types](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-PhysicalDataAnalysisandDashboards/PhysicalDataAnalysisRunTypesPlayerLevelDashboard)
*    [Player Total Distance](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-PhysicalDataAnalysisandDashboards/PhysicalDataAnalysisTotalDistancePlayerLevelDashboard)
*    [Player High Intensity Distance](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-PhysicalDataAnalysisandDashboards/PhysicalDataAnalysisHighIntensityTotalDistancePlayerLevelDashboard)
*    [Player Off-the-Ball Distance](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-PhysicalDataAnalysisandDashboards/PhysicalDataAnalysisOff-the-BallTotalDistancePlayerLevelDashboard)
*    [Team Total Distance](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-PhysicalDataAnalysisandDashboards/PhysicalDataAnalysisTeamADistancebyMatchDashboard)
*    [Player 5 Min Run Types](https://public.tableau.com/app/profile/edd.webster/viz/EddWebsterWatfordF_C_-PhysicalDataAnalysisandDashboards/PhysicalDataAnalysisTotalDistanceper5MinsTotalDistanceRunTypePlayerLevelDashboard)


<a href="#table-of-contents">Back to Contents</a>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- DATA SOURCES -->
<h2 id="data-sources"> :floppy_disk: Data Sources</h2>

Due to the 100mb file size limitation in GitHub, all datasets used in this analysis have been exported and made publicly available to view and download in Google Drive at the following [[link](https://drive.google.com/drive/folders/1UCQYCijuasphus_XzIRtpN4nZbSWT7Q2?usp=sharing)]. Some of the files are available in the [`data`](https://github.com/eddwebster/watford/tree/main/data) folder of this repository.


<a href="#table-of-contents">Back to Contents</a>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- DOCUMENTATION -->
<h2 id="documentation"> :page_facing_up: Documentation</h2>

All documentation saved locally in the [`docs`](https://github.com/eddwebster/watford/tree/main/docs) subfolder, including:
*    
*    


<a href="#table-of-contents">Back to Contents</a>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png)


<!-- RESOURCES -->
<h2 id="resources"> :page_facing_up: Resources</h2>

Links to resources that helped create this piece of analysis:

### Event Data:
*    [Opta data](https://www.statsperform.com/opta/) by [Stats Perform](https://www.statsperform.com/) data

### Tracking Data:
*    [Second Spectrum](https://www.secondspectrum.com/index.html) data
*    [Laurie Shaw](https://twitter.com/EightyFivePoint)'s Metrica Sports Tracking data series for #FoT - [Introduction](https://www.youtube.com/watch?v=8TrleFklEsE), [Measuring Physical Performance](https://www.youtube.com/watch?v=VX3T-4lB2o0), [Pitch Control modelling](https://www.youtube.com/watch?v=5X1cSehLg6s), and [Valuing Actions](https://www.youtube.com/watch?v=KXSLKwADXKI). See the following for code [[link](https://github.com/Friends-of-Tracking-Data-FoTD/LaurieOnTracking)]
*    Laurie Shaw's Metrica Sports Tracking data series for [Friends of Tracking](https://www.youtube.com/channel/UCUBFJYcag8j2rm_9HkrrA7w) (see the following for code [[link](https://github.com/Friends-of-Tracking-Data-FoTD/LaurieOnTracking)]):
     +    [Introduction](https://www.youtube.com/watch?v=8TrleFklEsE);
     +    [Measuring Physical Performance](https://www.youtube.com/watch?v=VX3T-4lB2o0);
     +    [Pitch Control modelling](https://www.youtube.com/watch?v=5X1cSehLg6s); and
     +    [Valuing Actions](https://www.youtube.com/watch?v=KXSLKwADXKI).
*    [Demystifying Tracking data Sportlogiq webinar](https://www.youtube.com/watch?v=miEWHSTYvX4) by Sam Gregory and Devin Pleuler
*    [Will Spearman's masterclass in Pitch Control](https://www.youtube.com/watch?v=X9PrwPyolyU&list=PL38nJNjpNpH-l59NupDBW7oG7CmWBgp7Y) for Friends of Tracking
*    [How Tracking Data is Used in Football and What are the Future Challenges](https://www.youtube.com/watch?v=kHTq9cwdkGA) with Javier Fernández, Sudarshan 'Suds' Gopaladesikan, Laurie Shaw, Will Spearman and David Sumpter for Friends of Tracking.
*    [Introduction to tracking data in football](https://www.youtube.com/watch?v=fYqEnoOV9Po) by David Sumpter for Friends of Tracking

### Expected Goals Modeling:

#### Tutorials
*    Friends of Tracking YouTube channel [[link](https://www.youtube.com/channel/UCUBFJYcag8j2rm_9HkrrA7w)] and Mathematical Modelling of Football course by Uppsala University [[link](https://uppsala.instructure.com/courses/28112)]. The GitHub repo with all code featured can be found at the following [[link](https://github.com/Friends-of-Tracking-Data-FoTD)]. Lectures of note include:
     +    David Sumpter's Expected Goals webinars for #FoT - [How to Build An Expected Goals Model 1: Data and Model](https://www.youtube.com/watch?v=bpjLyFyLlXs), [How to Build An Expected Goals Model 2: Statistical fitting](https://www.youtube.com/watch?v=wHOgINJ5g54), and [The Ultimate Guide to Expected Goals](https://www.youtube.com/watch?v=310_eW0hUqQ). See the following for code [3xGModel](https://github.com/Friends-of-Tracking-Data-FoTD/SoccermaticsForPython/blob/master/3xGModel.py), [4LinearRegression](https://github.com/Friends-of-Tracking-Data-FoTD/SoccermaticsForPython/blob/master/4LinearRegression.py), [5xGModelFit.py](https://github.com/Friends-of-Tracking-Data-FoTD/SoccermaticsForPython/blob/master/5xGModelFit.py), and [6MeasuresOfFit](https://github.com/Friends-of-Tracking-Data-FoTD/SoccermaticsForPython/blob/master/6MeasuresOfFit.py);
     +    Peter McKeever's ['Good practice in data visualisation'](https://www.youtube.com/watch?v=md0pdsWtq_o) webinar for Friends of Tracking. See the following for code [[link](https://github.com/petermckeeverPerform/friends-of-tracking-viz-lecture)];
*    [Soccer Analytics Handbook](https://github.com/devinpleuler/analytics-handbook) by [Devin Pleuler](https://twitter.com/devinpleuler). See tutorial notebooks (also available in Google Colab) that notably include: [3. Logistic Regression](https://github.com/devinpleuler/analytics-handbook/blob/master/notebooks/logistic_regression.ipynb), and [7. Data Visualization](https://github.com/devinpleuler/analytics-handbook/blob/master/notebooks/data_visualization.ipynb):
*    [FC Python](https://twitter.com/fc_python) tutorials [[link](https://fcpython.com/)];
*    DataViz, Python, and matplotlib tutorials by Peter McKeever [[link](http://petermckeever.com/)] - I think his website is currently in redevelopment, with many of the old tutorials not currently available (28/02/2021). Check out his revamped [How to Draw a Football Pitch](http://petermckeever.com/2020/10/how-to-draw-a-football-pitch/) tutorial;
*    [McKay Johns YouTube channel](https://www.youtube.com/channel/UCmqincDKps3syxvD4hbODSg);
*    [Tech how-to: build your own Expected Goals model](https://www.scisports.com/tech-how-to-build-your-own-expected-goals-model/) by [Jan Van Haaren](https://twitter.com/JanVanHaaren) and [SciSports](https://twitter.com/SciSportsNL).
*    [Fitting your own football xG model](https://www.datofutbol.cl/xg-model/) by [Dato Fútbol](https://twitter.com/DatoFutbol_cl) (Ismael Gómez Schmidt). See GitHub repo [[link](https://github.com/Dato-Futbol/xg-model)];
*    [Python for Fantasy Football series](http://www.fantasyfutopia.com/python-for-fantasy-football-introduction/) by [Fantasy Futopia](https://twitter.com/FantasyFutopia) ([Thomas Whelan](https://twitter.com/tom_whelan)).  See the following posts:
     +    [Introduction to Machine Learning](http://www.fantasyfutopia.com/python-for-fantasy-football-introduction-to-machine-learning/)
     +    [Addressing Class Imbalance in Machine Learning](http://www.fantasyfutopia.com/python-for-fantasy-football-addressing-class-imbalance-in-machine-learning/)
     +    [Addressing Class Imbalance Part 2](http://www.fantasyfutopia.com/python-for-fantasy-football-addressing-class-imbalance-part-2/)
     +    [Understanding Random Forests](http://www.fantasyfutopia.com/python-for-fantasy-football-understanding-random-forests/)
     +    [Feature Engineering for Machine Learning](http://www.fantasyfutopia.com/python-for-fantasy-football-feature-engineering-for-machine-learning/)
*    [Building an Expected Goals Model in Python](https://web.archive.org/web/20200301071559/http://petermckeever.com/2019/01/building-an-expected-goals-model-in-python/) by [Peter McKeever](https://twitter.com/petermckeever) (using WayBackMachine);
*    [An xG Model for Everyone in 20 minutes (ish)](https://differentgame.wordpress.com/2017/04/29/an-xg-model-for-everyone-in-20-minutes-ish/ ) by [Football Fact Man](https://twitter.com/footballfactman) (Paul Riley).
*    [How to Draw a Football Pitch](http://petermckeever.com/2020/10/how-to-draw-a-football-pitch/) by Peter McKeever
*    [How To Create xG Flow Charts in Python](https://www.youtube.com/watch?v=bvoOOYMQkac) by [McKay Johns](https://twitter.com/mckayjohns). For code, see [[link](https://github.com/mckayjohns/Viz-Templates)]

#### Libaries and GitHub Repos
*    [`Friends-of-Tracking-Data-FoTD`](https://github.com/Friends-of-Tracking-Data-FoTD);
*    [`SoccermaticsForPython`](https://github.com/Friends-of-Tracking-Data-FoTD/SoccermaticsForPython) - repo by David Sumpter dedicated for people getting started with Python using the concepts derived from the book Soccermatics;
*    [`LaurieOnTracking`](https://github.com/Friends-of-Tracking-Data-FoTD/LaurieOnTracking) by [Laurie Shaw](https://twitter.com/EightyFivePoint) - Python code for working with Metrica tracking data; and
*    [`Expected Goals Thesis`](https://github.com/andrewRowlinson/expected-goals-thesis) by [Andrew Rowlinson](https://twitter.com/numberstorm). See both his thesis [[link](https://github.com/andrewRowlinson/expected-goals-thesis/blob/master/FOOTBALL%20SHOT%20QUALITY%20-%20Visualizing%20the%20Quality%20of%20Football%20Soccer%20Goals.pdf)] and the following notebooks:
     +    [Explore Data Quality Overlap](https://github.com/andrewRowlinson/expected-goals-thesis/blob/master/notebooks/00-explore-data-quality-overlap.ipynb);
     +    [Expected Goals Model](https://github.com/andrewRowlinson/expected-goals-thesis/blob/master/notebooks/01-expected-goals-model.ipynb);
     +    [Expected Goals Calculate xG and Shap](https://github.com/andrewRowlinson/expected-goals-thesis/blob/master/notebooks/02-expected-goals-calculate-xg-and-shap.ipynb);
     +    [Visualise Models](https://github.com/andrewRowlinson/expected-goals-thesis/blob/master/notebooks/03-visualize-models.ipynb);
     +    [kernel Density Probability Scoring](https://github.com/andrewRowlinson/expected-goals-thesis/blob/master/notebooks/04-kernel-density-probability-scoring.ipynb);
     +    [Simulate Match Results from xG](https://github.com/andrewRowlinson/expected-goals-thesis/blob/master/notebooks/05-simulate-match-results-from-xg.ipynb);
     +    [Freeze Frame Examples](https://github.com/andrewRowlinson/expected-goals-thesis/blob/master/notebooks/06-freeze_frame-example.ipynb);
     +    [Red Zone Heatmap](https://github.com/andrewRowlinson/expected-goals-thesis/blob/master/notebooks/07-red-zone-heatmap.ipynb);
     +    [Shots Follow Poisson Distribution](https://github.com/andrewRowlinson/expected-goals-thesis/blob/master/notebooks/08-shots_follow_poisson_distribution.ipynb); and
     +    [Angle Features](https://github.com/andrewRowlinson/expected-goals-thesis/blob/master/notebooks/09_figure3_angle_features.ipynb).
*    [`expected_goals_deep_dive`](https://github.com/andrewsimplebet/expected_goals_deep_dive) by [Andrew Puopolo](https://twitter.com/andrew_puopolo). See the following notebooks:
     +    [Setting Our Data Up](https://github.com/andrewsimplebet/expected_goals_deep_dive/blob/master/0.%20Setting%20Our%20Data%20Up.ipynb)
     +    [Random Forest Cross Validation And Hyperparameter Tuning](https://github.com/andrewsimplebet/expected_goals_deep_dive/blob/master/1.%20Random%20Forest%20Cross%20Validation%20And%20Hyperparameter%20Tuning.ipynb)
     +    [Comparing Logistic Regression and Random Forest For Expected Goals](https://github.com/andrewsimplebet/expected_goals_deep_dive/blob/master/2.%20Basic%20Logistic%20Regression%20and%20Comparison%20To%20Random%20Forests.ipynb)
     +    [Calibrating Expected Goals Models](https://github.com/andrewsimplebet/expected_goals_deep_dive/blob/master/3.%20Calibrating%20Expected%20Goals%20Models.ipynb)
     +    [Sanity Checking Our Expected Goals Model and Final Thoughts](https://github.com/andrewsimplebet/expected_goals_deep_dive/blob/master/4.%20Sanity%20Checking%20Our%20Expected%20Goals%20Models%20And%20Final%20Thoughts.ipynb)
*    [`soccer_analytics`](https://github.com/CleKraus/soccer_analytics) by [Kraus Clemens](https://twitter.com/CleKraus). See the following notebooks:
     +    [Expected goal model with logistic regression](https://github.com/CleKraus/soccer_analytics/blob/master/notebooks/expected_goal_model_lr.ipynb)
     +    [Challenges using gradient boosters](https://github.com/CleKraus/soccer_analytics/blob/master/notebooks/challenges_with_gradient_boosters.ipynb)
*    [`xg-model`](https://github.com/Dato-Futbol/xg-model)] by [Dato Fútbol](https://twitter.com/DatoFutbol_cl) (Ismael Gómez Schmidt)
*    [`soccer-xg`](https://pypi.org/project/soccer-xg/) by [Jesse Davis](https://twitter.com/jessejdavis1) and [Pieter Robberechts](https://twitter.com/p_robberechts) - a Python package for training and analyzing expected goals (xG) models in soccer (not used this this assignment but referenced here); and
*    [`Google Research Football`](https://github.com/google-research/football). See the Kaggle Competition alongside Manchester City [[link](https://www.kaggle.com/c/google-football) (ended October 2020).

#### Written Pieces

##### Papers
*    [Football Shot Quality: Visualising the Quality of Soccer/Football Shots](https://github.com/andrewRowlinson/expected-goals-thesis/blob/master/FOOTBALL%20SHOT%20QUALITY%20-%20Visualizing%20the%20Quality%20of%20Football%20Soccer%20Goals.pdf) by [Andrew Rowlinson](https://twitter.com/numberstorm). See his GitHub repo for code [[link](https://github.com/andrewRowlinson/expected-goals-thesis)]; and
*    [“Quality vs Quantity”: Improved Shot Prediction in Soccer using Strategic Features from Spatiotemporal Data](https://s3-us-west-1.amazonaws.com/disneyresearch/wp-content/uploads/20150308192147/Quality-vs-Quantity%E2%80%9D-Improved-Shot-Prediction-in-Soccer-using-Strategic-Features-from-Spatiotemporal-Data-Paper.pdf) (2015) by Patrick Lucey, Alina Bialkowski, Mathew Monfort, Peter Carr, and Iain Matthews; and

##### Blogs
*    [Sam Green](https://twitter.com/aSamGreen)'s [xG model](https://www.optasportspro.com/news-analysis/assessing-the-performance-of-premier-league-goalscorers/);
*    [Michael Caley](https://twitter.com/MC_of_A)'s [xG model](https://cartilagefreecaptain.sbnation.com/2014/9/11/6131661/premier-league-projections-2014#methoderology);
*    [Using Data to Analyse Team Formations](https://eightyfivepoints.blogspot.com/2019/11/using-data-to-analyse-team-formations.html) by [Laurie Shaw](https://twitter.com/EightyFivePoint);
*    [Structure in football: putting formations into context](https://eightyfivepoints.blogspot.com/2020/12/structure-in-football-putting.html) by [Laurie Shaw](https://twitter.com/EightyFivePoint);
*    [xG explained](https://fbref.com/en/expected-goals-model-explained/) by [FBref](https://twitter.com/fbref);
*    [What are expected Goals?](https://www.americansocceranalysis.com/explanation) by [American Soccer Analysis](https://twitter.com/AnalysisEvolved);
*    [How StatsBomb Data Helps Measure Counter-Pressing](https://statsbomb.com/2018/05/how-statsbomb-data-helps-measure-counter-pressing/) - used to determine 5-yard radius
*    [David Sumpter](https://twitter.com/Soccermatics)'s Expected Goals pieces:
     +    [Should you write about real goals or expected goals? A guide for journalists](https://soccermatics.medium.com/should-you-write-about-real-goals-or-expected-goals-a-guide-for-journalists-2cf0c7ec6bb6);
     +    [Football’s magical equation?](https://soccermatics.medium.com/footballs-magical-equation-bfe212ce7d4a)
     +    [The Geometry of Shooting](https://soccermatics.medium.com/the-geometry-of-shooting-ae7a67fdf760).
*    [Michael Caley](https://twitter.com/MC_of_A)'s Expected Goals pieces:
     +    [Shot Matrix I: Shot Location and Expected Goals](https://cartilagefreecaptain.sbnation.com/2013/11/13/5098186/shot-matrix-i-shot-location-and-expected-goals)
     +    [Let's talk about expected goals](https://cartilagefreecaptain.sbnation.com/2015/4/10/8381071/football-statistics-expected-goals-michael-caley-deadspin)
*    [Jesse Davis](https://twitter.com/jessejdavis1) and [Pieter Robberechts](https://twitter.com/p_robberechts)' Expected Goals pieces for KU Leuven;
     +    [How Data Avilability Affects the Ability to learn Good xG Models](https://dtai.cs.kuleuven.be/sports/blog/how-data-availability-affects-the-ability-to-learn-good-xg-models)
     +    [Illustrating the Interplay between Features and Models in xG](https://dtai.cs.kuleuven.be/sports/blog/illustrating-the-interplay-between-features-and-models-in-xg)
     +    [How Data Quality Affects xG](https://dtai.cs.kuleuven.be/sports/blog/how-data-quality-affects-xg)
*    [Will Gürpinar-Morgan](https://twitter.com/WillTGM)'s Expected Goals pieces:
     +    [Unexpected goals](https://2plus2equals11.com/2015/12/31/unexpected-goals/) on [2+2=11](https://2plus2equals11.com/);
     +    [Great Expectations](https://2plus2equals11.com/2015/05/31/great-expectations/) on [2+2=11](https://2plus2equals11.com/);
     +    [On single match expected goal totals](https://2plus2equals11.com/2015/12/16/on-single-match-expected-goal-totals/) on [2+2=11](https://2plus2equals11.com/);
     +    [How StatsBomb Data Helps Measure Counter-Pressing](https://statsbomb.com/2018/05/how-statsbomb-data-helps-measure-counter-pressing/) for StatsBomb
*    [Martin Eastwoood](https://twitter.com/penaltyblog) (Pena.lt/y)'s Expected Goals pieces [[link](https://pena.lt/y/category/expected-goals.html)];
     +    [Expected Goals For All.](https://pena.lt/y/2014/02/12/expected-goals-for-all)
     +    [Actual Goals Versus Expected Goals](https://pena.lt/y/2014/02/15/actual-goals-versus-expected-goals);
     +    [Expected Goals Updated](https://pena.lt/y/2014/03/01/expected-goals-updated);
     +    [Expected Goals: The Y Axis](https://pena.lt/y/2014/04/16/expected-goals-the-y-xis);
     +    [Expected Goals And Exponential Decay](https://pena.lt/y/2014/04/22/expected-goals-and-exponential-decay);
     +    [Expected Goals: Foot Shots Versus Headers](https://pena.lt/y/2014/08/28/expected-goals-foot-shots-versus-headers);
     +    [Expected Goals And Support Vector Machines](https://pena.lt/y/2015/07/13/expected-goals-svm);
     +    [Expected Goals and Uncertainty](https://pena.lt/y/2016/04/29/expected-goals-and-uncertainty); and
     +    [Sharing xG Using Multi-touch Attribution Modelling](https://pena.lt/y/2019/11/23/multitouch-attributed-xg).
*    [Garry Gelade](https://twitter.com/GarryGelade)'s Expected Goals pieces:
     +    [Expected Goals and Unexpected Goals](https://web.archive.org/web/20200724125157/http://business-analytic.co.uk/blog/expected-goals-and-unexpected-goals/) (using WayBackMachine);
     +    [Assessing Expected Goals Models. Part 1: Shots](https://web.archive.org/web/20200724125157/http://business-analytic.co.uk/blog/evaluating-expected-goals-models/) (using WayBackMachine);
     +    [Assessing Expected Goals Models. Part 2: Anatomy of a Big Chance](https://web.archive.org/web/20200724125157/http://business-analytic.co.uk/blog/assessing-expected-goals-models-part-2-anatomy-of-a-big-chance/) (using WayBackMachine);
*    [Introducing xGChain and xGBuildup](https://statsbomb.com/2018/08/introducing-xgchain-and-xgbuildup/) by [Thom Lawrence](https://twitter.com/lemonwatcher);
*    [Quantifying finishing skill](https://statsbomb.com/2017/07/quantifying-finishing-skill/) by [Marek Kwiatkowski](https://twitter.com/statlurker);
*    [The Dual Life of Expected Goals (Part 1)](https://statsbomb.com/2018/05/the-dual-life-of-expected-goals-part-1/) by [Mike L. Goodman](https://twitter.com/TheM_L_G);
*    [A close look at my new Expected Goals Model](https://web.archive.org/web/20200320193539/http://11tegen11.net/2015/08/14/a-close-look-at-my-new-expected-goals-model/) by by [11tegen](https://twitter.com/11tegen11) ([Sander IJtsma](https://twitter.com/IJtsma)] (using WayBackMachine);
*    [An analysis of different expected goals models](https://www.pinnacle.com/en/betting-articles/Soccer/expected-goals-model-analysis/MEP2N9VMG5CTW99D) by [Benjamin Cronin](https://twitter.com/PinnacleBen);
*    [Expected Goals 3.0 Methodology](https://www.americansocceranalysis.com/home/2015/4/14/expected-goals-methodology) by [Matthias Kullowatz](https://twitter.com/mattyanselmo);
*    [Explaining and Training Shot Quality](https://statsbomb.com/2016/04/explaining-and-training-shot-quality/) by [Ted Knutson](https://twitter.com/mixedknuts);
*    [A simple Expected Goals model](https://cricketsavant.wordpress.com/2017/01/21/a-simple-expected-goals-model/) by Cricket Savant;
*    [How we calculate Expected Goals (xG)](https://www.fantasyfootballfix.com/blog-index/how-we-calculate-expected-goals-xg/) by Fantasy Football Fix; and
*    [Una mirada al Soccer Analytics usando R — Parte III](https://medium.com/datos-y-ciencia/una-mirada-al-soccer-analytics-usando-r-parte-iii-3bdff9cd3752) by [Dato Fútbol](https://twitter.com/DatoFutbol_cl) (Ismael Gómez Schmidt).
*    [StatsBomb](https://statsbomb.com/)'s latest 360 release [[link](https://statsbomb.com/2021/02/statsbomb-360-and-evolve/)]
*    [Impect](https://www.impect.com/en/about-us)'s 'Packing' metric [[link](https://www.youtube.com/watch?v=fk8yAQU9U1E&ab_channel=IMPECT)].

#### Videos
For a YouTube playlist of videos collated around the topics of Expected Goals, see [[link](https://www.youtube.com/playlist?list=PL38nJNjpNpH_VPRZJrkaPZOJfyuIaZHUY)]. For a Tracking data in Football specific playlist, see [[link](https://www.youtube.com/playlist?list=PL38nJNjpNpH-UX0YVNu7oN5gAWQc2hq8F)].

*    Laurie Shaw's Metrica Sports Tracking data series for [Friends of Tracking](https://www.youtube.com/channel/UCUBFJYcag8j2rm_9HkrrA7w) (see the following for code [[link](https://github.com/Friends-of-Tracking-Data-FoTD/LaurieOnTracking)]):
     +    [Introduction](https://www.youtube.com/watch?v=8TrleFklEsE);
     +    [Measuring Physical Performance](https://www.youtube.com/watch?v=VX3T-4lB2o0);
     +    [Pitch Control modelling](https://www.youtube.com/watch?v=5X1cSehLg6s); and
     +    [Valuing Actions](https://www.youtube.com/watch?v=KXSLKwADXKI).
*    [Demystifying Tracking data Sportlogiq webinar](https://www.youtube.com/watch?v=miEWHSTYvX4) by Sam Gregory and Devin Pleuler;
*    [Will Spearman's masterclass in Pitch Control](https://www.youtube.com/watch?v=X9PrwPyolyU&list=PL38nJNjpNpH-l59NupDBW7oG7CmWBgp7Y) for Friends of Tracking;
*    [How Tracking Data is Used in Football and What are the Future Challenges](https://www.youtube.com/watch?v=kHTq9cwdkGA) with Javier Fernández, Sudarshan 'Suds' Gopaladesikan, Laurie Shaw, Will Spearman and David Sumpter for Friends of Tracking.
*    [Introduction to tracking data in football](https://www.youtube.com/watch?v=fYqEnoOV9Po) by David Sumpter for Friends of Tracking;
*    [Learning to Watch Football: Self-Supervised Representations](https://vimeo.com/398489039/80d8dcfb58) for Tracking Data by Karun Singh. See accompanying blog post [[link](https://karun.in/blog/ssr-tracking-data.html)];
*    David Sumpter's Expected Goals webinars for [Friends of Tracking](https://www.youtube.com/channel/UCUBFJYcag8j2rm_9HkrrA7w) (see the following for code [3xGModel](https://github.com/Friends-of-Tracking-Data-FoTD/SoccermaticsForPython/blob/master/3xGModel.py), [4LinearRegression](https://github.com/Friends-of-Tracking-Data-FoTD/SoccermaticsForPython/blob/master/4LinearRegression.py), [5xGModelFit.py](https://github.com/Friends-of-Tracking-Data-FoTD/SoccermaticsForPython/blob/master/5xGModelFit.py), and [6MeasuresOfFit](https://github.com/Friends-of-Tracking-Data-FoTD/SoccermaticsForPython/blob/master/6MeasuresOfFit.py)):
     +    [How to Build An Expected Goals Model 1: Data and Model](https://www.youtube.com/watch?v=bpjLyFyLlXs);
     +    [How to Build An Expected Goals Model 2: Statistical fitting](https://www.youtube.com/watch?v=wHOgINJ5g54); and
     +    [The Ultimate Guide to Expected Goals](https://www.youtube.com/watch?v=310_eW0hUqQ).
*    ['Good practice in data visualisation'](https://www.youtube.com/watch?v=md0pdsWtq_o) webinar by Peter McKeever for Friends Of Tracking. See the following for code [[link](https://github.com/petermckeeverPerform/friends-of-tracking-viz-lecture)];
*    [The Ultimate Guide to Expected Goals](https://www.youtube.com/watch?v=310_eW0hUqQ) David Sumpter for Friends of Tracking;
*    [How to explain Expected Goals to a football player](https://www.youtube.com/watch?v=Xc6IG9-Dt18) by David Sumpter;
*    [What is xG?](https://www.youtube.com/watch?v=zSaeaFcm1SY) by [Tifo Football](https://www.youtube.com/channel/UCGYYNGmyhZ_kwBF_lqqXdAQ);
*    [Opta Expected Goals](https://www.youtube.com/watch?v=w7zPZsLGK18) by [The Analyst](https://www.youtube.com/user/optasports) (formally Opta);
*    [What are Expected Goals?](https://www.youtube.com/watch?v=Xc6IG9-Dt18) by [David Sumpter](https://twitter.com/Soccermatics) and Axel Pershagen;
*    [Anatomy of a Goal](https://www.youtube.com/watch?v=YJuHC7xXsGA) by [Numberphile](https://twitter.com/numberphile) [Brady Haran](https://twitter.com/BradyHaran));
*    [Sam Green OptaPro Interview](https://www.youtube.com/watch?v=gHIY-MgDh_o);
*    [How Did These Goals Go In? - We Explain How Goal Probability Works](https://www.youtube.com/watch?v=_vGhocyvKhA) by the Bundesliga;
*    [Soccer Analytics: Expected Goals](https://www.youtube.com/watch?v=3rsDCxszCD0) by [Dan Altman](https://twitter.com/NYAsports); and
*    [Anatomy of an Expected Goal](https://www.youtube.com/watch?v=mgHIx0LSrqM) by [11tegen](https://twitter.com/11tegen11) ([Sander IJtsma](https://twitter.com/IJtsma));
*    [Anatomy of a Goal (with Sam Green)](https://www.youtube.com/watch?v=YJuHC7xXsGA) by Numberphile: 
*    ["Is Our Model Learning What We Think It Is?" Estimating the xG Impact of Actions in Football](https://www.youtube.com/watch?v=i7Ra4Qv4_m4) by [Tom Decroos](https://twitter.com/TomDecroos) from the 2019 StatsBomb Innovation in Football Conference;
*    [Statsbomb Data Launch - Beyond Naive xG](https://www.youtube.com/watch?v=_AYY9XlWEB0) by [Ted Knutson](https://twitter.com/mixedknuts)

#### Podcasts 
List of notable episodes:
*    [The Football Fanalytics Podcast](https://open.spotify.com/show/6JwWRPMaHfGicFBtl7nI3V?si=IwQ00tyTRPaBcW-0XLwS4w&nd=1)
     +   [#1: What Did You Expect?](https://open.spotify.com/episode/3CkvTYcsLmNmD5BCIZhpvi?si=NaeVt2zOStm9EJ56n4EozQ)
*    [Tifo Podcast](https://open.spotify.com/show/06QIGhqK31Qw1UvfHzRIDA?si=eJzpmtMeSPWUDP9fQ-5pqA):
     +    The Future of Stats: xG, xA - [Spotify](https://open.spotify.com/episode/7fPpKZSt2o9SSNynayROwd)

#### Tweets
*    The benefits of including fake data in an Expected Goals model by David Sumpter [[link](https://twitter.com/Soccermatics/status/1260598182624575490)].


### Expected Threat (xT) Modeling:
*    [Introducing Expected Threat (xT)](https://karun.in/blog/expected-threat.html) by [Karun Singh](https://twitter.com/karun1710). Check out also as an unrolled Twitter thread [[link](https://threadreaderapp.com/thread/1361695899131387909.html)] Karun's Twitter thread for the many resources out there around this topic, including: [Episode 19 of The Football Fanalytics Podcast](https://open.spotify.com/episode/0HvcNPxg8Ux6zJB2nGp3VK?si=AOkxcH3KTue4jeEIA6kpWw&nd=1), Karun's StatsBomb conference presentation [[link](https://www.youtube.com/watch?v=mE3sUVCIwfA)] and slides [[link](https://docs.google.com/presentation/d/1tu603CdONhI17AZTrd3mdf1UAf7k-rHwwCLSU_tCx6g/edit#slide=id.p)], [Rob Hickman](https://twitter.com/robwhickman)'s StatsBomb conference presentation where he extended xT to take defensive risk into account [[link](https://twitter.com/robwhickman)], [Last Row View](https://twitter.com/lastrowview) ([Ricardo Tavares](https://twitter.com/rjtavares))'s blog post for evaluating off-the-ball player movements by combining xT and tracking data, and Karun's xT values as a 12x8 grid to download as a JSON file [[link](https://t.co/IoZdCa2BbX?amp=1)].
*    [Football's New Stat - What is Expected Threat?](https://www.youtube.com/watch?v=RwVLUH4BFfA) by Tifo


### Pitch Control Modeling:

#### Tutorials
*    [Pitch Control modelling](https://www.youtube.com/watch?v=5X1cSehLg6s) and [Valuing Actions](https://www.youtube.com/watch?v=KXSLKwADXKI) tutorials by [Laurie Shaw](https://twitter.com/EightyFivePoint) as part of his Metrica Sports Tracking data series for [Friends of Tracking](https://www.youtube.com/channel/UCUBFJYcag8j2rm_9HkrrA7w). See the following for code [[link](https://github.com/Friends-of-Tracking-Data-FoTD/LaurieOnTracking)];

#### GitHub Repositories

*    [`Metrica-pitch-control`](https://github.com/anenglishgoat/Metrica-pitch-control) by [Will Thompson](https://twitter.com/AnEnglishGoat) - a Python implementation of [Javier Fernández](https://twitter.com/JaviOnData) and [Luke Bornn](https://twitter.com/LukeBornn)'s Pitch Control model from their paper [Wide Open Spaces: A statistical technique for measuring space creation in professional soccer](https://www.researchgate.net/publication/324942294_Wide_Open_Spaces_A_statistical_technique_for_measuring_space_creation_in_professional_soccer) (2018) and [Will Spearman](https://twitter.com/the_spearman)'s Pitch Control model from his paper [Beyond Expected Goals](https://www.researchgate.net/profile/William_Spearman/publication/327139841_Beyond_Expected_Goals/links/5b7c3023a6fdcc5f8b5932f7/Beyond-Expected-Goals.pdf) (2018). The respectively Google Colab notebooks are available  [[link](https://colab.research.google.com/drive/18HcpBywUTKpgxxwrkx15g6skrWuKBQB7?usp=sharing)] and [[link](https://colab.research.google.com/drive/1GPjXYEmDHxE6GPHNS3nN3mAjWRFEd-Z_?usp=sharing)];

#### Written Pieces

*    [Everything you need to know about 'pitch control'](https://get-goalside.letterdrop.com/p/everything-you-need-to-know-about-pitch-control) by [Mark Thompson](https://twitter.com/EveryTeam_Mark);
*    [A Framework for the Fine-Grained Evaluation of the Instantaneous Expected Value of Soccer Possessions](https://arxiv.org/abs/2011.09426) (2020) by Javier Fernández, Luke Bornn and Daniel Cervone;
*    [Decomposing the Immeasurable Sport: A deep learning expected possession value framework for soccer](https://www.semanticscholar.org/paper/Decomposing-the-Immeasurable-Sport%3A-A-deep-learning-Fern%C3%A1ndez/fc78b144a531a8ffdf3216a677f3a65e70dad3c7) (2019) by [Javier Fernández](https://twitter.com/JaviOnData), [Bornn](https://twitter.com/LukeBornn), and [Dan Cervone](https://twitter.com/dcervone0). Accompanying talks - [SSAC19](https://www.youtube.com/watch?v=JIa7Td3YXxI), [StatsBomb conference](https://www.youtube.com/watch?v=nfPEEbKJbpM);
*    [Beyond Expected Goals](https://www.researchgate.net/profile/William_Spearman/publication/327139841_Beyond_Expected_Goals/links/5b7c3023a6fdcc5f8b5932f7/Beyond-Expected-Goals.pdf) (2018) by [Will Spearman](https://twitter.com/the_spearman);
*    [Replaying the NBA](http://www.lukebornn.com/papers/sandholtz_ssac_2018.pdf) (2018) by Luke Bornn
*    [Wide Open Spaces: A statistical technique for measuring space creation in professional soccer](https://www.researchgate.net/publication/324942294_Wide_Open_Spaces_A_statistical_technique_for_measuring_space_creation_in_professional_soccer) (2018) by [Javier Fernandez](https://twitter.com/JaviOnData) and [Luke Bornn](https://twitter.com/LukeBornn);
*    [Physics-Based	Modeling	of Pass	Probabilities	in	Soccer](https://www.researchgate.net/publication/315166647_Physics-Based_Modeling_of_Pass_Probabilities_in_Soccer) (2017) by [Will Spearman](https://twitter.com/the_spearman), Austin Basye, Greg Dick, Ryan Hotovy, and Paul Pop;


### Data Science

#### Logistic Regression
*    [scikit-learn Logistic Regression official docs](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
*    [Logistic Regression wiki](https://en.wikipedia.org/wiki/Logistic_regression#:~:text=Logistic%20regression%20is%20a%20statistical,a%20form%20of%20binary%20regression)
*    [Logistic Regression](https://www.youtube.com/watch?v=yIYKR4sgzI8) by StatQuest (Josh Starmer)
*    [Logistic Regression for Machine Learning](https://machinelearningmastery.com/logistic-regression-for-machine-learning/) by Jason Brownlee
*    [Logistic Regression Tutorial for Machine Learning](https://machinelearningmastery.com/logistic-regression-tutorial-for-machine-learning/) by Jason Brownlee


### Visualisation
*    [How to Make a Plot with Two Different Y-axis in Python with Matplotlib](https://cmdlinetips.com/2019/10/how-to-make-a-plot-with-two-different-y-axis-in-python-with-matplotlib/)
*    https://stackoverflow.com/questions/39409866/correlation-heatmap
*    [Control color in seaborn heatmaps](https://www.python-graph-gallery.com/92-control-color-in-seaborn-heatmaps)

<a href="#table-of-contents">Back to Contents</a>

