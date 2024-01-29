# BS5 Boshlash

### Bootstrap nima ?

* Bootstrap - bu veb-saytni tezroq va osonroq tuzish uchun bepul front-end framework
* Bootstrap tipografiya, formalar, tugmalar, jadvallar, navigatsiya, modallar, rasmli karusellar va boshqa ko'plab, JavaScript plaginlari uchun HTML va CSS-ga asoslangan dizayn shablonlarini o'z ichiga oladi.
* Bootstrap sizga moslashuvchan dizaynlarni osongina yaratish imkonini beradi

{% hint style="warning" %}
**Responsive veb-dizayn nima ?**\
\
Responsiv veb-dizayn kichik telefonlardan tortib katta ish stollarigacha bo'lgan barcha qurilmalarda to'g'ri ko'rinishga avtomatik tarzda moslashadigan veb-saytlar yaratishdir.
{% endhint %}

{% code title="Bootstrap 5ga misol:" %}
```
<div class="container-fluid p-5 bg-primary text-white text-center">
  <h1>My First Bootstrap Page</h1>
  <p>Resize this responsive page to see the effect!</p>
</div>

<div class="container mt-5">
  <div class="row">
    <div class="col-sm-4">
      <h3>Column 1</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
      <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris...</p>
    </div>
    <div class="col-sm-4">
      <h3>Column 2</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
      <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris...</p>
    </div>
    <div class="col-sm-4">
      <h3>Column 3</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
      <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris...</p>
    </div>
  </div>
</div>
```
{% endcode %}

### Bootstrap versiyalari

Bootstrap 5 (2021-yilda chiqarilgan) - Bootstrapning eng birinchi versiyasi (2013-yilda chiqarilgan)

Bootstrap 5 barcha asosiy brauzerlar va platformalarning so'nggi, barqaror versiyalarini qo'llab-quvvatlaydi. Biroq, Internet Explorer 11 va undan oldingi versiyalarda qo'llab-quvvatlanmaydi.

Bootstrap 5 va Bootstrap 3 & 4 o'rtasidagi asosiy farq shundaki, Bootstrap 5 jQuery o'rniga [JavaScript](broken-reference)-ga o'tgan.

{% hint style="warning" %}
**Eslatma:** Bootstrap 3 va Bootstrap 4 hali ham ulardagi xatolarni tuzatish va hujjatlarni o'zgartirish uchun jamoa tomonidan qo'llab-quvvatlanadi va ulardan foydalanishni davom ettirish mutlaqo xavfsizdir. Biroq, ularga yangi xususiyatlar qo'shilmaydi.
{% endhint %}

### Nima uchun Bootstrap dan foydalanish kerak ?

Bootstrap-ning afzalliklari:

* **Foydalanish oson:** HTML va CSS-ni bilgan har bir kishi Bootstrap-dan foydalanishni boshlashi mumkin
* **Moslashuvchan xususiyatlar:** Bootstrap-ning moslashuvchan CSSi telefonlar, planshetlar va ish stollariga moslashadi.
* **Mobile-first yondashuvi:** Bootstrap-da mobil-first stillari asosiy tizimning bir qismi hisoblanadi
* **Brauzerga mosligi:** Bootstrap 5 barcha zamonaviy brauzerlar (Chrome, Firefox, Edge, Safari va Opera) bilan mos keladi. **Diqqat qiling**, agar IE11 va undan kichik versiyalar uchun yordam kerak bo'lsa, BS4 yoki BS3 dan foydalanishingiz kerak.

### Bootstrap 5 ni qayerdan olish mumkin ?

Veb-saytingizda Bootstrap 5-dan foydalanishni ikki yo'l bilan boshlashingiz mumkin:

* CDN orqali Bootstrap 5 ni ulab
* Getbootstrap.com saytidan Bootstrap 5-ni yuklab olib

### Bootstrap 5 CDN

Agar Bootstrap 5-ni yuklab olishni va joylashtirishni xohlamasangiz, uni CDN (Content Delivery Network) orqali ulashingiz mumkin.

jsDelivr Bootstrap-ning CSS va JavaScripti uchun CDN-ni qo'llab-quvvatlaydi:

