---
description: Rasmlar veb-sahifaning dizayni va ko'rinishini yaxshilaydi.
---

# Rasmlar

<figure><img src="../../../.gitbook/assets/image (389).png" alt=""><figcaption></figcaption></figure>

```html
<img src="pic_trulli.jpg" alt="Italian Trulli">
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_trulli" %}

{% code title="Misol" %}
```html
<img src="img_girl.jpg" alt="Girl in a jacket">
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_girl" %}

{% code title="Misol:" %}
```html
<img src="img_chania.jpg" alt="Flowers in Chania">
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_chania" %}

## <mark style="color:green;">HTML Rasmlar sintaksisi</mark>

HTMLda <mark style="color:red;">`<img>`</mark> tegi rasmni veb-sahifaga joylashtirish uchun ishlatiladi.

Rasmlar texnik jihatdan veb-sahifaga joylashtirilmaydi; ular veb-sahifalarga havola sifatida ulanadi.  <mark style="color:red;">`<img>`</mark> tegi ulaniladigan rasmni saqlash uchun joy yaratadi.

<mark style="color:red;">`<img>`</mark> tegi toq teg hisoblanib faqatgina attributlarni o'z ichiga oladi va tag yopilmaydi.

<mark style="color:red;">`<img>`</mark> tegi 2 ta attribut talab qiladi.

* <mark style="color:red;">`src`</mark> - Rasmning joyashuvi
* <mark style="color:red;">`alt`</mark> - Rasm uchun alternativ matn

{% code title="Sintaksis" %}
```html
 <img src="url" alt="alternatetext"> 
```
{% endcode %}

## <mark style="color:green;">`src`</mark> <mark style="color:green;"></mark><mark style="color:green;">attributi</mark>

<mark style="color:red;">`src`</mark> atributi rasm uchun uning joylashuvi (URL) ni talab qiladi

**Eslatma:** Veb-sahifa yuklanganda, brauzer rasmni veb-serverdan oladi va uni sahifaga kiritadi. Shuning uchun, rasm havolasi to'g'ri ekanligiga ishonch hosil qiling, aks holda foydalanuvchilaringiz havola noto'g'ri ulanganda chiqadigan belgini ko'rishadi. Agar brauzer rasmni topa olmasa, belgi va `alt` attributidagi matn ko'rsatiladi.

{% code title="Misol" %}
```html
<img src="img_chania.jpg" alt="Flowers in Chania"> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_alt_chania" %}

## <mark style="color:green;">`alt`</mark> <mark style="color:green;"></mark><mark style="color:green;">attributi</mark>

Agar foydalanuvchi biron sababga ko'ra rasmni ko'ra olmasa (internet sekinligi, <mark style="color:red;">`src`</mark> atributidagi xatolik yoki foydalanuvchi ekranni o'qish vositasidan foydalansa) <mark style="color:red;">`alt`</mark> atributi rasm uchun berilgan matnni ko'rsatadi.

Alt attributiga kiritilgan matn rasmni tasvirlab berishi kerak:

{% code title="Misol" %}
```html
<img src="img_chania.jpg" alt="Flowers in Chania"> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_alt_chania" %}

Agar brauzer rasmni topa olmasa, `alt` attributining qiymatiga kiritilgan matnni ko'rsatadi:

{% code title="Misol" %}
```html
<img src="wrongname.gif" alt="Flowers in Chania"> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_wrongname" %}

{% hint style="warning" %}
**Maslahat:** Ekranni oʻqib beruvchi dasturlar HTML kodni oʻqiydi va foydalanuvchiga kontentni “eshitish” imkonini beradi. Ekranni o'qib beruvchi dasturlar ko'rish qobiliyati zaif yoki o'rganish imkoniyati cheklangan odamlar uchun foydalidir.
{% endhint %}

## <mark style="color:green;">Rasm o'lchami - Width va Height</mark>

<mark style="color:red;">`style`</mark> attributidan foydalanib rasmning eni va balandlik o'lchamini berishingiz mumkin.

{% code title="Misol:" %}
```html
<img src="img_girl.jpg" alt="Girl in a jacket" style="width:500px;height:600px;"> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_size" %}

<mark style="color:red;">`width`</mark> va <mark style="color:red;">`height`</mark> attributlari bilan ham buni boshqacharoq ko'rinishda amalga oshirishingiz mumkin.

{% code title="Misol:" %}
```html
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600"> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_attributes" %}

<mark style="color:red;">`width`</mark> va <mark style="color:red;">`height`</mark> attributlari rasmning eni va balandlgini pixellarda qabul qiladi.

{% hint style="warning" %}
**Eslatma:** Har doim rasmning eni va balandligini belgilang. Agar uning eni va balandligi ko'rsatilmagan bo'lsa, rasm yuklanayotganda veb-sahifa miltillashi mumkin.
{% endhint %}

## <mark style="color:green;">Width va Height yoki Stylemi ?</mark>

width, height va style atributlarining barchasi HTMLda to'g'ri ishlaydi.

Lekin, biz <mark style="color:red;">`style`</mark> atributdan foydalanishni maslahat beramiz. U CSS orqali o'zgartirilgan o'lchamlar sabab rasmning o'lchami o'zgarib ketishini oldini oladi:

