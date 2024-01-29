# AJAX Database

AJAX ma'lumotlar bazasi bilan interaktiv aloqa uchun ishlatilishi mumkin.

### AJAX ma'lumotlar bazasi misoli

Quyidagi misol veb-sahifa qanday qilib AJAX yordamida ma'lumotlar bazasidan ma'lumot olishi mumkinligini ko'rsatadi:

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

### Misolni tushuntirish - showCustomer() funksiyasi

Agar foydalanuvchi yuqoridagi dropdown ro'yxatida biror mijozni tanlasa, `showCustomer()` funksiyasi bajariladi. Funksiya `onchange` hodisasi tomonidan ishga tushiriladi:

```
function showCustomer(str) {
  if (str == "") {
    document.getElementById("txtHint").innerHTML = "";
    return;
  }
  const xhttp = new XMLHttpRequest();
  xhttp.onload = function() {
    document.getElementById("txtHint").innerHTML = this.responseText;
  }
  xhttp.open("GET", "getcustomer.php?q="+str);
  xhttp.send();
}
```

`showCustomer()` funksiyasi quyidagilarni bajaradi:

* Mijoz tanlanganligini tekshirish
* `XMLHttpRequest` obyektini yaratish
* Server response-i tayyor bo'lganda ishga tushadigan funksiyani yaratish
* Reuqestni serverdagi faylga yuborish
* URL manziliga parametr (q) qo'shilganiga e'tibor bering

### AJAX Server sahifasi

Yuqorida JavaScript tomonidan chaqirilgan serverdagi sahifa "getcustomer.php" nomli PHP fayldir.

"getcustomer.php" dagi kod ma'lumotlar bazasiga qarshi so'rovni bajaradi va natijani HTML jadvaliga qaytaradi:

```
<?php
$mysqli = new mysqli("servername", "username", "password", "dbname");
if($mysqli->connect_error) {
  exit('Could not connect');
}

$sql = "SELECT customerid, companyname, contactname, address, city, postalcode, country
FROM customers WHERE customerid = ?";

$stmt = $mysqli->prepare($sql);
$stmt->bind_param("s", $_GET['q']);
$stmt->execute();
$stmt->store_result();
$stmt->bind_result($cid, $cname, $name, $adr, $city, $pcode, $country);
$stmt->fetch();
$stmt->close();

echo "<table>";
echo "<tr>";
echo "<th>CustomerID</th>";
echo "<td>" . $cid . "</td>";
echo "<th>CompanyName</th>";
echo "<td>" . $cname . "</td>";
echo "<th>ContactName</th>";
echo "<td>" . $name . "</td>";
echo "<th>Address</th>";
echo "<td>" . $adr . "</td>";
echo "<th>City</th>";
echo "<td>" . $city . "</td>";
echo "<th>PostalCode</th>";
echo "<td>" . $pcode . "</td>";
echo "<th>Country</th>";
echo "<td>" . $country . "</td>";
echo "</tr>";
echo "</table>";
?>
```
