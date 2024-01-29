# Xaritalar Boshlag'ich

### Asosiy Google xaritasini yarating

Ushbu misol markazi London, Angliyada joylashgan Google xaritasini yaratadi:

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

Ushbu sahifaning qolgan qismi yuqoridagi misolni bosqichma-bosqich tasvirlaydi.

***

### Xarita konteyneri va hajmi

Xaritani ushlab turish uchun xaritaga HTML elementi kerak:

\<div id="googleMap" style="width:100%;height:400px">\</div>

Shuningdek, xaritaning o'lchamini o'rnating.

***

***

### Xarita xususiyatlarini o'rnatish uchun funktsiya yarating

function myMap() {\
var mapProp = {\
&#x20;   center:new google.maps.LatLng(51.508742,-0.120850),\
&#x20;   zoom:5,\
};\
var map = new google.maps.Map(document.getElementById("googleMap"),mapProp);\
}

mapProp **o'zgaruvchisi** xarita uchun xususiyatlarni belgilaydi.

Markaz xususiyati xaritani qayerga markazlashtirishni (kenglik va uzunlik koordinatalaridan foydalangan holda) belgilaydi **.**

Kattalashtirish xususiyati xarita uchun masshtab darajasini belgilaydi (kattalashtirish darajasi bilan tajriba o'tkazishga harakat qiling) **.**

Qator: **var map=new google.maps.Map(document.getElementById("googleMap"), mapProp);** o'tkazilgan parametrlar (mapProp) yordamida \<div> elementi ichida id="googleMap" bilan yangi xarita yaratadi.

***

### Bir nechta xaritalar

Quyidagi misol turli xil xarita turlariga ega to'rtta xaritani belgilaydi:

#### Misol

var map1 = new google.maps.Map(document.getElementById("googleMap1"), mapOptions1);\
var map2 = new google.maps.Map(document.getElementById("googleMap2"), mapOptions2);\
var map3 = new google.maps.Map(document.getElementById("googleMap3"), mapOptions3);\
var map4 = new google.maps.Map(document.getElementById("googleMap4"), mapOptions4);

***

### Bepul Google API kaliti

Google veb-saytga kuniga minglab marta istalgan Google API-ga bepul qo'ng'iroq qilish imkonini beradi.

API kalitini qanday olishni oʻrganish uchun [https://developers.google.com/maps/documentation/javascript/get-api-key](https://translate.google.com/website?sl=auto\&tl=uz\&hl=en\&client=webapp\&u=https://developers.google.com/maps/documentation/javascript/get-api-key) sahifasiga oʻting .

Google Xaritalar API-ni yuklashda **asosiy** parametrda API kalitini topishni kutadi :

\<script src="https://maps.googleapis.com/maps/api/js?**key=YOUR\_KEY**\&callback=myMap">\</script>
