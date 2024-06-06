# Sentinel-1 Land Cover Classification with Google Earth Engine

Dear Alam Sher Sir,

I am writing to inform you that I have uploaded two scripts for the land cover classification of the Lakki Marwat district using Google Earth Engine (GEE). Below are the details of the two scripts:

# Script with Shapefile from GEE Asset:

This script utilizes a shapefile of the Lakki Marwat boundary, which has been uploaded to the GEE asset.
The script imports this shapefile to define the Area of Interest (AOI) and proceeds with the Sentinel-1 image processing and land cover classification.
The shapefile provides precise boundary details, ensuring accurate analysis within the defined AOI.

# Script with Coordinates to Cover Entire District:

This script defines the AOI using a bounding box with coordinates, covering the entire Lakki Marwat district.
The coordinates have been adjusted to ensure the whole district is included in the analysis.
This approach eliminates the need for a shapefile and allows for direct execution using specified coordinates.
Both scripts perform similar image processing and land cover classification tasks using Sentinel-1 data and a Random Forest classifier. The main difference lies in how the AOI is defined—either through a shapefile or coordinates.

Please review the scripts and let me know if there are any adjustments or further actions required.
Thank you for your guidance and support.

Best regards,

Muhammad Tashfeen 
Roll No 22

The script performs the following steps:

1. **Load the Area of Interest (AOI)**: The AOI is imported from an existing GEE asset.
2. **Filter Sentinel-1 Data**: Sentinel-1 SAR imagery is filtered for the AOI and a specified date range. Both ascending and descending orbit data are used.
3. **Create a Composite Image**: A composite image is created by calculating the mean values of VH and VV polarizations from ascending and descending orbits.
4. **Define Land Cover Classes**: Sample points for different land cover classes (water, forest, barren, and urban) are defined.
5. **Merge Sample Points**: Sample points are merged into a single FeatureCollection.
6. **Sample Regions**: The composite image is sampled at the locations of the land cover classes.
7. **Split Data**: The data is split into training and validation sets.
8. **Train Classifier**: A Random Forest classifier is trained using the training set.
9. **Classify Image**: The composite image is classified into the defined land cover classes.
10. **Evaluate Classifier**: The classifier's accuracy is evaluated using a confusion matrix.
11. **Export Classified Image**: The classified image is exported to Google Drive.
