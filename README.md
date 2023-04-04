Readme for MATLAB Script: ROI Analysis for MSI Data

This MATLAB script is used for analyzing regions of interest (ROI) in multispectral imaging (MSI) data, specifically for oxygen saturation (SO2) maps. The script imports data, processes it, and calculates summary statistics for selected regions of interest.
Features

    Import and process data for ROI selection
    Calculate oxygen saturation (SO2) per pixel and process the data for contour plotting
    Draw or load mask for ROI selection and obtain summary statistics
    Analyze ROI according to distance from anatomical landmarks
    Data fitting using Curve Fitter app

Usage

    Import the data and process it to allow the selection of ROI
    Position the ROI to allow identification of the trend line using the Curve Fitter app
    Record the data in a specific Excel file

Dependencies

    MATLAB R2019a or later
    Curve Fitting Toolbox

Data Import

    Load a baseline .mat file, which includes total hemoglobin (THb) and oxyhemoglobin (HbO2) to obtain the SO2 maps
    Load a pre-selected mask that should be present in the corresponding analysis folder

Data Processing

    Calculate O2 saturation per pixel and exclude unreliable pixels with a low CoD
    Fill missing NaN values with 0 using imputation of the mean of nearest values
    Convert SO2_processed into a grayscale image for segmentation

ROI Analysis

    Draw or load mask and obtain summary statistics from the masks
    Aggregate summary statistics (mean, mode, max, min, and standard deviation) for each ROI
    Plot main contour and mask results side by side

Region of Interest Analysis According to Distance from Anatomical Landmarks

    Crop the region of interest and rotate the matrix to place the X-axis perpendicular to the desired anatomical landmark
    Regional data fitting using the Curve Fitter app

Notes

    Most tasks will only work on ROI1
    The script uses the Curve Fitter app for data fitting, which is not shown in the script directly
    Ensure that the input file paths are updated according to your specific file locations
