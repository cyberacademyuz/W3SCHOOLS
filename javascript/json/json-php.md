# JSON PHP

JSON-dan keng tarqalgan foydalanish usuli veb-serverdan ma'lumotlarni olish va ularni veb-sahifada ko'rsatish hisoblanadi.

Ushbu bo'lim sizga Brauzer va PHP serveri o'rtasida JSON ma'lumotlarini qanday almashishni o'rgatadi.

### PHP fayl

PHP da JSON bilan ishlash uchun baʼzi built-in funksiyalar mavjud.

PHPning `json_encode()` funksiyasi yordamida PHP-dagi obyektlar JSON-ga aylantirilishi mumkin:

{% code title="php fayl" %}
```
<?php
$myObj->name = "John";
$myObj->age = 30;
$myObj->city = "New York";

$myJSON = json_encode($myObj);

echo $myJSON;
?>
```
{% endcode %}

### Client JavaScript

Manabu yuqoridagi misoldan PHP faylini so'rash uchun AJAX chaqiruvidan foydalanadigan brazerdagi JavaScript:

{% code title="Natijani JavaScript obyektiga aylantirish uchun JSON.parse() dan foydalaning:" %}
```
const xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myObj = JSON.parse(this.responseText);
  document.getElementById("demo").innerHTML = myObj.name;
}
xmlhttp.open("GET", "demo_file.php");
xmlhttp.send();
```
{% endcode %}

### PHP Massiv

PHP `json_encode()` funksiyasidan foydalanganda PHP-dagi massivlar ham JSONga aylantiriladi:

{% code title="php fayl" %}
```
<?php
$myArr = array("John", "Mary", "Peter", "Sally");

$myJSON = json_encode($myArr);

echo $myJSON;
?>
```
{% endcode %}

### Client JavaScript

Mana yuqoridagi massiv misolidan PHP faylini so'rash uchun AJAX chaqiruvidan foydalanadigan brauzerdagi JavaScript:

{% code title="Natijani JavaScript massiviga aylantirish uchun JSON.parse() dan foydalaning:" %}
```
var xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myObj = JSON.parse(this.responseText);
  document.getElementById("demo").innerHTML = myObj[2];
}
xmlhttp.open("GET", "demo_file_array.php", true);
xmlhttp.send();
```
{% endcode %}

### PHP ma'lumotlar bazasi

PHP server-side dasturlash tili bo'lib, ma'lumotlar bazasiga murojaat qilish uchun ishlatilishi mumkin.

Serveringizda ma'lumotlar bazasi bor deb tasavvur qiling va unga brauzerdan "clients" deb nomlangan jadvalning birinchi 10 ta qatorini so'raydigan request yubormoqchisiz.

Clientda siz qaytarmoqchi bo'lgan qatorlar sonini tavsiflovchi JSON obyektini yarating.

So'rovni serverga yuborishdan oldin, JSON obyektini stringga aylantiring va uni PHP sahifasining url manziliga parametr sifatida yuboring:

{% code title="JavaScript obyektini JSONga aylantirish uchun JSON.stringify() dan foydalaning:" %}
```
const limit = {"limit":10};
const dbParam = JSON.stringify(limit);
xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  document.getElementById("demo").innerHTML = this.responseText;
}
xmlhttp.open("GET","json_demo_db.php?x=" + dbParam);
xmlhttp.send();
```
{% endcode %}

#### Misolni tushuntirish:

* "limit" xususiyatini va qiymatini o'z ichiga olgan obyekt yarating.
* Obyektni JSON stringiga aylantiring.
* Parametr sifatida JSON stringi bilan PHP fayliga so'rov yuboring.
* request response bilan qaytguncha kuting (JSON sifatida)
* PHP faylidan olingan natijani ko'rsating.

PHP faylini ko'rib chiqing:

{% code title="php fayl" %}
```
<?php
header("Content-Type: application/json; charset=UTF-8");
$obj = json_decode($_GET["x"], false);

$conn = new mysqli("myServer", "myUser", "myPassword", "Northwind");
$stmt = $conn->prepare("SELECT name FROM customers LIMIT ?");
$stmt->bind_param("s", $obj->limit);
$stmt->execute();
$result = $stmt->get_result();
$outp = $result->fetch_all(MYSQLI_ASSOC);

echo json_encode($outp);
?>
```
{% endcode %}

#### PHP faylni tushuntirish:

* PHP json\_decode() funktsiyasidan foydalanib, requestni obyektga aylantiradi.
* Ma'lumotlar bazasiga murojaat qiladi va massivni so'ralgan ma'lumotlar bilan to'ldiradi
* Massivni obyektga qo'shing va json\_encode() funktsiyasidan foydalanib obyektni JSON sifatida qaytaradi.

### Ma'lumotlardan foydalanish

```
xmlhttp.onload = function() {
  const myObj = JSON.parse(this.responseText);
  let text = "";
  for (let x in myObj) {
    text += myObj[x].name + "<br>";
  }
  document.getElementById("demo").innerHTML = text;
}
```

### PHP Method = POST

Serverga ma'lumotlarni jo'natishda odatda HTTPning`POST` metodidan foydalanish yaxshi.

`POST` metodi yordamida AJAX so'rovlarini yuborish uchun metod va to'g'ri header belgilang.

Serverga yuborilgan ma'lumotlar endi `send()` metodiga argument bo'lishi kerak:

```
const dbParam = JSON.stringify({"limit":10});
const xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myObj = JSON.parse(this.responseText);
  let text ="";
  for (let x in myObj) {
    text += myObj[x].name + "<br>";
  }
  document.getElementById("demo").innerHTML = text;
}
xmlhttp.open("POST", "json_demo_db_post.php");
xmlhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
xmlhttp.send("x=" + dbParam);
```

PHP faylidagi yagona farq - uzatilgan ma'lumotlarni olish usuli.

{% code title="php fayl: $_GET oʻrniga $_POST dan foydalaning:" %}
```
<?php
header("Content-Type: application/json; charset=UTF-8");
$obj = json_decode($_POST["x"], false);

$conn = new mysqli("myServer", "myUser", "myPassword", "Northwind");
$stmt = $conn->prepare("SELECT name FROM customers LIMIT ?");
$stmt->bind_param("s", $obj->limit);
$stmt->execute();
$result = $stmt->get_result();
$outp = $result->fetch_all(MYSQLI_ASSOC);

echo json_encode($outp);
?>
```
{% endcode %}
