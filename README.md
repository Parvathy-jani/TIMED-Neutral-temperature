# TIMED-Neutral-temperature
Kinetic Temperature Data Processing

Overview
This project involves parsing, processing, and analyzing kinetic temperature data from multiple .txt files containing measurements from a satellite instrument.
The data is processed for specific latitude and longitude ranges and at a fixed altitude of 110 km. The final output consists of daily average kinetic temperature values, which are saved into CSV files for further analysis.
The project is structured into four main Python scripts, each handling specific tasks related to reading the data, processing it, and saving the results.
1. File Parsing and Data Extraction (TIMED_L2A_SABER_1269291.txt)
Purpose:

This script reads the file TIMED_L2A_SABER_1269291.txt to extract key data such as time, altitude, latitude, longitude, kinetic temperature, and tangent altitude. The data is filtered by latitude and longitude range and processed for measurements at an altitude of 110 km.
Key Steps:

    File Reading: Opens and reads the .txt file line by line.
    Data Parsing: Extracts time, altitude, latitude, longitude, kinetic temperature, and tangent altitude from the lines.
    Kinetic Temperature Filtering: Extracts the kinetic temperature at the specified tangent altitude (110 km) using a helper function.
    Latitude/Longitude Filtering: Filters the data based on the specified geographic bounds.
    Date Grouping: Groups the filtered data by date and calculates daily average kinetic temperatures.
    Output: Saves the resulting daily average kinetic temperature to a CSV file.

Output:

    A CSV file containing the date and average kinetic temperature at 110 km.

2. File Parsing and Data Extraction (TIMED_L2A_SABER_1316450.txt)
Purpose:

This script performs the same data extraction and processing as the first script but for a different file: TIMED_L2A_SABER_1316450.txt.
Key Steps:

    File Reading: Opens and reads the .txt file line by line.
    Data Parsing: Extracts data (time, altitude, latitude, longitude, kinetic temperature, and tangent altitude).
    Kinetic Temperature Filtering: Extracts the kinetic temperature at the 110 km altitude.
    Latitude/Longitude Filtering: Filters the data based on the geographic bounds.
    Date Grouping: Groups the data by date and calculates the daily average kinetic temperature.
    Output: Saves the daily average kinetic temperature to a CSV file.

Output:

    A CSV file with the date and average kinetic temperature at 110 km.

3. File Parsing and Data Extraction (TIMED_L2A_SABER_1316144.txt)
Purpose:

Similar to the first two scripts, this script reads and processes data from the TIMED_L2A_SABER_1316144.txt file. It performs the same tasks: reading, parsing, filtering, and extracting kinetic temperatures at 110 km for the specified latitude and longitude ranges.
Key Steps:

    File Reading: Opens the .txt file and reads each line.
    Data Parsing: Extracts time, altitude, latitude, longitude, kinetic temperature, and tangent altitude.
    Kinetic Temperature Filtering: Extracts the temperature at the specified 110 km altitude.
    Latitude/Longitude Filtering: Filters the data based on geographic bounds.
    Date Grouping: Groups the data by date and calculates the daily average kinetic temperature.
    Output: Saves the resulting data to a CSV file.

Output:

    A CSV file containing the date and average kinetic temperature at 110 km.

4. Data Aggregation and Plotting
Purpose:

This script is used to aggregate the data from the three previously generated CSV files and plot the daily average kinetic temperatures for each of the specified months (December, January, February).
Key Steps:

    Loading CSV Files: Loads the three CSV files generated from the previous scripts.
    Data Concatenation: Combines the data from the three CSV files into a single DataFrame.
    Plotting: Plots the daily average kinetic temperature over the period covered by the three CSV files.
    Display: The resulting plot is displayed for visual inspection.

Output:

    A plot showing the daily average kinetic temperature at 110 km for the combined data from December 2009, January 2010, and February 2010.

    Requirements

    Python: Python 3.x
    Libraries:
        pandas: For data manipulation and analysis.
        numpy: For numerical operations.
        matplotlib: For plotting the results.

        How to Run the Scripts

    Ensure that you have all the necessary data files: The .txt files and output CSV files must be in the correct directory as described in the directory structure.
    Run the scripts:
        First, run the scripts that parse and process the data (TIMED_L2A_SABER_1269291.txt, TIMED_L2A_SABER_1316450.txt, TIMED_L2A_SABER_1316144.txt).
        Then, run the script for data aggregation and plotting.
    Check the outputs: The daily average kinetic temperature CSV files will be saved in the directory, and a final plot will be displayed and saved.

Conclusion

This project processes kinetic temperature data from satellite measurements, filters it based on geographic location and altitude, and computes daily average temperatures at 110 km.
The results are saved into CSV files for each month, and a final plot provides a visual representation of the temperature trends over time.
