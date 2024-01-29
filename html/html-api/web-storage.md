# Web Storage

HTML veb-storage; cookielardan ko'ra yaxshi.

### HTML Web Storage nima?

Veb-ilovalar web-storage orqali ma'lumotlarni foydalanuvchining brauzerida lokal tarzda saqlashi mumkin.

HTML5 dan oldin dastur ma'lumotlari har bir server so'roviga kiritilgan cookie-fayllarda saqlanishi kerak edi. Veb-storage yanada xavfsizroq va katta hajmdagi ma'lumotlar veb-sayt ishlashiga ta'sir qilmasdan lokal tarzda saqlanishi mumkin.

Cookie-fayllardan farqli o'laroq, hotira miqdori ancha ko'p (kamida 5 MB) va ma'lumot hech qachon serverga yuborilmaydi.

Web-storage har bir origindir (domen va protokol bo'yicha). Bitta origin-dan olingan barcha sahifalar bir xil ma'lumotlarni saqlashi va ularga murojaat qilishi mumkin.

### Brauzerni qo'llab-quvvatlash

Jadvaldagi raqamlar web-storageni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini bildiradi.

| API         | Chrome | Edge | Firefox | Safari | Opera |
| ----------- | ------ | ---- | ------- | ------ | ----- |
| Web Storage | 4.0    | 8.0  | 3.5     | 4.0    | 11.5  |

### HTML web-storage obyektlari

Web-storage brauzerda ma'lumotlarni saqlash uchun ikkita obyektni taqdim qiladi:

* `window.localStorage`- amal qilish muddati ko'rsatilmagan ma'lumotlarni saqlaydi
* `window.sessionStorage`- bir sessiya uchun ma'lumotlarni saqlaydi (brauzer oynasi yopilganda ma'lumotlar yo'qoladi)

Veb-storagedan foydalanishdan oldin, **localStorage** va **sessionStorage** uchun brauzer qo'llab quvvatlashini tekshiring:

```
if (typeof(Storage) !== "undefined") {
  // Code for localStorage/sessionStorage.
} else {
  // Sorry! No Web Storage support..
}
```

### LocalStorage obyekti

localStorage obyekti ma'lumotlarni amal qilish muddatisiz saqlaydi. Brauzer yopilganda ma'lumotlar o'chirilmaydi va keyingi kun, hafta yoki yil davomida saqlanib turaveradi.

```
// Store
localStorage.setItem("lastname", "Smith");

// Retrieve
document.getElementById("result").innerHTML = localStorage.getItem("lastname");O'zingiz sinab ko'ring »
```

Misolni tushuntirish:

* Name="lastname" va value="Smit" bilan name/value juftligida localStorage yarating
* "lastname" qiymatini qabul qilib uni elementga id="value" bilan kiriting

Yuqoridagi misol mana bunday ham yozilishi mumkin:

```
// Store
localStorage.lastname = "Smith";
// Retrieve
document.getElementById("result").innerHTML = localStorage.lastname;
```

localStoragening "lastname" elementini o'chirish sintaksisi quyidagicha:

```
localStorage.removeItem("lastname");
```

**Eslatma:** name/value juftligi har doim string sifatida saqlanadi. Zarur bo'lganda ularni boshqa formatga o'tkazishni unutmang!

Quyidagi misol foydalanuvchi tugmani necha marta bosganini hisoblaydi. Ushbu kodda qiymatdagi string hisoblagichni oshirish uchun integerga aylantiriladi:

```
if (localStorage.clickcount) {
  localStorage.clickcount = Number(localStorage.clickcount) + 1;
} else {
  localStorage.clickcount = 1;
}
document.getElementById("result").innerHTML = "You have clicked the button " +
localStorage.clickcount + " time(s).";
```

### SessionStorage obyekti

`sessionStorage` obyekti localStorage obyektiga teng, ma'lumotlarni faqat bitta sessiya uchun saqlaydi. Foydalanuvchi brauzer oynasini yopganida ma'lumotlar o'chiriladi.

Quyidagi misol foydalanuvchi joriy sessiyada tugmani necha marta bosganini hisoblaydi:

```
if (sessionStorage.clickcount) {
  sessionStorage.clickcount = Number(sessionStorage.clickcount) + 1;
} else {
  sessionStorage.clickcount = 1;
}
document.getElementById("result").innerHTML = "You have clicked the button " +
sessionStorage.clickcount + " time(s) in this session.";
```
