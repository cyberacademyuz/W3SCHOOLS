---
description: HTMLning <ul> elementi tartiblanmagan ro'hat yaratadi
---

# Tartiblanmagan ro'yhat

## Tartiblanmagan ro'yhat

Tartiblanmagan ro'yhatlar `<ul>` tegi bilan boshlanadi. Ro'yhatning har bir elementi `<li>` tegi ichida bo'ladi.

Ro'yhatning har bir elementining oldida kichik qora aylana bo'ladi.

```
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```

## Tartiblanmagan ro'yhat - Ro'yhat oldidagi belgilarni o'zgartirish

Cssning `list-style-type` xususiyatidan foydalanib ro'yhat elementilarining oldidagi belgini o'zgartirishingiz mumkin. Uahbu xusisyatning qiymatlari quyidagilardir:

| Qiymat | Tarif                                            |
| ------ | ------------------------------------------------ |
| disc   | Ro'yhat elementlarining standart belgi           |
| circle | Ro'yhat elementlariga aylana belgi qo'yadi       |
| square | Ro'yhat elementlariga kvadrat belgi qo'yadi      |
| none   | Ro'yhat elementlaridan belgilarni olib tashlaydi |

{% code title="Disc ga misol" %}
```
<ul style="list-style-type:disc;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```
{% endcode %}

{% code title="Circle ga misol" %}
```
<ul style="list-style-type:circle;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```
{% endcode %}

{% code title="Square ga misol" %}
```
ul style="list-style-type:square;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```
{% endcode %}

{% code title="None ga misol" %}
```
<ul style="list-style-type:none;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```
{% endcode %}

## HTMLdagi ichki ro'yhatlar

Ro'yhatlar ichma ich ham bo'lishi mumkin (ro'yhat ichida ro'yhat)

```
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

{% hint style="warning" %}
**Eslatma**: Roʻyxat elementi (`<li>`) yangi roʻyxatni hamda rasmlar va havolalar kabi boshqa HTML elementlarini ham oʻz ichiga olishi mumkin.
{% endhint %}

## CSS orqali gorizontal ro'yhat

HTML ro'yxatlarini CSS yordamida turli xil ko'rinishga keltirish mumkin.

Bulardan eng mashhuri  - navbar yaratish uchun ro'yxatni gorizontal ko'rinishga keltirishdir

```
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

{% hint style="warning" %}
**Maslahat**: Bizning CSS o'quv qo'llanmamiz orqali CSS haqida ko'proq narsa o'rganishingiz mumkin.
{% endhint %}

## Bo'lim xulosasi

* Tartiblanmagan ro'yhat yaratish uchun `<ul>` elementidan foydalaning
* Ro'yhat elementlarining belgisini o'zgartirish uchun CSSning `list-style-type` xususiyatidan foydalaning
* Ro'yhat elementlarini yaratish uchun `<li>` elementidan foydalaning
* Ro'yhatlar ichma ich bo'lishi ham mumkin
* Ro'yhat elementlari boshqa HTML elementlarini ham o'z ichiga olishi mumkin
* Ro'yhatni gorizontal qilish uchun CSSning `float:left` xususiyatidan foydalaning

| Teg   | Tarif                                            |
| ----- | ------------------------------------------------ |
| \<ul> | Tartiblanmagan ro'yhat yaratadi                  |
| \<ol> | Tartiblangan ro'yhat yaratadi                    |
| \<li> | Ro'yhat elementlarini belgilaydi                 |
| \<dl> | Tariflar ro'yhatini belgilaydi                   |
| \<dt> | Ta'riflar ro'yxatidagi atamani belgilaydi        |
| \<dd> | Ta'riflar ro'yxatidagi atama tarifini belgilaydi |
