# AJAX PHP

AJAX ko'proq interaktiv ilovalar yaratish uchun ishlatiladi.

### AJAX PHPga misol

Quyidagi misol foydalanuvchi input maydoniga belgilar kiritayotganda veb-sahifa veb-server bilan qanday bog'lanishi mumkinligini ko'rsatadi:

<figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

### Misolni tushuntirish

Yuqoridagi misolda foydalanuvchi input maydoniga belgi yozganda, chaqirilgan `showHint()` funksiyasi bajariladi.

Funktsiya `onkeyup` hodisasi tomonidan ishga tushiriladi.

Mana uning kodi:

```
<p>Start typing a name in the input field below:</p>
<p>Suggestions: <span id="txtHint"></span></p>

<form>
First name: <input type="text" onkeyup="showHint(this.value)">
</form>

<script>
function showHint(str) {
  if (str.length == 0) {
    document.getElementById("txtHint").innerHTML = "";
    return;
  } else {
    const xmlhttp = new XMLHttpRequest();
    xmlhttp.onload = function() {
      document.getElementById("txtHint").innerHTML = this.responseText;
    }
  xmlhttp.open("GET", "gethint.php?q=" + str);
  xmlhttp.send();
  }
}
</script>
```

Kodni tushuntirish:

Birinchi, input maydonida hech narsa yo'qligini tekshiring (str.length == 0). Agar rostdan ham hech narsa bo'lmasa, `txtHint` tarkibini tozalang va funksiyadan chiqing.

Ammo input maydonida biror belgi bo'lsa, quyidagilarni bajaring:

* `XMLHttpRequest` obyektini yarating
* Server javobi tayyor bo'lganda bajariladigan funksiyani yarating
* So'rovni serverdagi PHP fayliga (gethint.php) yuboring
* q parametri gethint.php?q="+str kabi qo'shilganiga e'tibor qiling
* str o'zgaruvchisi input maydonining tarkibini saqlaydi

### PHP fayli - "gethint.php"

PHP fayli bir qator ismlarni tekshiradi va brauzerga tegishli ism(lar)ni qaytaradi:

```
<?php
// Array with names
$a[] = "Anna";
$a[] = "Brittany";
$a[] = "Cinderella";
$a[] = "Diana";
$a[] = "Eva";
$a[] = "Fiona";
$a[] = "Gunda";
$a[] = "Hege";
$a[] = "Inga";
$a[] = "Johanna";
$a[] = "Kitty";
$a[] = "Linda";
$a[] = "Nina";
$a[] = "Ophelia";
$a[] = "Petunia";
$a[] = "Amanda";
$a[] = "Raquel";
$a[] = "Cindy";
$a[] = "Doris";
$a[] = "Eve";
$a[] = "Evita";
$a[] = "Sunniva";
$a[] = "Tove";
$a[] = "Unni";
$a[] = "Violet";
$a[] = "Liza";
$a[] = "Elizabeth";
$a[] = "Ellen";
$a[] = "Wenche";
$a[] = "Vicky";

// get the q parameter from URL
$q = $_REQUEST["q"];

$hint = "";

// lookup all hints from array if $q is different from ""
if ($q !== "") {
  $q = strtolower($q);
  $len=strlen($q);
  foreach($a as $name) {
    if (stristr($q, substr($name, 0, $len))) {
      if ($hint === "") {
        $hint = $name;
      } else {
        $hint .= ", $name";
      }
    }
  }
}

// Output "no suggestion" if no hint was found or output correct values
echo $hint === "" ? "no suggestion" : $hint;
?>
```
