# Google Maps API v2 - 2009 Release Notes / Readme

**Version:** 2.x (Last major updates before v3)  
**Release Date:** 2009  
**Compatibility:** IE6+, Firefox 2+, Safari 3+, Chrome 1+, Mobile browsers (Symbian, Windows Mobile)

---

## 1. Overview

The Google Maps API allows developers to embed interactive maps on webpages. Key features include:

- Map display (map, satellite, hybrid views)
- Markers, polylines, polygons, info windows
- Events (click, mouseover, drag, zoom)
- Geocoding and reverse geocoding
- KML and GeoRSS overlays

---

## 2. New Features (2009)

- Introduction of **Google Maps API v3** (late 2009)
  - Lighter and faster
  - Designed for mobile browsers
- Experimental 3D map types for v2 (satellite overlays)
- Improved handling of KML layers and GeoRSS feeds
- Mobile layer support on Symbian and Windows Mobile

---

## 3. Bug Fixes

- Fixed memory leaks in IE6/IE7 with multiple maps
- Improved pan/zoom handling
- Resolved Street View info window click issue

---

## 4. Installation / Usage

Include the API script:

```html
<script src="http://maps.google.com/maps?file=api&v=2&key=YOUR_API_KEY"></script>
var map = new GMap2(document.getElementById("map"));
map.setCenter(new GLatLng(LATITUDE, LONGITUDE), ZOOM_LEVEL);
var marker = new GMarker(new GLatLng(LATITUDE, LONGITUDE));
map.addOverlay(marker);
GEvent.addListener(marker, "click", function() {
    marker.openInfoWindowHtml("Hello from 2009!");
});
