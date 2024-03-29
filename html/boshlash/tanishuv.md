# Tanishuv

HTML web sahifalar yaratish uchun standart markuplash tili.

## <mark style="color:green;">HTML o'zi nima ?</mark>

* HTML <mark style="color:green;">**H**</mark>yper <mark style="color:green;">**T**</mark>ext <mark style="color:green;">**M**</mark>arkup <mark style="color:green;">**L**</mark>anguage so'zining qisqa ko'rinishi.
* HTML veb sahifalar yaratish uchun standart belgilashli til.
* HTML veb sahifalarning strukturasini tasvirlaydi.
* HTML bir necha elementlardan tashkil topgan bo'ladi.
* HTML elementlari brauzerlarga kontentni (veb sahifadagi ma'lumotlarni) qanday ko'rsatishni tushuntiradi.
* HTML elementlari kontent qismlarini "bu sarlavha", "bu oddiy matn", "bu havola" kabi belgilab beradi.

## <mark style="color:green;">Oddiy HTML hujjat</mark>

{% tabs %}
{% tab title="HTML" %}
```html
<!DOCTYPE html>
<html>
<head>
<title>Sahifa mavzusi</title>
</head>
<body>

<h1>Mening birinchi sarlavham</h1>
<p>Mening birinchi paragrafim.</p>

</body>
</html> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_intro" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Misol orqali tushuntirish</mark>

* <mark style="color:red;">`<!DOCTYPE html>`</mark> hujjat HTML5 da yozilganini bildiradi.
* <mark style="color:red;">`<html>`</mark> - HTML sahifaning eng asosiy (root) elementi hisoblanadi.
* <mark style="color:red;">`<head>`</mark> - ​veb sahifa haqidagi meta-ma'lumotlarni saqlovchi element. Meta ma'lumotlar haqida keyingi darslarda gaplashamiz.
* <mark style="color:red;">`<title>`</mark> - veb sahifaning nomini saqlovchi element ( sahifa nomi brauzerda ochilgan har bir oynaning sarlavhalar qatorida ko'rsatiladi).
* <mark style="color:red;">`<body>`</mark> - veb sahifaning tana (body) qismidagi foydalanuvchilarga ko'rinadigan sarlavha, paragraflar, rasmlar, havolalar(hyperlink), jadvallar, ro'yxatlar kabi kontentni saqlovchi element.
* <mark style="color:red;">`<h1>`</mark> - eng katta o'lchamdagi sarlavha elementi.
* <mark style="color:red;">`<p>`</mark> - paragraf elementi.

## <mark style="color:green;">HTML elementlari nima ?</mark>

HTML elementlari, biror ma'lumotni o'z ichiga olgan ochiluvchi va yopiluvchi tegni bildiradi.

<mark style="color:blue;">`<`</mark><mark style="color:red;">`tegnomi`</mark><mark style="color:blue;">`>`</mark> Shu yerga biror ma'lumot kiritiladi <mark style="color:blue;">`<`</mark><mark style="color:red;">`/tegnomi`</mark><mark style="color:blue;">`>`</mark>

<mark style="color:blue;">`<`</mark><mark style="color:red;">`h1`</mark><mark style="color:blue;">`>`</mark> Mening birinchi sarlavham <mark style="color:blue;">`<`</mark><mark style="color:red;">`/h1`</mark><mark style="color:blue;">`>`</mark>

<mark style="color:blue;">`<`</mark><mark style="color:red;">`p`</mark><mark style="color:blue;">`>`</mark> Mening birinchi paragrafim <mark style="color:blue;">`<`</mark><mark style="color:red;">`/p`</mark><mark style="color:blue;">`>`</mark>

<table><thead><tr><th width="265.3333333333333">Ochiluvchi teg</th><th>Element kontenti</th><th>Yopiluvchi teg</th></tr></thead><tbody><tr><td><code>&#x3C;h1></code></td><td>Mening birinchi sarlavham</td><td>&#x3C;/h1></td></tr><tr><td><code>&#x3C;p></code></td><td>Mening birinchi paragrafim</td><td>&#x3C;/p></td></tr><tr><td><code>&#x3C;br></code></td><td>Yozilmaydi</td><td>Yozilmaydi</td></tr></tbody></table>

{% hint style="warning" %}
**Eslatma:**

Ba'zi HTML elementlarida kontent bo'lmaydi (\<br> elementi kabi) Bu elementlar bo'sh elementlar deyiladi. Bo'sh elementlarda yopiluvchi teg ham bo'lmaydi.
{% endhint %}

## <mark style="color:green;">Veb brauzerlar</mark>

Veb-brauzerlar (Chrome, Safari, Firefox, Edge, Opera) HTML hujjatlarni o'qib, ulardagi ma'lumotni foydalanuvchiga to'g'rilab ko'rsatuvchi maxsus dasturlardir.

<figure><img src="../../.gitbook/assets/image (766).png" alt=""><figcaption></figcaption></figure>

HTML sahifa strukturasi

Pastdagi suratda HTML sahifasining vizual strukturasi:

<figure><img src="../../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Eslatma:** ​Brauzerda faqatgina `<body>` tegi ichidagi kontent (yuqorida turgan rasmdagi oq rangli qism) ko'rinadi. `<title>` elementi ichidagi kontent esa brauzerning tab qismida ko'rinadi.
{% endhint %}

## <mark style="color:green;">HTML tarixi</mark>

|      |                                      |
| ---- | ------------------------------------ |
| 1989 | Tim Berners-Lee www-ni ixtiro qildi  |
| 1991 | Tim Berners-Lee HTML-ni ixtiro qildi |
| 1993 | Dave Raggett HTML+ ni chiqardi       |
| 1995 | HTML Working Group HTML 2.0L         |
| 1997 | W3C tavsiyasi: HTML 3.2              |
| 1999 | W3C tavsiyasi: HTML 4.01             |
| 2000 | W3C tavsiyasi: XHTML 1.0             |
| 2008 | WHATWG HTML5                         |
| 2012 | WHATWG HTML5 standartlari            |
| 2014 | W3C tavsiyasi: HTML5                 |
| 2016 | W3C kandidat tavsiyasi: HTML5.1      |
| 2017 | W3C tavsiyasi: HTML5.1 2-nashr       |
| 2017 | W3C tavsiyasi: HTML5.2               |
