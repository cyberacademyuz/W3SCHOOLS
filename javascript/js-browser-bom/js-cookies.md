# JS Cookies

Cookie-fayllar foydalanuvchi ma'lumotlarini veb-sahifalarda saqlash imkonini beradi.

### Cookie fayllar nima?

Cookielar kompyuteringizda kichik matnli fayllarda saqlanadigan ma'lumotlardir.

Veb-server veb-sahifani brauzerga yuborganida, ulanish o'chiriladi va server foydalanuvchi haqida barcha ma'lumotni unutadi.

Cookie fayllari "foydalanuvchi haqidagi ma'lumotni eslab qolish" muammosini hal qilish uchun ixtiro qilingan:

* Foydalanuvchi veb-sahifaga tashrif buyurganida, uning ismi cookie faylida saqlanishi mumkin.
* Keyingi safar foydalanuvchi sahifaga tashrif buyurganida, cookie uning ismini “eslaydi”.

Cookie fayllaridagi ma'lumotlar nom-qiymat juftligi ko'rinishida saqlanadi:

```
username = John Doe
```

Brauzer serverdan veb-sahifani so'raganda, sahifaga tegishli cookielar so'rovga qo'shiladi. Shunday qilib, server foydalanuvchilar haqidagi ma'lumotlarni "eslash" uchun kerakli ma'lumotlarni oladi.

{% hint style="warning" %}
Agar brauzeringizda lokal cookielarni qo‘llab-quvvatlash o‘chirilgan bo‘lsa, quyidagilarning hech biri ishlamaydi.
{% endhint %}

### JavaScript yordamida cookie yaratish

JavaScript `document.cookie` xususiyati orqali cookielarni yaratishi, o'qishi va o'chirishi mumkin.

JavaScript yordamida cookie quyidagicha yaratilishi mumkin:

```
document.cookie = "username=John Doe";
```

Yaroqlilik muddatini ham qo'shishingiz mumkin (UTC vaqti). Standart tarzda, brauzer yopilganda cookie o'chiriladi:

```
document.cookie = "username=John Doe; expires=Thu, 18 Dec 2013 12:00:00 UTC";
```

`path` parametri yordamida brauzerga cookie fayli qaysi joylashuvga tegishli ekanligini aytishingiz mumkin. Standart holda, cookie joriy sahifaga tegishli bo'ladi.

```
document.cookie = "username=John Doe; expires=Thu, 18 Dec 2013 12:00:00 UTC; path=/";
```

### JavaScript yordamida cookieni o'qish

JavaScript yordamida cookieni quyidagicha o'qish mumkin:

```
let x = document.cookie;
```

{% hint style="warning" %}
`document.cookie` barcha cookielarni bitta stringda qaytaradi: cookie1=value; cookie2=value; cookie3=value;
{% endhint %}

### JavaScript yordamida cookieni o'zgartirish

JavaScript yordamida cookieni xuddi uni yaratganingizdek o'zgartirishingiz mumkin:

```
document.cookie = "username=John Smith; expires=Thu, 18 Dec 2013 12:00:00 UTC; path=/";
```

Eski cookie o'rniga yozilgan.

### JavaScript yordamida cookieni o'chirish

Cookie-ni o'chirish juda oddiy.

Cookieni o'chirishda cookie qiymatini belgilashingiz shart emas.

Faqat expires parametriga o'tib ketgan sanani bering:

```
document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
```

{% hint style="warning" %}
To'g'ri cookieni o'chirayotganingizga ishonch hosil qilish uchun cookie joylashuvini berishingi kerak.

Agar joylashuvni ko'rsatmasangiz, ba'zi brauzerlar cookie faylini o'chirishga ruxsat bermaydi.
{% endhint %}

### Cookie string

`document.cookie` xususiyati oddiy matn stringgiga o'xshaydi. Lekin unday emas.

Agar document.cookie-ga butun cookielar stringgini yozsangiz ham, uni qayta o'qiganingizda, uning faqat nom-qiymat juftligini ko'rishingiz mumkin.

Agar yangi cookieni o'rnatsangiz, eski cookielar o'rniga yozilmaydi. Yangi cookie document.cookie-ga qo'shiladi, shuning uchun agar document.cookie-ni qayta o'qisangiz, quyidagi kabi narsalarni olasiz:

```
cookie1 = qiymat; cookie2 = qiymat;
```

Agar bitta cookie qiymatini topmoqchi bo'lsangiz, cookielar stringgida cookie qiymatini qidiradigan JavaScript funksiyasini yozishingiz kerak.

### Cookielarga misol

