# Xaritalar Controllar

### Google Xaritalar - Standart boshqaruv elementlari

Standart Google xaritasini ko'rsatishda u standart boshqaruv to'plami bilan birga keladi:

* Kattalashtirish - xaritaning masshtab darajasini boshqarish uchun slayder yoki "+/-" tugmalarini ko'rsatadi
* Pan - xaritani varaqlash uchun panorama boshqaruvini ko'rsatadi
* MapType - foydalanuvchiga xarita turlari (yo'l xaritasi va sun'iy yo'ldosh) o'rtasida almashish imkonini beradi.
* Ko‘cha ko‘rinishi - Ko‘cha ko‘rinishini yoqish uchun xaritaga sudrab olib boriladigan Pegman belgisini ko‘rsatadi

***

### Google Xaritalar - Boshqa boshqaruvlar

Standart boshqaruvlardan tashqari, Google Xaritalar ham quyidagilarga ega:

* Scale - xarita masshtab elementini ko'rsatadi
* Rotate - xaritalarni aylantirish imkonini beruvchi kichik dumaloq belgini ko'rsatadi
* Umumiy ko‘rinish xaritasi - kengroq hududdagi joriy xarita ko‘rish oynasini aks ettiruvchi eskiz umumiy xaritasini ko‘rsatadi.

Xaritani yaratishda (MapOptions ichida) yoki xarita parametrlarini oʻzgartirish uchun setOptions() ga qoʻngʻiroq qilib, qaysi boshqaruv elementlari koʻrsatilishini belgilashingiz mumkin.

***

### Google Xaritalar - Standart boshqaruvlarni o'chirish

Buning o'rniga siz standart boshqaruvlarni o'chirib qo'yishingiz mumkin.

Buning uchun Xaritaning disableDefaultUI xususiyatini (Xarita variantlari obyekti ichida) rostga o‘rnating:

#### Misol

var mapOptions {disableDefaultUI: true}

***

***

### Google Xaritalar - Barcha boshqaruv elementlarini yoqing

Ba'zi boshqaruv elementlari sukut bo'yicha xaritada paydo bo'ladi; Agar siz ularni o'rnatmaguningizcha boshqalar paydo bo'lmaydi.

Xaritaga boshqaruv elementlarini qo‘shish yoki olib tashlash Map options obyektida ko‘rsatilgan.

Boshqaruvni ko'rinadigan qilish uchun rost qiymatini o'rnating - uni yashirish uchun boshqaruvni noto'g'ri qilib qo'ying.

Quyidagi misol barcha boshqaruv elementlarini "yoqadi":

#### Misol

var mapOptions {\
&#x20; panControl: true,\
&#x20; zoomControl: true,\
&#x20; mapTypeControl: true,\
&#x20; scaleControl: true,\
&#x20; streetViewControl: true,\
&#x20; overviewMapControl: true,\
&#x20; rotateControl: true\
}

***

### Google Xaritalar - Boshqaruvlarni o'zgartirish

Xarita boshqaruvlarining bir nechtasini sozlash mumkin.

Boshqarish parametrlari maydonlarini belgilash orqali boshqaruv elementlarini o'zgartirish mumkin.

Masalan, Zoom boshqaruvini o'zgartirish imkoniyatlari zoomControlOptions maydonida ko'rsatilgan. ZoomControlOptions maydoni quyidagilarni o'z ichiga olishi mumkin:

* google.maps.ZoomControlStyle.SMALL - kichik masshtabni boshqarishni ko'rsatadi (faqat + va - tugmalari)
* google.maps.ZoomControlStyle.LARGE - standart kattalashtirish slayderini ko'rsatadi
* google.maps.ZoomControlStyle.DEFAULT - qurilma va xarita hajmiga qarab eng yaxshi masshtab boshqaruvini tanlaydi

#### Misol

zoomControl: true,\
zoomControlOptions: {\
&#x20;   style: google.maps.ZoomControlStyle.SMALL\
}

Eslatma: Agar siz boshqaruvni o'zgartirsangiz, har doim birinchi navbatda boshqaruvni yoqing (uni rostga o'rnating).

Boshqa konfiguratsiya qilinadigan boshqaruv MapType boshqaruvidir.

Boshqaruvni o'zgartirish imkoniyatlari mapTypeControlOptions maydonida ko'rsatilgan. mapTypeControlOptions maydoni quyidagilarni o'z ichiga olishi mumkin:

* google.maps.MapTypeControlStyle.HORIZONTAL\_BAR - har bir xarita turi uchun bitta tugmani ko'rsatish
* google.maps.MapTypeControlStyle.DROPDOWN\_MENU - ochiladigan menyu orqali xarita turini tanlang
* google.maps.MapTypeControlStyle.DEFAULT - "standart" xatti-harakatni ko'rsatadi (ekran o'lchamiga bog'liq)

#### Misol

mapTypeControl: true,\
mapTypeControlOptions: {\
&#x20; style: google.maps.MapTypeControlStyle.DROPDOWN\_MENU\
}

Boshqaruvni ControlPosition xususiyati bilan ham joylashtirishingiz mumkin:

#### Misol

mapTypeControl: true,\
mapTypeControlOptions: {\
&#x20; style: google.maps.MapTypeControlStyle.DROPDOWN\_MENU,\
&#x20; position: google.maps.ControlPosition.TOP\_CENTER\
}
