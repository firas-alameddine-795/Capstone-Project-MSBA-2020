# Capstone-Project-MSBA-2020
This is my official project I submitted to otbain my second degree in Business Analystics in 2020. <br>
It is split in two parts: a python script to clean and process the Lebanese trade data between 2011 and 2019, and a dash app to show the output of the first part as a dashboard. Packages used are pandas, numpy, seaborn, re, plotly.express, plotly.graph_objects, dash, dash-daq, dash-core-components, dash-html-components, dash-bootstrap-components and jupyter-dash. More details are explained as follows: 

### Part One:
Publicly available data about monthly imports and exports in Lebanon was downloaded, cleaned, processed and wrangled to created a data frame of records that is consistent with what the World Customs Organization (WCO) shows. I break down the work as follows:

1. Data Preparation:
   * Concatenate 9 files, considering proper renaming of columns.
   * Melt the data frame. Imports and exports are now stacked row wise, and a binary column called "trade flow" is added.
2. Data Cleaning:
   * Remove punctuations from harmonized codes for commodities.
   * Match harmonized codes written by Lebanese Authorities with those written by WCO to have consistent.
3. Data Enrichment:
   * Determine higher levels of the harmonized codes (4 levels of hierarchy: HS1, HS@, HS4 and HS6)
   * Match the newly found HS1, HS2 and HS4 codes with their proper titles and descriptions, also publicly available and provided by WCO.
   * Add regions and/or continents information by country.
 4. Data Validation: treat missing values

### Part Two:
After cleaning this data, it is time to create the dash app. Dash, developed by Plotly, allows you to create interactive, web-ready data visualizations with just Python. A basic dash app consists of two main components: the layout and the callback, and they are built using a combination of Python, Dash's core components and HTML components. The layout represents what the app looks like, and callbacks are the interactive part of the app (actions on the web app when clicking, scrolling and/or hovering etc.).

A Tableau version of this dash app is provided in another repository.
