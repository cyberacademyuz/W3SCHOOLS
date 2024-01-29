# Xaritalar Typelar

### Google Xaritalar - Asosiy xarita turlari

Google Maps API’da quyidagi xarita turlari qo‘llab-quvvatlanadi:

* ROADMAP (oddiy, standart 2D xarita)
* SATELLITE (fotografik xarita)
* GYBRID (fotografik xarita + yo'llar va shahar nomlari)
* YERLAR (tog'lar, daryolar va boshqalar ko'rsatilgan xarita)

Xarita turi MapTypeId xususiyati bilan Map xususiyatlari obyektida koʻrsatilgan:

var mapOptions = {\
&#x20; center:new google.maps.LatLng(51.508742,-0.120850),\
&#x20; zoom:7,\
&#x20; mapTypeId: google.maps.MapTypeId.HYBRID\
};

Yoki xaritaning setMapTypeId() usulini chaqirish orqali:

map.setMapTypeId(google.maps.MapTypeId.HYBRID);

***

***

### Google Xaritalar - 45° istiqbolli koʻrinish

SATELLITE va GYBRID xarita turlari maʼlum joylar uchun 45° istiqbolli tasvir koʻrinishini qoʻllab-quvvatlaydi (faqat yuqori masshtab darajalarida).

Agar siz 45° tasvir koʻrinishiga ega joyni kattalashtirsangiz, xarita avtomatik ravishda istiqbol koʻrinishini oʻzgartiradi. Bundan tashqari, xarita qo'shiladi:

* Tasvirni aylantirish imkonini beruvchi Pan boshqaruvi atrofidagi kompas g'ildiragi
* Tasvirni 90° ga aylantirish imkonini beruvchi Panorama va Masshtab boshqaruvlari o‘rtasida aylantirish boshqaruvi
* Sun'iy yo'ldosh boshqaruvi/yorlig'i ostida 45° istiqbolli ko'rinishni ko'rsatish uchun o'tish tugmasi

Eslatma: 45° tasvirli xaritadan kichraytirish bu oʻzgarishlarning har birini qaytaradi va asl xarita koʻrsatiladi.

Quyidagi misol Venetsiya, Italiyadagi Palazzo Ducalening 45° istiqbolli ko‘rinishini ko‘rsatadi:

#### Misol

var mapOptions = {\
&#x20; center:myCenter,\
&#x20; zoom:18,\
&#x20; mapTypeId:google.maps.MapTypeId.HYBRID\
};

***

### Google Xaritalar - 45° istiqbolli koʻrinishni oʻchirish - setTilt(0)

Map ob'ektida setTilt(0) ga qo'ng'iroq qilish orqali 45° istiqbolli ko'rinishni o'chirib qo'yishingiz mumkin:

#### Misol

map.setTilt(0);

Maslahat: 45° istiqbolli koʻrinishni keyinroq yoqish uchun setTilt(45) ga qoʻngʻiroq qiling.
