# CityMapPOIs
City grids and POI crawling for data visualization.

## Usage
### 1.Instal Matplotlib 3.1.3
Install numpy
### 2.Building footprint
osmnx.geometries module
Download geospatial entities’ geometries and attributes from OpenStreetMap.
Retrieve points of interest, building footprints, or any other objects from OSM, including their geometries and attribute data, and construct a GeoDataFrame of them.

https://osmnx.readthedocs.io/en/stable/osmnx.html#osmnx.geometries.geometries_from_place

5 methods：
osmnx.geometries.geometries_from_address(address, tags, dist=1000)
osmnx.geometries.geometries_from_bbox(north, south, east, west, tags)
osmnx.geometries.geometries_from_place(query, tags, which_result=None, buffer_dist=None)
osmnx.geometries.geometries_from_point(center_point, tags, dist=1000)
osmnx.geometries.geometries_from_polygon(polygon, tags)
tags
tags = {"building": True} would return all building footprints in the area
tags = {"amenity":True, "landuse":["retail","commercial"], "highway":"bus_stop"} would return all amenities, landuse=retail, landuse=commercial, and highway=bus_stop.

### 3.Points of interest (POI)
Points-of-interest
OpenStreetMap POI features
https://wiki.openstreetmap.org/wiki/Map_features

Amenity
Used to map facilities used by visitors and residents. For example: toilets, telephones, banks, pharmacies, cafes, parking and schools. See the page Amenities for an introduction on its usage.

Sustenance
Education
Transportation
Financial
Healthcare
Entertainment, Arts & Culture
Public Service
Facilities
Waste Management
Others

### 5.draw the boundary of Bronx
area_name = "南沙区, 广州, 中国" area, edges = ox.geocode_to_gdf(area_name) area.plot()
