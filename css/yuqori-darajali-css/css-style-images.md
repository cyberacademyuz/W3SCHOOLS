# CSS Style images

Rasmlarga CSS orqali qanday qilib stil berishni o'rganamiz

### Yumaloq rasmlar <a href="#yumaloq-rasmlar" id="yumaloq-rasmlar"></a>

`border-radius` xususiyati orqali yumaloq rasmlar yasash mumkin.

Yumaloq rasm

![](<../../.gitbook/assets/paris (1).jpg>)

```
img {
  border-radius: 8px;
}
```

Dumaloq rasm

![](<../../.gitbook/assets/image (252).png>)

```
img {
  border-radius: 50%;
}
```

### Eskiz rasmlari <a href="#eskiz-rasmlari" id="eskiz-rasmlari"></a>

`border` xususiyati orqali eskiz rasmlar yaratish mumkin

thumbnail rasm

![](<../../.gitbook/assets/image (609).png>)&#x20;

```
img {
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 5px;
  width: 150px;
}

<img src="paris.jpg" alt="Paris">
```

Link sifatidagi eskiz rasm

![](<../../.gitbook/assets/image (650).png>)

```
img {
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 5px;
  width: 150px;
}

img:hover {
  box-shadow: 0 0 2px 1px rgba(0, 140, 186, 0.5);
}

<a href="paris.jpg">
  <img src="paris.jpg" alt="Paris">
</a>
```

### Responsive rasmlar <a href="#responsive-rasmlar" id="responsive-rasmlar"></a>

Responsive rasmlar avtomatik tarzda ekran o'lchamiga moslashadi

Quyidagi rasmning moslashishini ko'rish uchun brauzer oynasini kichkinalashtiring:

<figure><img src="../../.gitbook/assets/img_5terre_wide.jpg" alt=""><figcaption></figcaption></figure>

Agar rasmni kichkroq qilmoqchi bo'lsangiz kichraytirishigiz mumkin, lekin uni asl o'lchamida kattalashtirmang, quyidagilarni qo'shib qo'ying:

```
img {
  max-width: 100%;
  height: auto;
}
```

**Maslahat:** Responsive veb-dizayn haqida ko'proq ma'lumot olish uchun [CSS RWD qo'llanma](broken-reference)mizga o'ting.

### Rasmni o'rtaga joylashtirish <a href="#rasmni-ortaga-joylashtirish" id="rasmni-ortaga-joylashtirish"></a>

Rasmni o'rtaga joylashtirish uchun chap va o'ng tomondagi marginga auto qiymatini bering va uni block elementiga aylantiring:

<figure><img src="../../.gitbook/assets/paris.jpg" alt=""><figcaption></figcaption></figure>

```
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}
```

### Polaroid rasmlar / Kartalar <a href="#polaroid-rasmlar-kartalar" id="polaroid-rasmlar-kartalar"></a>

<figure><img src="../../.gitbook/assets/image (644).png" alt=""><figcaption></figcaption></figure>

```
div.polaroid {
  width: 80%;
  background-color: white;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

img {width: 100%}

div.container {
  text-align: center;
  padding: 10px 20px;
}
```

### Shaffof rasmlar <a href="#shaffof-rasmlar" id="shaffof-rasmlar"></a>

<figure><img src="../../.gitbook/assets/image (228).png" alt=""><figcaption></figcaption></figure>

`opacity` xususiyati 0.0 va 1.0 oralig'idagi qiymat sifatida qabul qiladi. Qiymat qanchalik kcihkina bo'lsa, u shunchalik shaffof bo'ladi.

```
 img {
  opacity: 0.5;
}
```

### Rasmdagi matn <a href="#rasmdagi-matn" id="rasmdagi-matn"></a>

Matnni rasm ichiga qanday joylashtirish kerak:

<figure><img src="../../.gitbook/assets/image (233).png" alt=""><figcaption></figcaption></figure>

### Rasm filterlari <a href="#rasm-filterlari" id="rasm-filterlari"></a>

CSSning `filter` xususiyati elementga vizual effektlar qo'shadi (blur va saturation kabi)

**Eslatma:** `filter` xususiyati **Edge 12** va **Internet Explorer**da qo'llab quvvatlanmaydi.

Barcha rasmlarning rangini oq qora qiling:

```
 img {
  filter: grayscale(100%);
}
```

<figure><img src="../../.gitbook/assets/image (255).png" alt=""><figcaption></figcaption></figure>

**Maslahat:** CSS filterlari haqida batafsil ma'lumot olish <mark style="color:green;">CSS filter reference</mark> sahifamizga o'ting.

### Rasmni o'rab turuvchi overlayni joylashtirish <a href="#rasmni-orab-turuvchi-overlayni-joylashtirish" id="rasmni-orab-turuvchi-overlayni-joylashtirish"></a>

Hover qilinganda chiqadigan overlay effektini yaratish:

<figure><img src="../../.gitbook/assets/image (570).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (269).png" alt=""><figcaption></figcaption></figure>

### Rasmni chapdan o'ngga aylantirish <a href="#rasmni-chapdan-ongga-aylantirish" id="rasmni-chapdan-ongga-aylantirish"></a>

Rasm ustiga sichqonchani olib boring

![](<../../.gitbook/assets/image (595).png>)

```
img:hover {
  transform: scaleX(-1);
}
```

### Responsive rasm gallereyalari <a href="#responsive-rasm-gallereyalari" id="responsive-rasm-gallereyalari"></a>

CSS-dan rasm galereyalarini yaratish uchun foydalanish mumkin. Ushbu misolda turli xil ekran o'lchamlarida rasmlarni qayta tartiblash uchun **media qierie**lardan foydalanilgan. Buni ko'rish uchun brauzer oynasining o'lchamini o'zgartiring:

<figure><img src="../../.gitbook/assets/image (264).png" alt=""><figcaption></figcaption></figure>

```
.responsive {
  padding: 0 6px;
  float: left;
  width: 24.99999%;
}

@media only screen and (max-width: 700px){
  .responsive {
    width: 49.99999%;
    margin: 6px 0;
  }
}

@media only screen and (max-width: 500px){
  .responsive {
    width: 100%;
  }
}
```

**Maslahat:** Responsive Web Design haqida batafsil o'qish uchun CSS RWD darsligimizga o'ting.

### Rasmli modal (Ixtiyoriy) <a href="#rasmli-modal-ixtiyoriy" id="rasmli-modal-ixtiyoriy"></a>

Ushbu misolda CSS va Javascriptni birga ishlatish ko'rsatilgan.

Birinchi, modal oynasini yaratish uchun CSS dan foydalaning va uni berkiting,

Keyin esa foydalanuvchi rasm ustiga bosganida rasmni modal ichida ko'rsatish uchun JavaScript dan foydalaning.

![](<../../.gitbook/assets/image (347).png>)

```
// Get the modal
var modal = document.getElementById('myModal');

// Get the image and insert it inside the modal - use its "alt" text as a caption
var img = document.getElementById('myImg');
var modalImg = document.getElementById("img01");
var captionText = document.getElementById("caption");
img.onclick = function(){
  modal.style.display = "block";
  modalImg.src = this.src;
  captionText.innerHTML = this.alt;
}

// Get the <span> element that closes the modal
var span = document.getElementsByClassName("close")[0];

// When the user clicks on <span> (x), close the modal
span.onclick = function() {
  modal.style.display = "none";
} 
```