{% code title="MaxCDN:" %}
```
<!-- Latest compiled and minified CSS -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" rel="stylesheet">

<!-- Latest compiled JavaScript -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js"></script>
```
{% endcode %}

{% hint style="warning" %}
Bootstrap 5 CDN-dan foydalanishning afzalliklaridan biri:\
Ko'p foydalanuvchilar boshqa saytga tashrif buyurganlarida allaqachon jsDelivr'dan Bootstrap 5-ni yuklab olishgan. Natijada, ular saytingizga tashrif buyurishganda, u keshdan yuklanadi, bu esa tezroq yuklash vaqtini olib keladi. Bundan tashqari, ko'pchilik CDN-lar foydalanuvchi undan fayl so'ragandan so'ng, u ularga eng yaqin serverdan xizmat ko'rsatishiga ishonch hosil qiladi, bu ham tezroq yuklash vaqtiga olib keladi.\
\
**JavaScript?**\
Bootstrap 5 JavaScript-ni turli komponentlar uchun ishlatadi (modellar, maslahatlar, popoverlar va boshqalar). Biroq, agar siz Bootstrap-ning CSS qismidan foydalansangiz, ularga kerak emas.
{% endhint %}

### Bootstrap 5 yuklab olish

Agar Bootstrap 5-ni yuklab olishini va joylashtirishni istasangiz, [https://getbootstrap.com/](https://getbootstrap.com/) saytiga o'ting va u yerdagi ko'rsatmalarga amal qiling.

### Bootstrap 5 yordamida birinchi veb-sahifangizni yarating

**1. HTML5 hujjat turini qo'shing**

Bootstrap 5 HTML5 hujjat turini talab qiluvchi HTML elementlari va CSS xususiyatlaridan foydalanadi.

Har doim HTML5 hujjat turini sahifaning boshiga lang atributi va toʻgʻri nom va belgilar toʻplami bilan birga kiriting:

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Bootstrap 5 Example</title>
    <meta charset="utf-8">
  </head>
</html>
```

**2. Bootstrap 5 mobile-first hisoblanadi**

Bootstrap 5 mobil qurilmalarga moslashish uchun mo'ljallangan. Mobil-first stillar freymworkning asosiy bir qismi hisoblanadi.

To'g'ri ishlash va touch zoomingni ta'minlash uchun `<head>` elementining ichiga `<meta>` tegini qo'shing:

```
<meta name="viewport" content="width=device-width, initial-scale=1">
```

`width=device-width` qismi sahifaning kengligini qurilmaning ekran kengligiga rioya qilish uchun o'rnatiladi (bu qurilmaga qarab o'zgaradi).

`initial-scale=1` qismi esa brauzer tomonidan sahifa birinchi marta yuklanganda boshlang'ich kattalik darajasini o'rnatadi.

**3. Konteynerlar**

Bootstrap 5 shuningdek, sayt tarkibini o'z o'rab turish uchun o'zining elementini talab qiladi.

Tanlash uchun ikkita konteyner classi mavjud:

1. `.container` classi moslashuvchan kenglikdagi konteyner taqdim qiladi
2. `.container-fluid` classi ko'rish oynasining butun kengligini qamrab oluvchi to'liq kenglikdagi konteyner taqdim etadi

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

### Bootstrap 5 uchun boshlang'ich ikki sahifa

Quyidagi misolda Bootstrap 5 da boshlang'ich sahifasi yaratish uchun kod ko'rsatilgan (moslashuvchan kenglikdagi konteyner bilan):

{% code title="Konteynerga misol:" %}
```
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap Example</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>

<div class="container">
  <h1>My First Bootstrap Page</h1>
  <p>This part is inside a .container class.</p>
  <p>The .container class provides a responsive fixed width container.</p>
</div>

</body>
</html>
```
{% endcode %}

Quyidagi misolda Bootstrap 5 da boshlang'ich sahifasi yaratish uchun kod ko'rsatilgan (to'liq kenglikdagi konteyner bilan):

{% code title="Idishdagi suyuqlik misoli:" %}
```
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap Example</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>

<div class="container-fluid">
  <h1>My First Bootstrap Page</h1>
  <p>This part is inside a .container-fluid class.</p>
  <p>The .container-fluid class provides a full width container, spanning the entire width of the viewport.</p>
</div>

</body>
</html>
```
{% endcode %}
