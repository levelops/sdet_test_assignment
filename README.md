
#### python 3 online compiler
- https://www.programiz.com/python-programming/online-compiler/

#### test data: Climate Data Online
- https://www.ncdc.noaa.gov/cdo-web/webservices/v2

#### request token
- DQCquPdcBMIQkhKhjjVffHTlYMauvmRH

1. Create a wrapper function for `/datasets` endppoint based on given documentation.
   - https://www.ncdc.noaa.gov/cdo-web/webservices/v2#datasets
   - All of the CDO data are in datasets. The containing dataset must be known before attempting to access its data.
   - example data: dataset returns a dictionary:
     {"metadata": {"resultset":{"offset":1, "count": 11, "limit": 25}}, "results": [{'uid': 'gov.noaa.ncdc:C00861', 'mindate': '1763-01-01', 'maxdate': '2021-06-20', 'name': 'Daily Summaries', 'datacoverage': 1, 'id': 'GHCND'}]}
2. Create a wrapper function for `/stations` endpoint based on given documentation.
   - Stations are where the data comes from (for most datasets) and can be considered the smallest granual of location data. If the desired station is known, all of its data can quickly be viewed
   - https://www.ncdc.noaa.gov/cdo-web/webservices/v2#stations
   - example data: stations returns adictionary:
     {"metadata": {"resultset": {"offset": 5001, "count": 9833, "limit": 1}}, "results": [{'elevation': 267.6, 'mindate': '2010-01-01', 'maxdate': '2010-01-01', 'latitude': 44.8418, 'name': 'MALONE, NY US', 'datacoverage': 1, 'id': 'GHCND:USC00304996', 'elevationUnit': 'METERS', 'longitude': -74.306}]}
3. Create a wrapper function for `/data` endpoint based on given documentation.
   - https://www.ncdc.noaa.gov/cdo-web/webservices/v2#data
   - example data: data returns a dictionary
     {'metadata': {'resultset': {'offset': 1, 'count': 473, 'limit': 1}}, 'results': [{'date': '2010-01-01T00:00:00', 'datatype': 'ANN-CLDD-BASE45', 'station': 'GHCND:USC00304996', 'attributes': 'S', 'value': 2787}]}

