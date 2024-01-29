# DOM Metodlar

DOM metodlari HTML elementlarida bajarishingiz mumkin bo'lgan **harakatlar** hisoblanadi.

DOM xususiyatlari - bu HTML elementlarida belgilashingiz yoki o'zgartirishingiz mumkin bo'lgan **qiymatlar**dir.

### DOM dasturlash interfeysi

DOM ga JavaScript (va boshqa dasturlash tillari) orqali murojaat qilish mumkin.

DOMda barcha HTML elementlari **obyekt** sifatida yaratiladi.

Dasturlash interfeysi har bir obeyktning xususiyatlari va metodlaridir.

Xususiyat siz olishingiz yoki belgilashingiz mumkin bo'lgan qiymatdir (masalan, HTML elementining kontentini o'zgartirish).

Metod - bu bajarishingiz mumkin bo'lgan harakat (masalan , HTML elementini qo'shish yoki o'chirish).

### Misol

Quyidagi misol `<p>` elementining tarkibini (`innerHTML`)  `id="demo"` bilan o'zgartiradi:

```
<html>
<body>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = "Hello World!";
</script>

</body>
</html>
```

Yuqoridagi misolda `getElementById` bu **metod**, `innerHTML` esa xususiyatdir.

### getElementById metodi

HTML elementiga murojaat qilishning eng keng tarqalgan usuli bu element `id`sidan foydalanishdir.

Yuqoridagi misolda `getElementById` metodi elementni topish uchun `id="demo"` dan foydalanilgan.

### innerHTML xususiyati

Element tarkibini olishning eng oson yo'li `innerHTML` xususiyatidan foydalanishdir.

`innerHTML` xususiyati HTML elementlarining tarkibini olish yoki almashtirish uchun foydali xususiyat.

{% hint style="warning" %}
innerHTML xususiyati istalgan HTML elementini, jumladan \<html> va \<body>ni olish yoki o'zgartirish uchun ishlatilishi mumkin.
{% endhint %}
