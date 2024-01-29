# AJAX Applicationlar

Ushbu bo'limda XML, HTTP, DOM va JavaScript-dan foydalanadigan ba'zi HTML ilovalari ko'rsatilgan.

### Foydalanilgan XML hujjati

Ushbu bobda biz "[cd\_catalog.xml](https://www.w3schools.com/js/cd\_catalog.xml)" deb nomlangan XML faylidan foydalanamiz.

### XML ma'lumotlarini HTML jadvalida ko'rsatish

Ushbu misol har bir \<CD> elementi bo'ylab harakatlanadi va HTML jadvalidagi \<ARTIST> va \<TITLE> elementlarining qiymatlarini ko'rsatadi:

```
<table id="demo"></table>

<script>
function loadXMLDoc() {
  const xhttp = new XMLHttpRequest();
  xhttp.onload = function() {
    const xmlDoc = xhttp.responseXML;
    const cd = xmlDoc.getElementsByTagName("CD");
    myFunction(cd);
  }
  xhttp.open("GET", "cd_catalog.xml");
  xhttp.send();
}

function myFunction(cd) {
  let table="<tr><th>Artist</th><th>Title</th></tr>";
  for (let i = 0; i < cd.length; i++) {
    table += "<tr><td>" +
    cd[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue +
    "</td><td>" +
    cd[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue +
    "</td></tr>";
  }
  document.getElementById("demo").innerHTML = table;
}
</script>

</body>
</html>
```

JavaScript va XML DOM-dan foydalanish haqida batafsil ma'lumot olish uchun [DOM Intro](../js-html-dom/domga-kirish.md)-ga o'ting.

### Birinchi CDni HTMLning \<div> elementida ko'rsatish

Ushbu misolda HTML elementidagi birinchi CD elementini `id="showCD"` atributi orqali ko'rsatish uchun funksiyadan foydalaniladi:

```
const xhttp = new XMLHttpRequest();
xhttp.onload = function() {
  const xmlDoc = xhttp.responseXML;
  const cd = xmlDoc.getElementsByTagName("CD");
  myFunction(cd, 0);
}
xhttp.open("GET", "cd_catalog.xml");
xhttp.send();

function myFunction(cd, i) {
  document.getElementById("showCD").innerHTML =
  "Artist: " +
  cd[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue +
  "<br>Title: " +
  cd[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue +
  "<br>Year: " +
  cd[i].getElementsByTagName("YEAR")[0].childNodes[0].nodeValue;
}
```

### CD lar bo'ylab harakatlanish

Yuqorida turgan misoldagi CD lar orasida harakat qilish uchun `previous()` va `next()` funksiyasini yarating:

```
function next() {
  // display the next CD, unless you are on the last CD
  if (i < len-1) {
    i++;
    displayCD(i);
  }
}

function previous() {
  // display the previous CD, unless you are on the first CD
  if (i > 0) {
    i--;
    displayCD(i);
  }
}
```

### CDni bosganda albom ma'lumotlarini ko'rsatish

Oxirgi misol foydalanuvchi CD-ni bosganida albom ma'lumotlarini qanday ko'rsatilishini ko'rsatadi:

```
function displayCD(i) {
  document.getElementById("showCD").innerHTML =
  "Artist: " +
  cd[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue +
  "<br>Title: " +
  cd[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue +
  "<br>Year: " +
  cd[i].getElementsByTagName("YEAR")[0].childNodes[0].nodeValue;
}
```
