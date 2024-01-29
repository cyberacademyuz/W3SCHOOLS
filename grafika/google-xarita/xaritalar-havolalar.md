# Xaritalar Havolalar

### Map() konstruktori

#### Misol

Google xaritasini yarating:

var map = new google.maps.Map(mapCanvas, mapOptions);

***

### Ta'rifi va qo'llanilishi

Map() konstruktori belgilangan HTML elementi (odatda \<div> elementi) ichida yangi xarita yaratadi.

***

### Sintaksis

new google.maps.Map(_HTMLElement_,_MapOptions_)

### Parametr qiymatlari

| Parameter                                                                                                                                                                     | Description                                                             |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| _HTMLElement_                                                                                                                                                                 | Specifies in what HTML element to put the map                           |
| [_MapOptions_](https://www-w3schools-com.translate.goog/graphics/tryit.asp?filename=trymap\_ref\_mapoptions&\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | A MapOptions object that holds the map initialization variables/options |

***

### Map () usullari

| Method                              | Return Value                                     | Description                                                                                             |
| ----------------------------------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------------------- |
| fitBounds(_LatLngBounds_)           | None                                             | Sets the viewport to contain the given bounds                                                           |
| getBounds()                         | _LatLng,LatLng_                                  | Returns the south-west latitude/longitude and the north-east latitude/longitude of the current viewport |
| getCenter()                         | _LatLng_                                         | Returns the lat/lng of the center of the map                                                            |
| getDiv()                            | _Node_                                           | Returns a DOM object that contains the map                                                              |
| getHeading()                        | _number_                                         | Returns the compass heading of aerial imagery (for SATELLITE and HYBRID map types)                      |
| getMapTypeId()                      | <p>HYBRID<br>ROADMAP<br>SATELLITE<br>TERRAIN</p> | Returns the current map type                                                                            |
| getProjection()                     | _Projection_                                     | Returns the current Projection                                                                          |
| getStreetView()                     | _StreetViewPanorama_                             | Returns the default StreetViewPanorama bound to the map                                                 |
| getTilt()                           | _number_                                         | Returns the angle of incidence for aerial imagery in degrees (for SATELLITE and HYBRID map types)       |
| getZoom()                           | _number_                                         | Returns the current zoom level of the map                                                               |
| panBy(_xnumber,ynumber_)            | None                                             | Changes the center of the map by the given distance in pixels                                           |
| panTo(_LatLng_)                     | None                                             | Changes the center of the map to the given LatLng                                                       |
| panToBounds(_LatLngBounds_)         | None                                             | Pans the map by the minimum amount necessary to contain the given LatLngBounds                          |
| setCenter(_LatLng_)                 | None                                             | Sets the lat/lng of the center of the map                                                               |
| setHeading(_number_)                | None                                             | Sets the compass heading for aerial imagery measured in degrees from cardinal direction North           |
| setMapTypeId(_MapTypeId_)           | None                                             | Sets the map type to display                                                                            |
| setOptions(_MapOptions_)            | None                                             |                                                                                                         |
| setStreetView(_StreetViewPanorama_) | None                                             | Binds a StreetViewPanorama to the map                                                                   |
| setTilt(_number_)                   | None                                             | Sets the angle of incidence for aerial imagery in degrees (for SATELLITE and HYBRID map types)          |
| setZoom(_number_)                   | None                                             | Sets the zoom level of the map                                                                          |

***

***

### Map() xususiyatlari

| Property        | Type                        | Description                                  |
| --------------- | --------------------------- | -------------------------------------------- |
| controls        | _Array.\<MVCArray.\<Node>>_ | Additional controls to attach to the map     |
| mapTypes        | _MapTypeRegistry_           | A registry of MapType instances by string ID |
| overlayMapTypes | _MVCArray.\<MapType>_       | Additional map types to overlay              |

***

### Xarita voqealari()

| Event               | Arguments    | Description                                                  |
| ------------------- | ------------ | ------------------------------------------------------------ |
| bounds\_changed     | None         | Fired when the viewport bounds have changed                  |
| center\_changed     | None         | Fired when the map center property changes                   |
| click               | _MouseEvent_ | Fired when the user clicks on the map                        |
| dblclick            | _MouseEvent_ | Fired when the user double-clicks on the map                 |
| drag                | None         | Fired repeatedly while the user drags the map                |
| dragend             | None         | Fired when the user stops dragging the map                   |
| dragstart           | None         | Fired when the user starts dragging the map                  |
| heading\_changed    | None         | Fired when the map heading property changes                  |
| idle                | None         | Fired when the map becomes idle after panning or zooming     |
| maptypeid\_changed  | None         | Fired when the mapTypeId property changes                    |
| mousemove           | _MouseEvent_ | Fired whenever the user's mouse moves over the map container |
| mouseout            | _MouseEvent_ | Fired when the user's mouse exits the map container          |
| mouseover           | _MouseEvent_ | Fired when the user's mouse enters the map container         |
| projection\_changed | None         | Fired when the projection has changed                        |
| resize              | None         | Fired when the map (div) changes size                        |
| rightclick          | _MouseEvent_ | Fired when the user right-clicks on the map                  |
| tilesloaded         | None         | Fired when the visible tiles have finished loading           |
| tilt\_changed       | None         | Fired when the map tilt property changes                     |
| zoom\_changed       | None         | Fired when the map zoom property changes                     |

***

### Qoplamalar

| Constructor/Object   | Description                                                                                      |
| -------------------- | ------------------------------------------------------------------------------------------------ |
| Marker               | Creates a marker. (Note that the position must be set for the marker to display)                 |
| MarkerOptions        | Options for rendering the marker                                                                 |
| MarkerImage          | A structure representing a Marker icon or shadow image                                           |
| MarkerShape          | Defines the marker shape to use in determination of a marker's clickable region (type and coord) |
| Animation            | Specifies animations that can be played on a marker (bounce or drop)                             |
| InfoWindow           | Creates an info window                                                                           |
| InfoWindowOptions    | Options for rendering the info window                                                            |
| Polyline             | Creates a polyline (contains path and stroke styles)                                             |
| PolylineOptions      | Options for rendering the polyline                                                               |
| Polygon              | Creates a polygon (contains path and stroke+fill styles)                                         |
| PolygonOptions       | Options for rendering the polygon                                                                |
| Rectangle            | Creates a rectangle (contains bounds and stroke+fill styles)                                     |
| RectangleOptions     | Options for rendering the rectangle                                                              |
| Circle               | Creates a circle (contains center+radius and stroke+fill styles)                                 |
| CircleOptions        | Options for rendering the circle                                                                 |
| GroundOverlay        |                                                                                                  |
| GroundOverlayOptions |                                                                                                  |
| OverlayView          |                                                                                                  |
| MapPanes             |                                                                                                  |
| MapCanvasProjection  |                                                                                                  |

***

### Voqealar

| Constructor/Object | Description                                                                                                                                              |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| MapsEventListener  | It has no methods and no constructor. Its instances are returned from addListener(), addDomListener() and are eventually passed back to removeListener() |
| event              | Adds/Removes/Trigger event listeners                                                                                                                     |
| MouseEvent         | Returned from various mouse events on the map and overlays                                                                                               |

***

### Boshqaruv

| Constructor/Object        | Description                                                               |
| ------------------------- | ------------------------------------------------------------------------- |
| MapTypeControlOptions     | Holds options for modifying a control (position and style)                |
| MapTypeControlStyle       | Specifies what kind of map control to display (Drop-down menu or buttons) |
| OverviewMapControlOptions | Options for rendering of the overview map control (opened or collapsed)   |
| PanControlOptions         | Options for rendering of the pan control (position)                       |
| RotateControlOptions      | Options for rendering of the rotate control (position)                    |
| ScaleControlOptions       | Options for rendering of the scale control (position and style)           |
| ScaleControlStyle         | Specifies what kind of scale control to display                           |
| StreetViewControlOptions  | Options for rendering of the street view pegman control (position)        |
| ZoomControlOptions        | Options for rendering of the zoom control (position and style)            |
| ZoomControlStyle          | Specifies what kind of zoom control to display (large or small)           |
| ControlPosition           | Specifies the placement of controls on the map                            |
