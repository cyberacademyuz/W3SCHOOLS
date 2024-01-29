# Xaritalar Hodisalar

### Kattalashtirish uchun Markerni bosing

Biz hali ham oldingi sahifadagi xaritadan foydalanamiz: markazi London, Angliyada joylashgan xarita.

Endi biz foydalanuvchi markerni bosganida kattalashtirishni xohlaymiz (Biz bosilganda xaritani kattalashtiradigan markerga hodisa ishlov beruvchisini biriktiramiz).

Mana qo'shilgan kod:

#### Misol

// Zoom to 9 when clicking on marker\
google.maps.event.addListener(marker,'click',function() {\
&#x20; map.setZoom(9);\
&#x20; map.setCenter(marker.getPosition());\
});

Biz addListener() hodisa ishlovchisi yordamida hodisa bildirishnomalarini ro'yxatdan o'tkazamiz. Ushbu usul ob'ektni, tinglash uchun hodisani va belgilangan hodisa sodir bo'lganda chaqirish uchun funktsiyani oladi.

***

***

### Markerga qaytish

Bu erda biz masshtabdagi o'zgarishlarni saqlaymiz va 3 soniyadan keyin xaritani orqaga aylantiramiz:

#### Misol

google.maps.event.addListener(marker,'click',function() {\
&#x20; var pos = map.getZoom();\
&#x20; map.setZoom(9);\
&#x20; map.setCenter(marker.getPosition());\
&#x20; window.setTimeout(function() {map.setZoom(pos);},3000);\
});

***

### Markerni bosganingizda ma'lumot oynasini oching

Ba'zi matnli ma'lumot oynasini ko'rsatish uchun markerni bosing:

#### Misol

var infowindow = new google.maps.InfoWindow({\
&#x20; content:"Hello World!"\
});\
\
google.maps.event.addListener(marker, 'click', function() {\
&#x20; infowindow.open(map,marker);\
});

***

### Markerlarni o'rnating va har bir marker uchun ma'lumot oynasini oching

Foydalanuvchi xaritani bosganida funktsiyani ishga tushiring.

placeMarker() funksiyasi foydalanuvchi bosgan joyga markerni joylashtiradi va markerning kengliklari va uzunliklari bilan maʼlumot oynasini koʻrsatadi:

#### Misol

google.maps.event.addListener(map, 'click', function(event) {\
&#x20; placeMarker(map, event.latLng);\
});\
\
function placeMarker(map, location) {\
&#x20; var marker = new google.maps.Marker({\
&#x20;   position: location,\
&#x20;   map: map\
&#x20; });\
&#x20; var infowindow = new google.maps.InfoWindow({\
&#x20;   content: 'Latitude: ' + location.lat() +\
&#x20;   '\<br>Longitude: ' + location.lng()\
&#x20; });\
&#x20; infowindow.open(map,marker);\
}