{% code title="Misol:" %}
```html
<!DOCTYPE html>
<html>
<head>
<style>
img {
  width: 100%;
}
</style>
</head>
<body>

<img src="html5.gif" alt="HTML5 Icon" width="128" height="128">

<img src="html5.gif" alt="HTML5 Icon" style="width:128px;height:128px;">

</body>
</html> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_style" %}

## <mark style="color:green;">Boshqa papkadagi rasmlar</mark>

Agar sizning rasmlaringiz boshqa  ichkipapkalarda bo'lsa papka nomini `src` attributiga kiritishingiz kerak:

{% code title="Misol:" %}
```html
<img src="/images/html5.gif" alt="HTML5 Icon" style="width:128px;height:128px;"> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_folder" %}

## <mark style="color:green;">Boshqa server/veb-saytdagi rasmlar</mark>

Ba'zi web saytlar boshqa serverdagi rasmlarni ko'rsatadi.

Boshqa serverdagi rasmni ko'rsatish uchun <mark style="color:red;">`src`</mark> atributida to'liq URL manzilni ko'rsatishingiz kerak:

{% code title="Misol" %}
```html
<img src="https://www.w3schools.com/images/w3schools_green.jpg" alt="W3Schools.com"> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_w3schools" %}

**Tashqi rasmlar bo'yicha eslatmalar:** tashqi rasmlar mualliflik huquqi ostida bo'lishi mumkin. Agar siz undan foydalanishga ruxsat olmagan bo'lsangiz, mualliflik huquqi qonunlarini buzgan bo'lishingiz mumkin. Bundan tashqari, siz tashqi rasmlarni nazorat qila olmaysiz; ular to'satdan olib tashlanishi yoki o'zgartirilishi mumkin.

## <mark style="color:green;">Animatsiyali rasmlar</mark>

HTML animatsiyali GIFlarni qabul qiladi:

```html
<img src="programming.gif" alt="Computer Man" style="width:48px;height:48px;">
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_hackman" %}

## <mark style="color:green;">Havola sifatidagi rasm</mark>

Rasmdan havola sifatida foydalanish uchun <mark style="color:red;">`<img>`</mark> tegini <mark style="color:red;">`<a>`</mark> tegining ichiga joylash kerak:

```html
<a href="default.asp">
  <img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">
</a> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_link" %}

## <mark style="color:green;">Floating (suzuvchi) rasm</mark>

Rasm matnning o'ng yoki chap tomonida turishi uchun CSSning <mark style="color:red;">`float`</mark> xususiyatidan foydalaning:

```html
<p>
<img src="smiley.gif" alt="Smiley face" style="float:right;width:42px;height:42px;">
The image will float to the right of the text.
</p>

<p>
<img src="smiley.gif" alt="Smiley face" style="float:left;width:42px;height:42px;">
The image will float to the left of the text.
</p> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_float" %}

## <mark style="color:green;">Rasmlarning umumiy format turlari</mark>

Bu yerda barcha brauzerlarda (Chrome, Edge, Firefox, Safari, Opera) qo'llab-quvvatlanadigan eng keng tarqalgan rasm format turlari ko'rsatilgan:

| Qisqartma | Fayl formati                          | Fayl kengaytmasi                 |
| --------- | ------------------------------------- | -------------------------------- |
| APNG      | Animated Portable Network Graphics    | .apng                            |
| GIF       | Graphics Interchange Format           | .gif                             |
| ICO       | Microsoft Icon                        | .ico, .cur                       |
| JPEG      | Joint Photographic Expert Group image | .jpg, .jpeg, .jfif, .pjpeg, .pjp |
| PNG       | Portable Network Graphics             | .png                             |
| SVG       | Scalable Vector Graphics              | .svg                             |

## <mark style="color:green;">Bo'lim hulosasi</mark>

* Rasmni ko'rsatish uchun HTMLning <mark style="color:red;">`<img>`</mark> elementidan foydalaning
* Rasmning joylashuvini ko'rsatish uchun HTMLning <mark style="color:red;">`src`</mark> attributidan foydalaning
* Rasm ko'rinmay qolganida u haqidagi matnni ko'rsatish uchun HTMLning <mark style="color:red;">`alt`</mark> attributidan foydalaning
* Rasmning o'lchamini berish uchun HTMLning width va height attributlaridan yoki CSS ning width va height xususiyatlaridan foydalaning
* Rasm o'ng yoki chap tomonga turishi uchun CSS ning float xususiyatidan foydalaning

{% hint style="warning" %}
**Eslatma:** Katta hajmdagi rasmlarni yuklash biroz vaqt talab qilishi va veb-sahifangizni sekinlashtirishi mumkin. Rasmlardan ehtiyotkorlik bilan foydalaning.
{% endhint %}

## <mark style="color:green;">Rasmga aloqador teglar</mark>

| Teg        | Tavsif                                          |
| ---------- | ----------------------------------------------- |
| \<img>     | Rasmni joylashtirish                            |
| \<map>     | Rasm xaritasini ifodalash                       |
| \<area>    | Rasm xaritasidagi bosiluvchi maydonni belgilash |
| \<picture> | Resurslarda bir nechta rasmlarni joylashtirish  |
