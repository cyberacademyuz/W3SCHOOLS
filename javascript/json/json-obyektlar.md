# JSON Obyektlar

JSON bu string:

```
'{"name":"John", "age":30, "car":null}'
```

JSON stringida JSON obyektining literali mavjud:

```
{"name":"John", "age":30, "car":null}
```

JSON obyektining belgilari {} jingalak qavslar bilan o'ralgan.

JSON obyektining literallarida kalit/qiymat juftligi mavjud.

Kalitlar va qiymatlar ikki nuqta bilan ajratiladi.

Kalitlar string va qiymatlar JSONda qabul qilinadigan maʼlumot turi boʻlishi kerak:

* string
* raqam
* obyekt
* massiv
* boolean
* null

Har bir kalit/qiymat juftligi vergul bilan ajratiladi.

{% hint style="warning" %}
JSON obyektini "JSON obyekti" deb atash keng tarqalgan xato hisoblanadi.

JSON obekt bo'lishi mumkin emas. JSON bu string formati hisoblanadi.

Ma'lumotlar faqat JSON string formatida bo'ladi. U JavaScript o'zgaruvchisiga aylantirilsagina obyektga aylanadi.
{% endhint %}

### JavaScript obyektlari

JSON obyektining literalidan JavaScript obyektini yaratishingiz mumkin:

```
myObj = {"name":"John", "age":30, "car":null};
```

Odatda JSON stringini parse qilish orqali JavaScript obyektini yarata olasiz:

```
myJSON = '{"name":"John", "age":30, "car":null}';
myObj = JSON.parse(myJSON);
```

### Obyekt qiymatlariga murojaat qilish

Obyekt qiymatlariga nuqta (.) belgisi yordamida murojaat qilishingiz mumkin:

```
const myJSON = '{"name":"John", "age":30, "car":null}';
const myObj = JSON.parse(myJSON);
x = myObj.name;
```

Qavs (\[]) belgisidan foydalanib, obyekt qiymatlariga ham murojaat qilishingiz mumkin:

```
const myJSON = '{"name":"John", "age":30, "car":null}';
const myObj = JSON.parse(myJSON);
x = myObj["name"];
```

### Obyektni tskil qilish

For-in tsikli yordamida obyekt xususiyatlari bo'ylab harakatlanishingiz mumkin:

```
const myJSON = '{"name":"John", "age":30, "car":null}';
const myObj = JSON.parse(myJSON);

let text = "";
for (const x in myObj) {
  text += x + ", ";
}
```

For-in tsiklida xususiyat _qiymatlariga_ murojaat qilish uchun qavs belgisidan foydalaning:

```
const myJSON = '{"name":"John", "age":30, "car":null}';
const myObj = JSON.parse(myJSON);

let text = "";
for (const x in myObj) {
  text += myObj[x] + ", ";
}
```
