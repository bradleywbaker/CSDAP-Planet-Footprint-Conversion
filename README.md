# Converting Planet Labs Data Footprints for DESIS Tasking 

## Description
This script converts Area of Interest (AOI) footprints from Planet Labs data ordered each month through CSDAP into usable DESIS tasking regions.  The idea is that it may prove valuable to task DESIS for data that has similar AOIs as data ordered from Planet Labs. This script takes a CSV file that contains Planet geoJSON_geometry and converts it to GeoPandas geometry to determine polygons, area (km2), maximum latitude and longitude, and minimum latitude and longitude for DESIS tasking.

## Required Libraries
pandas, GeoPandas, shapely 

## Running the Script
1. Download the monthly NASA Planet Labs Mirror CSV file. 
2. Run the script.
3. The script will first prompt to enter the CSV file name.
4. User will next be prompted to enter the year (e.g., xxxx) of the mirrored data. This will be included in the output file name.
5. User will then be prompted to enter the month (e.g., xx) of the mirrored data. This will be included in the output file name.
6. The script will output a CSV file.

## Examples
1. User downloads the following Planet Labs monthly data order CSV file to convert for DESIS tasking: "NASA_Mirror_2020_06NASA.csv." Enter the following command:
'python planet_aoi_conversion.py'
2. User will be prompted with: "Please enter the CSV file name including the extension:"
In this case, the user will enter "NASA_Mirror_2020_06.csv"
3. User will be prompted with "Please enter the year that the data was mirrored in the following format yyyy:"
In this case, the user will enter "2020."  The year must be entered as a four-digit year or the script will invoke an error. 
4. User will be prompted with "Please enter the month that the data was mirrored in the following format mm:
In this case, the user will enter "06" for June. The month must be entered as two digits or the script will invoke an error. 


