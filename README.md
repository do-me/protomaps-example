# Protomaps Example
Simple Leaflet example for Protomaps with custom bbox.

## Tutorial

### 1 Download a pmtiles file
Either get a world file or use a bounding box. 

World:
- Download the latest non-alpha world file from https://maps.protomaps.com/builds/. As of 09/2024 it's 127Gb in size.

Area of interest:
- Search your bbox from http://bboxfinder.com/ and copy the values from bbox (not from the url as lat lon is switched!) e.g. `11.532383,48.106973,11.619759,48.162650`
- download the latest pmtiles binary from https://github.com/protomaps/go-pmtiles/releases and run the command, e.g. this for Munich: `./pmtiles extract https://build.protomaps.com/20240812.pmtiles munich.pmtiles --bbox=11.532383,48.106973,11.619759,48.162650`

### 2 Set up a minimal Leaflet web app

Download `index.html` and change the pmtiles filename if needed.

### 3 Run a simple webserver
Make sure that the index.html & your_area.pmtiles file is saved in the same directory. E.g.
- in VS Code simply run the webserver plugin for port 5500 and go to http://localhost:5500/
- using npx: `npx serve`
- using python: `python -m http.server`

You will now see a nicely rendered background map for your area of interest or the world.



