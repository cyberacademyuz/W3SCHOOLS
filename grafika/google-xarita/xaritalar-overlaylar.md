# Xaritalar Overlaylar

### Google Xaritalar - Qatlamlar

Qoplamalar xaritadagi kenglik/uzunlik koordinatalariga bog'langan ob'ektlardir.

Google Xaritalarda bir necha turdagi qoplamalar mavjud:

* Marker - Xaritadagi yagona joylar. Markerlar maxsus piktogramma tasvirlarini ham ko'rsatishi mumkin
* Polyline - Xaritadagi to'g'ri chiziqlar qatori
* Ko'pburchak - xaritadagi to'g'ri chiziqlar qatori va shakli "yopiq"
* Doira va to'rtburchak
* Ma'lumot Windows - Xaritaning tepasida qalqib chiquvchi shar ichida tarkibni ko'rsatadi
* Maxsus qoplamalar

***

### Google Xaritalar - Marker qo'shing

Marker konstruktori marker yaratadi. E'tibor bering, markerni ko'rsatish uchun joylashuv xususiyati o'rnatilishi kerak.

Markerni setMap() usuli yordamida xaritaga qo'shing:

#### Misol

var marker = new google.maps.Marker({position: myCenter});\
\
marker.setMap(map);

***

***

### Google Xaritalar - Markerni jonlantiring

Quyidagi misolda markerni animatsiya xususiyati bilan qanday jonlantirish mumkinligi ko‘rsatilgan:

#### Misol

var marker = new google.maps.Marker({\
&#x20; position:myCenter,\
&#x20; animation:google.maps.Animation.BOUNCE\
});\
\
marker.setMap(map);

***

### Google Xaritalar - Marker o'rniga belgi

Quyidagi misolda standart marker o‘rniga foydalanish uchun rasm (belgi) ko‘rsatilgan:

#### Misol

var marker = new google.maps.Marker({\
&#x20; position:myCenter,\
&#x20; icon:'pinkball.png'\
});\
\
marker.setMap(map);

***

### Google Xaritalar - Polyline

Polyline - bu tartiblangan ketma-ketlikda bir qator koordinatalar orqali o'tkaziladigan chiziq.

Polyline quyidagi xususiyatlarni qo'llab-quvvatlaydi:

* yo'l - chiziq uchun bir nechta kenglik/uzunlik koordinatalarini belgilaydi
* strokeColor - chiziq uchun o'n oltilik rangni belgilaydi (format: "#FFFFFF")
* strokeOpacity - chiziqning shaffofligini belgilaydi (0,0 dan 1,0 gacha bo'lgan qiymat)
* strokeWeight - chiziq chizig'ining piksellardagi og'irligini belgilaydi
* tahrirlanishi mumkin - qatorni foydalanuvchilar tomonidan tahrirlanishi mumkinligini aniqlaydi (to'g'ri/noto'g'ri)

#### Misol

var myTrip = \[stavanger,amsterdam,london];\
var flightPath = new google.maps.Polyline({\
&#x20; path:myTrip,\
&#x20; strokeColor:"#0000FF",\
&#x20; strokeOpacity:0.8,\
&#x20; strokeWeight:2\
});

***

### Google Xaritalar - Poligon

Ko'pburchak ko'p chiziqqa o'xshaydi, chunki u tartiblangan ketma-ketlikdagi bir qator koordinatalardan iborat. Biroq, ko'pburchaklar yopiq tsikldagi hududlarni aniqlash uchun mo'ljallangan.

Ko'pburchaklar to'g'ri chiziqlardan iborat bo'lib, shakli "yopiq" (barcha chiziqlar birlashadi).

Ko'pburchak quyidagi xususiyatlarni qo'llab-quvvatlaydi:

* yo'l - chiziq uchun bir nechta LatLng koordinatalarini belgilaydi (birinchi va oxirgi koordinatalar teng)
* strokeColor - chiziq uchun o'n oltilik rangni belgilaydi (format: "#FFFFFF")
* strokeOpacity - chiziqning shaffofligini belgilaydi (0,0 dan 1,0 gacha bo'lgan qiymat)
* strokeWeight - chiziq chizig'ining piksellardagi og'irligini belgilaydi
* fillColor - yopiq hududdagi maydon uchun o'n oltilik rangni belgilaydi (format: "#FFFFFF")
* fillOpacity - to'ldirish rangining shaffofligini belgilaydi (0,0 dan 1,0 gacha bo'lgan qiymat)
* tahrirlanishi mumkin - qatorni foydalanuvchilar tomonidan tahrirlanishi mumkinligini aniqlaydi (to'g'ri/noto'g'ri)

#### Misol

var myTrip = \[stavanger,amsterdam,london,stavanger];\
var flightPath = new google.maps.Polygon({\
&#x20; path:myTrip,\
&#x20; strokeColor:"#0000FF",\
&#x20; strokeOpacity:0.8,\
&#x20; strokeWeight:2,\
&#x20; fillColor:"#0000FF",\
&#x20; fillOpacity:0.4\
});

***

### Google Xaritalar - Circle

Doira quyidagi xususiyatlarni qo'llab-quvvatlaydi:

* center - aylana markazining google.maps.LatLng ni belgilaydi
* radius - aylana radiusini, metrda ko'rsatadi
* strokeColor - aylana atrofidagi chiziq uchun o'n oltilik rangni belgilaydi (format: "#FFFFFF")
* strokeOpacity - chiziq rangining shaffofligini belgilaydi (0,0 dan 1,0 gacha bo'lgan qiymat)
* strokeWeight - chiziq chizig'ining piksellardagi og'irligini belgilaydi
* fillColor - doira ichidagi maydon uchun o'n oltilik rangni belgilaydi (format: "#FFFFFF")
* fillOpacity - to'ldirish rangining shaffofligini belgilaydi (0,0 dan 1,0 gacha bo'lgan qiymat)
* tahrirlanishi mumkin - doira foydalanuvchilar tomonidan tahrirlanishi yoki yo'qligini aniqlaydi (to'g'ri/noto'g'ri)

#### Misol

var myCity = new google.maps.Circle({\
&#x20; center:amsterdam,\
&#x20; radius:20000,\
&#x20; strokeColor:"#0000FF",\
&#x20; strokeOpacity:0.8,\
&#x20; strokeWeight:2,\
&#x20; fillColor:"#0000FF",\
&#x20; fillOpacity:0.4\
});

***

### Google Xaritalar - InfoWindow

Marker uchun ba'zi matn mazmuni bilan InfoWindow ko'rsatish:

#### Misol

var infowindow = new google.maps.InfoWindow({\
&#x20; content:"Hello World!"\
});\
\
infowindow.open(map,marker);
