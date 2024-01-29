# JSON Server

Veb-server bilan ma'lumot almashish JSON-dan foydalanishning keng tarqalgan usuli hisoblanadi.

Veb-serverdan ma'lumotlarni qabul qilishda ma'lumotlar doimo string bo'ladi.

Ma'lumotni `JSON.parse()` bilan parse qiling va ma'lumotlar JavaScript obyektiga aylanadi.

### Ma'lumotlarni yuborish

Agar JavaScript obyektida saqlangan ma'lumotlaringiz bo'lsa, obyektni JSONga o'zgartirishingiz va uni serverga yuborishingiz mumkin:

```
const myObj = {name: "John", age: 31, city: "New York"};
const myJSON = JSON.stringify(myObj);
window.location = "demo_json.php?x=" + myJSON;
```

### Ma'lumotlarni qabul qilish

Agar ma'lumotlarni JSON formatida olsangiz, uni osongina JavaScript obyektiga aylantirishingiz mumkin:

```
const myJSON = '{"name":"John", "age":31, "city":"New York"}';
const myObj = JSON.parse(myJSON);
document.getElementById("demo").innerHTML = myObj.name;
```

### Serverdan JSON

AJAX so'rovidan foydalanib serverdan ma'lumotlarni JSON formatida so'rashingiz mumkin

Serverdan JSON formatida kelgan string ma'lumotlarni, JavaScript obyektiga parse qilishingiz mumkin.

{% code title="Serverdan ma'lumotlarni olish uchun XMLHttpRequest dan foydalaning:" %}
```
const xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myObj = JSON.parse(this.responseText);
  document.getElementById("demo").innerHTML = myObj.name;
};
xmlhttp.open("GET", "json_demo.txt");
xmlhttp.send();
```
{% endcode %}

[json\_demo.txt](https://www.w3schools.com/js/json\_demo.txt)ni ko'ring

### Massivdan JSON sifatida  foydalanish

`JSON.parse()` dan massivdan olingan JSON da foydalanilganda, metod obyekt o‘rniga massiv qaytaradi.

{% code title="JSON serverdan massiv sifatida qaytdi:" %}
```
const xmlhttp = new XMLHttpRequest();
xmlhttp.onload = function() {
  const myArr = JSON.parse(this.responseText);
  document.getElementById("demo").innerHTML = myArr[0];
  }
}
xmlhttp.open("GET", "json_demo_array.txt", true);
xmlhttp.send();json_demo_array.txt ga qarang
```
{% endcode %}
