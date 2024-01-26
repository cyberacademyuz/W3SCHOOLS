# Boshlang'ich

Bu bo'limda ba'zi boshlang'ich HTML misollarini ko'rsatamiz.

Agar biz, siz o'rganmagan teglardan foydalansak xavotir olmang.

## <mark style="color:green;">HTML Hujjatlar</mark>

Barcha HTML hujjatlari hujjat turini belgilovchi <mark style="color:red;">\<! DOCTYPE html></mark> tegi bilan boshlanishi kerak.

HTML - hujjatning o'zi <mark style="color:red;">`<html>`</mark> bilan boshlanadi va <mark style="color:red;">`</html>`</mark> bilan tugaydi.

HTML hujjatdagi ma'lumotlarning brauzerda ko'rinadigan qismi <mark style="color:red;">`<body>`</mark> va <mark style="color:red;">**`</body>`**</mark> teglari orasida joylashadi.

```html
<!DOCTYPE html>
<html>
<body>

<h1>Mening birinchi sarlavham</h1>
<p>Mening birinchi paragrafim</p>

</body>
</html> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_basic_document" %}

### <mark style="color:green;">\<!DOCTYPE> deklaratsiyasi</mark>

<mark style="color:red;">`<!DOCTYPE>`</mark> deklaratsiyasi hujjat turini ifodalaydi, ya'ni brauzerga bu hujjat HTML5da yozilganligini bildiradi va brauzerlarga veb-sahifalarni to'g'ri ko'rsatishga yordam beradi.

U faqat bir marta, sahifaning yuqori qismida (barcha HTML teglaridan oldin) yozilishi kerak.

<mark style="color:red;">`<!DOCTYPE>`</mark> deklaratsiyasida harflarning katta-kichiklikligi ahamiyatsiz.

HTML5 uchun <mark style="color:red;">`<!DOCTYPE>`</mark> deklaratsiyasi:

```html
<!DOCTYPE html>
```

### <mark style="color:green;">HTML Sarlavhalar</mark>

HTML sarlavhalari <mark style="color:red;">\<h1></mark> tegidan <mark style="color:red;">\<h6></mark> teg-gacha ifodalaniladi.

`<h1>` muhim sarlavhalar uchun ishlatiladi, `<h6>` esa uncha muhim bo'lmagan sarlavhalar uchun ishlatiladi:

```html
<h1>Bu 1 - sarlavha</h1>
<h2>Bu 2 - sarlavha</h2>
<h3>Bu 3 - sarlavha</h3> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_basic_headings" %}

### <mark style="color:green;">HTML paragraf</mark>

HTML paragraflari `<p>` tegi bilan ifodalanadi.

```html
<p>Bu paragraf</p>
<p>Bu boshqa paragraf</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_basic_paragraphs" %}

### <mark style="color:green;">HTML havolalar</mark>

HTML havolalar <mark style="color:red;">\<a></mark> tegi bilan yaratiladi.

```html
 <a href="https://www.w3schools.com">Bu havola</a>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_basic_link" %}

Havolaning qaysi manzilga yo'naltirilishi <mark style="color:red;">href</mark> atributida ko'rsatiladi.

Atributlar HTML elementlari haqida qo'shimcha ma'lumot berish uchun ishlatiladi.

Atributlar haqida keyingi darslarda ko'proq ma'lumot olasiz.

### <mark style="color:green;">HTML Rasmlar</mark>

HTMLda rasmlar <mark style="color:red;">\<img></mark> tegi yordamida qo'shiladi.

Rasmning fayl joylashuvi <mark style="color:red;">`src`</mark> atributiga beriladi. Rasm haqida qisqacha ma'lumot <mark style="color:red;">`alt`</mark> attributida, rasmning kengligi <mark style="color:red;">`width`</mark> va eni <mark style="color:red;">`height`</mark> attributi yordamida amalga oshiriladi.

```html
<img src="w3schools.jpg" alt="W3Schools.com" width="104" height="142"> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_basic_img" %}

### <mark style="color:green;">HTML manbalarini (source code-larni) qanday ko'rish mumkin ?</mark>

Biror bir veb-sahifaning html code-larini ko'rish uchun kompyuteringizdagi f12 tugmasini bosing.

Yoki bo'lmasam sichqonchaning o'ng tugmasini bosganingizda paydo bo'lgan menyudan "**inspect**" bo'limini tanlash orqali ko'rish mumkin.

Yana bir yo'li esa `ctrl + shift + i` yoki `ctrl + shift + c` tugmalarini bosgan holda ko'rish imkoniyatiga ega bo'lasiz.
