# osm-street-extractor
Small Python script to create keywords out of the streets within selected boundary in Open Street Map.

## requirements
```bash
pip3 install -r requirements.txt
```

## usage
```bash
./osm-street-extractor -h
```

### print streets line by line
Pass `--osm-box` flag with (south,west,north,east) a.k.a (latitude_min,longitude_min,latitude_max,longitude_max) values:
```bash
./osm-street-extractor --osm-box '52.20110,20.97937,52.20682,20.98462'  # some square in Warsaw, Poland
```

### make keywords (works for Polish only)
```bash
./osm-street-extractor --osm-box 'a,b,c,d' --format keyword
```

### works with OSM poly:
https://wiki.openstreetmap.org/wiki/Overpass_API/Language_Guide#Select_region_by_polygon
```bash
./osm-street-extractor --osm-polygon 'a,b,c,d,e,f'
```

## hints
### how to get box boundary:
1. Go to https://www.openstreetmap.org
2. Click 'Export', then 'Manually select a different data'

### how to write OSM query:
https://wiki.openstreetmap.org/wiki/Overpass_API/Language_Guide
