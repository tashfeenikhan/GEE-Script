# Sentinel-1 Land Cover Classification with Google Earth Engine

This repository contains a script to classify land cover types in the Lakki Marwat region using Sentinel-1 SAR imagery and a Random Forest classifier in Google Earth Engine (GEE).

## Description

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

## Usage

1. **Setup Google Earth Engine**: Ensure you have a Google Earth Engine account and the necessary permissions to access the required assets.

2. **Import the Script**: Copy the script into the GEE code editor or use the provided link to access it directly:
   [GEE Script](https://code.earthengine.google.com/?scriptPath=users%2Fbehzadsk12%2Fbehzad_sk%3ASentinel_1_Classification)

3. **Run the Script**: Execute the script in the GEE code editor.

4. **Modify Sample Points**: Adjust the sample points for land cover classes to better match your ground truth data if necessary.

5. **Export Results**: The classified image will be exported to your Google Drive.

## Notes

- Adjust the sample points for the land cover classes to match your specific study area and ground truth data.
- Ensure you have the necessary permissions to access the GEE assets and to export images to your Google Drive.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
