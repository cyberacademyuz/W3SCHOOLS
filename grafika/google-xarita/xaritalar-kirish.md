# Xaritalar Kirish

### Google Maps API

**Ushbu qo'llanma Google Maps API (I** nterfeys dasturlash **dasturi** ) haqida **.**

API - bu dasturiy ilovalarni yaratish uchun ishlatilishi mumkin bo'lgan usullar va vositalar to'plami.

***

### HTMLda Google Xaritalar

Ushbu misol HTMLda Google xaritasini yaratadi:

#### Misol

\<!DOCTYPE html>\
\<html>\
\<body>\
\
\<h1>My First Google Map\</h1>\
\
\<div id="googleMap" style="width:100%;height:400px;">\</div>\
\
\<script>\
function myMap() {\
var mapProp= {\
&#x20; center:new google.maps.LatLng(51.508742,-0.120850),\
&#x20; zoom:5,\
};\
var map = new google.maps.Map(document.getElementById("googleMap"),mapProp);\
}\
\</script>\
\
\<script src="https://maps.googleapis.com/maps/api/js?key=YOUR\_KEY\&callback=myMap">\</script>\
\
\</body>\
\</html>
