# JSON JSONP

JSONP - domenlararo muammolarni o'ylamasdan JSON ma'lumotlarini yuborish usuli.

JSONP `XMLHttpRequest` obyektidan foydalanmaydi.

Uning o'rniga `<script>` tegidan foydalanadi.

### JSONP Kirish

{% hint style="warning" %}
JSONP - JSON Padding degan ma'noni anglatadi.
{% endhint %}

Domenlararo siyosat tufayli boshqa domendan fayl so'rash muammolarga olib kelishi mumkin.

Boshqa domendan tashqi _skript faylini_ so'rashda bu muammo bo'lmaydi.

JSONP bu afzallikdan foydalanadi va fayllarni  `XMLHttpRequest` o'rniga skript tegidan foydalangan holda so'raydi.

```
<script src="demo_jsonp.php">
```

### Server fayli

Serverdagi fayl natijani funksiya chaqiruviga o'tkazadi:

```
<?php
$myJSON = '{ "name":"John", "age":30, "city":"New York" }';

echo "myFunc(".$myJSON.");";
?>
```

Natija parametr sifatida JSON ma'lumotlari bilan "myFunc" nomli funksiya chaqiruvini qaytaradi.

Funksiya clieantda mavjudligiga ishonch hosil qiling.

### JavaScript funksiyasi

"myFunc" nomli funksiya clieant joylashgan va JSON ma'lumotlarini qayta ishlashga tayyor:

```
function myFunc(myObj) {
  document.getElementById("demo").innerHTML = myObj.name;
}
```

### Dinamik skript tegini yaratish

Yuqoridagi misol skript tegini qo'ygan joyingizga qarab sahifa yuklanayotganda "myFunc" funksiyasini bajaradi, lekin bu unchalik qoniqarli emas.

Skript tegi faqat kerak bo'lgandagina yaratilishi kerak:

{% code title="Tugma bosilganda <script> tegini yarating va kiriting:" %}
```
function clickButton() {
  let s = document.createElement("script");
  s.src = "demo_jsonp.php";
  document.body.appendChild(s);
}
```
{% endcode %}

### Dinamik JSONP natijasi

Yuqoridagi misollar hali ham statik hisoblanadi.

PHP fayliga JSON yuborish orqali kodni dinamik qiling va PHP fayl olingan ma'lumotlarga asoslanib JSON obyektini qaytarishiga ruxsat bering.

{% code title="php fayli" %}
```
<?php
header("Content-Type: application/json; charset=UTF-8");
$obj = json_decode($_GET["x"], false);

$conn = new mysqli("myServer", "myUser", "myPassword", "Northwind");
$result = $conn->query("SELECT name FROM ".$obj->$table." LIMIT ".$obj->$limit);
$outp = array();
$outp = $result->fetch_all(MYSQLI_ASSOC);

echo "myFunc(".json_encode($outp).")";
?>
```
{% endcode %}

#### PHP Kodni tushuntirish:

* PHP `json_decode()` funksiyasidan foydalanib, so'rovni obyektga aylantiring
* Ma'lumotlar bazasiga murojaat qiladi va massivni so'ralgan ma'lumotlar bilan to'ldiring
* Massivni obyektga qo'shing
* `json_encode()` funksiyasidan foydalanib massivni JSONga aylantiring
* Qaytuvchi obyektni myFunc() funksiyasi ichiga kiriting

#### JavaScript misoli

{% code title=""myFunc" funksiyasi php faylidan chaqiriladi:" %}
```
const obj = { table: "products", limit: 10 };
let s = document.createElement("script");
s.src = "jsonp_demo_db.php?x=" + JSON.stringify(obj);
document.body.appendChild(s);

function myFunc(myObj) {
  let txt = "";
  for (let x in myObj) {
    txt += myObj[x].name + "<br>";
  }
  document.getElementById("demo").innerHTML = txt;
}
```
{% endcode %}

### Callback funktsiyasi

Agar server faylini nazorat qila olmasangiz, kerakli funksiyani chaqirish uchun server faylini qanday qilib olishingiz mumkin ?

Ba'zan server fayli parametr sifatida callback funktsiyasini taqdim qiladi:

{% code title="php fayli siz topshirgan funktsiyani qayta qo'ng'iroq parametri sifatida chaqiradi:" %}
```
let s = document.createElement("script");
s.src = "jsonp_demo_db.php?callback=myDisplayFunction";
document.body.appendChild(s);
```
{% endcode %}
