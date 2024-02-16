---
description: HTMLning <ul> elementi tartiblanmagan ro'yxat yaratadi
---

# Tartiblanmagan ro'yxat

## <mark style="color:green;">Tartiblanmagan ro'yhat</mark>

Tartiblanmagan ro'yxatlar <mark style="color:red;">`<ul>`</mark> tegi bilan boshlanadi. Ro'yhatning har bir elementi <mark style="color:red;">`<li>`</mark> tegi ichida bo'ladi.

Ro'yhatning har bir elementining oldida kichik qora aylana bo'ladi.

```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_unordered2" %}

## <mark style="color:green;">Tartiblanmagan ro'yxat - Ro'yxat oldidagi belgilarni o'zgartirish</mark>

Cssning <mark style="color:red;">`list-style-type`</mark> xususiyatidan foydalanib ro'yxat elementilarining oldidagi belgini o'zgartirishingiz mumkin. Uahbu xususiyatning qiymatlari quyidagilardir:

| Qiymat | Tarif                                            |
| ------ | ------------------------------------------------ |
| disc   | Ro'yxat elementlarining standart belgi           |
| circle | Ro'yxat elementlariga aylana belgi qo'yadi       |
| square | Ro'yxat elementlariga kvadrat belgi qo'yadi      |
| none   | Ro'yxat elementlaridan belgilarni olib tashlaydi |

{% code title="Disc ga misol" %}
```html
<ul style="list-style-type:disc;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_unordered_disc" %}

{% code title="Circle ga misol" %}
```html
<ul style="list-style-type:circle;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_unordered_circle" %}

{% code title="Square ga misol" %}
```html
<ul style="list-style-type:square;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_unordered_square" %}

{% code title="None ga misol" %}
```html
<ul style="list-style-type:none;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_unordered_none" %}

## <mark style="color:green;">HTMLdagi ichki ro'yxatlar</mark>

Ro'yxatlar ichma ich ham bo'lishi mumkin (ro'yxat ichida ro'yxat)

```html
<ul>
  <li>Coffee</li>
  <li>Tea
    <ul>
      <li>Black tea</li>
      <li>Green tea</li>
    </ul>
  </li>
  <li>Milk</li>
</ul> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_nested" %}

{% hint style="warning" %}
**Eslatma**: Roʻyxat elementi (<mark style="color:red;">`<li>`</mark>) yangi roʻyxatni hamda rasmlar va havolalar kabi boshqa HTML elementlarini ham oʻz ichiga olishi mumkin.
{% endhint %}

## <mark style="color:green;">CSS orqali gorizontal ro'yxat</mark>

HTML ro'yxatlarini CSS yordamida turli xil ko'rinishga keltirish mumkin.

Bulardan eng mashhuri  - navbar yaratish uchun ro'yxatni gorizontal ko'rinishga keltirishdir

```html
<!DOCTYPE html>
<html>
<head>
<style>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #111111;
}
</style>
</head>
<body>

<ul>
  <li><a href="#home">Home</a></li>
  <li><a href="#news">News</a></li>
  <li><a href="#contact">Contact</a></li>
  <li><a href="#about">About</a></li>
</ul>

</body>
</html> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_lists_menu" %}

{% hint style="warning" %}
**Maslahat**: Bizning CSS o'quv qo'llanmamiz orqali CSS haqida ko'proq narsa o'rganishingiz mumkin.
{% endhint %}

## <mark style="color:green;">Bo'lim xulosasi</mark>

* Tartiblanmagan ro'yxat yaratish uchun <mark style="color:red;">`<ul>`</mark> elementidan foydalaning
* Ro'yxat elementlarining belgisini o'zgartirish uchun CSSning <mark style="color:red;">`list-style-type`</mark> xususiyatidan foydalaning
* Ro'yxat elementlarini yaratish uchun <mark style="color:red;">`<li>`</mark> elementidan foydalaning
* Ro'yxatlar ichma ich bo'lishi ham mumkin
* Ro'yxat elementlari boshqa HTML elementlarini ham o'z ichiga olishi mumkin
* Ro'yxatni gorizontal qilish uchun CSSning <mark style="color:red;">`float:left`</mark> xususiyatidan foydalaning

| Teg   | Tarif                                            |
| ----- | ------------------------------------------------ |
| \<ul> | Tartiblanmagan ro'yxat yaratadi                  |
| \<ol> | Tartiblangan ro'yxat yaratadi                    |
| \<li> | Ro'yxat elementlarini belgilaydi                 |
| \<dl> | Tariflar ro'yxatini belgilaydi                   |
| \<dt> | Ta'riflar ro'yxatidagi atamani belgilaydi        |
| \<dd> | Ta'riflar ro'yxatidagi atama tarifini belgilaydi |
