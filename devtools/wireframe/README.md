# wireframe

## Introduction
This directory contains:
* the Excel spreadsheets used to calculate the SVG geometry for the schematic representation ("wireframe") of various limited-access routes
* HTML pages, with embedded JavaScript code, to generate visualizations of "wireframes" produced from these spreadsheets.

## Development Process
1. Calculate the geometry of the SVG <line> elements to represent the schematic geometry of the route in question using the first tab of the relevant Excel workbook
2. Copy and "paste as values" the results of (1) into another tab in the workbook
3. Export (2) as a CSV file
4. Use generate_wirefarme_vertical.html or generate_wireframe_horizontal.html (depending upon whether the route is oriented NB-SB or EB-WB) to produce a visualization of the wireframe in a web browser
5. Use (4) to "sanity check" the rendered schematic geometry, and make changes as needed.
6. Repeat the process until the "sanity check" passes.
  
Once an SVG geometry has been created that passes muster, one must then join the CSV "wireframe" data for a given {route, direction} pair to the relevant balanced volume data in CSV format. See the __devtools/ipynb__ directory of this repository for a sample Jupyter notebook to do this. The resulting CSV files are the actual input to the balanced volume application.
  
# Dependencies
The two HTML files depend upon the user providing access to the d3.js and underscore.js libraries. Some editing of the HTML to adjust the paths to these libraries in your installation may be needed.