Quyidagi misolda tashrif buyuruvchining ismini saqlaydigan cookie yaratamiz.

Foydalanuvchi veb-sahifaga birinchi marta kirganida, undan o'z ismini to'ldirish so'raladi. Keyin ism cookie faylida saqlanadi.

Foydalanuvchi keyingi safar o'sha sahifaga kirganida, u salomlash xabarini oladi.

Misol uchun biz 3 ta funksiya yaratamiz:

1. Cookie qiymatini o'rnatish funksiyasi
2. Cookie qiymatini olish funksiyasi
3. Cookie qiymatini tekshirish funksiyasi

### Cookie faylini o'rnatish funksiyasi

Birinchidan, foydalanuvchi nomini cookie o'zgaruvchisida saqlaydigan `function`  yaratamiz:

```
function setCookie(cname, cvalue, exdays) {
  const d = new Date();
  d.setTime(d.getTime() + (exdays*24*60*60*1000));
  let expires = "expires="+ d.toUTCString();
  document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
}
```

**Misolni tushuntirish:**

Yuqoridagi funksiyaning parametrlari cookie faylining nomi (cname), cookie qiymati (cvalue) va cookie muddati tugashi kerak bo'lgan kunlar soni (exdays).

Funksiya cookie nomini, cookie qiymatini va amal qilish muddati stringlarini qo'shish orqali cookie o'rnatadi.

### Cookieni olish funksiyasi

Keyin, belgilangan cookie qiymatini qaytaradigan `function` yaratamiz:

```
function getCookie(cname) {
  let name = cname + "=";
  let decodedCookie = decodeURIComponent(document.cookie);
  let ca = decodedCookie.split(';');
  for(let i = 0; i <ca.length; i++) {
    let c = ca[i];
    while (c.charAt(0) == ' ') {
      c = c.substring(1);
    }
    if (c.indexOf(name) == 0) {
      return c.substring(name.length, c.length);
    }
  }
  return "";
}
```

**Funktsiyani tushuntirish:**

Cookie nomini parametr (cname) sifatida oling.

Izlash uchun matn bilan o'zgaruvchi (ism) yarating (cname + "=").

Maxsus belgilar bilan cookielarni qayta ishlash uchun cookielar stringgini dekodlash, masalan, “$”

`document.cookie` dan nuqta-vergulni ajratib ca (ca = decodedCookie.split(';')) nomli massivga tayinlash

Ca massivi bo'ylab harakatlaning (i = 0; i < ca.length; i++) va c = ca\[i]ning har bir qiymatni o'qing).

Agar cookie topilsa (c.indexOf(name) == 0), cookie qiymatini qaytaring (c.substring(name.length, c.length).

Agar cookie topilmasa, bo'sh string `""` qaytaring.

### Cookieni tekshirish funksiyasi

Va nihoyat, biz cookie fayli o'rnatilgan yoki o'rnatilmaganligini tekshiradigan funksiya yaratamiz.

Agar cookie o'rnatilgan bo'lsa, u salomlashish oynasini ko'rsatadi.

Agar cookie o'rnatilmagan bo'lsa, u foydalanuvchi nomini so'rovchi so'rov oynasini ko'rsatadi va `setCookie` funksiyasini chaqirish orqali foydalanuvchining ismini cookie faylida 365 kun saqlaydi:

```
function checkCookie() {
  let username = getCookie("username");
  if (username != "") {
   alert("Welcome again " + username);
  } else {
    username = prompt("Please enter your name:", "");
    if (username != "" && username != null) {
      setCookie("username", username, 365);
    }
  }
}
```

### Barchasini jamlash

```
function setCookie(cname, cvalue, exdays) {
  const d = new Date();
  d.setTime(d.getTime() + (exdays * 24 * 60 * 60 * 1000));
  let expires = "expires="+d.toUTCString();
  document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
}

function getCookie(cname) {
  let name = cname + "=";
  let ca = document.cookie.split(';');
  for(let i = 0; i < ca.length; i++) {
    let c = ca[i];
    while (c.charAt(0) == ' ') {
      c = c.substring(1);
    }
    if (c.indexOf(name) == 0) {
      return c.substring(name.length, c.length);
    }
  }
  return "";
}

function checkCookie() {
  let user = getCookie("username");
  if (user != "") {
    alert("Welcome again " + user);
  } else {
    user = prompt("Please enter your name:", "");
    if (user != "" && user != null) {
      setCookie("username", user, 365);
    }
  }
}
```

Yuqoridagi misol sahifa yuklanganda `checkCookie()` funksiyasini ishga tushiradi.
