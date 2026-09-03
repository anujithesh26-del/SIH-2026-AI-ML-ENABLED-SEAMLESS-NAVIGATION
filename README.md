# SIH-2026-AI-ML-ENABLED-SEAMLESS-NAVIGATION
# seamless navigation sensor sanity test

This Python script offers a streamlined approach to analyzing time-series sensor data exported from the Physics Toolbox application. It automates crucial steps from data ingestion to visualization and integrity checks, making it an invaluable tool for anyone working with Physics Toolbox recordings.

## Purpose

To help researchers, students, and enthusiasts quickly understand, validate, and visualize their Physics Toolbox sensor data, identifying potential issues like data dropouts or recording gaps.

## Key Features

-   **CSV Upload & Parsing**: Easily upload Physics Toolbox CSV files and correctly parse their unique format.
-   **Time-Series Processing**: Converts raw timestamps into elapsed seconds for consistent analysis.
-   **Sampling Rate Validation**: Estimates the actual sampling rate and detects significant gaps in the recording.
-   **Sensor Data Visualization**: Generates plots for accelerometer and gyroscope data over time.
-   **Data Integrity Checks**: Verifies raw g-force magnitudes and identifies hidden recording gaps due to app backgrounding.
-   **GPS Speed Analysis**: Visualizes GPS speed data, distinguishing between valid readings and 'no fix' instances.
-   **Event Correlation**: Provides functionality to overlay custom event markers on plots for easy correlation with experiment logs.

## How to Use

1.  Run the notebook in Google Colab.
2.  Upload your Physics Toolbox CSV file when prompted.
3.  The script will automatically perform the analysis, display key statistics, and generate plots.
4.  Optionally, modify the `event_start` and `event_end` variables in the `run_analysis` function to mark specific events from your test log.
