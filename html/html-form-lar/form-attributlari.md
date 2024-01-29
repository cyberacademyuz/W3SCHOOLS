---
description: Ushbu bobda <form> elementining turli atributlari tushuntirilgan.
---

# Form attributlari

## Action atributi

`action` atributi forma yuborilganda uni qayerga yuborilishini belgilaydi.

Odatda, foydalanuvchi yuborish tugmasini bosganda forma ma'lumotlari serverdagi faylga yuboriladi.

Quyidagi misolda forma ma'lumotlari "action\_page.php" nomli faylga yuboriladi. Ushbu faylda forma ma'lumotlarini boshqaradigan backend kodlari mavjud:

{% code title="Tugma bosilganda forma ma'lumotlarini "action_page.php" manziliga yuboring:" %}
```
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form> 
```
{% endcode %}

**Maslahat:** Agar `action` atributi unutib qoldirilsa, ma'lumotlar shu sahifaning o'ziga yuboriladi.

## Target atributi

`target` atributi forma yuborilgandan so'ng olingan ma'lumotlarni qayerda ko'rsatish kerakligini belgilaydi.

`target` atributi quyidagi qiymatlardan biriga ega bo'ladi:

| Qiymat      | Ta'rif                                                          |
| ----------- | --------------------------------------------------------------- |
| \_blank     | Qabul qilingan ma'lumotlar yangi oynada ko'rsatiladi            |
| \_self      | Qabul qilingan ma'lumotlar joriy oynada ko'rsatiladi            |
| \_parent    | Qabul qilingan ma'lumotlar ota element ramkasida ko'rsatiladi   |
| \_top       | Qabul qilingan ma'lumotlar oynaning to'liq qismida ko'rsatiladi |
| _framename_ | Qabul qilingan ma'lumotlar berilgan iframe-da ko'rsatiladi      |

Target atributining standart qiymati `_self` qabul qilngan ma'lumotlarni joriy oynada ko'rsatilishini ifodalaydi.

{% code title="Bu yerda qabul qilingan ma'lumotlar yangi brauzer tabida ochiladi:" %}
```
<form action="/action_page.php" target="_blank"> 
```
{% endcode %}

## Method atributi

`method` atribut formasi ma'lumotlarini yuborishda ishlatiladigan HTTP turini belgilaydi.

Forma ma'lumotlari  `method="get"`  bilan GET yoki HTTP `method="post"` orqali POST  turi sifatida yuborilishi mumkin.

Forma ma'lumotlarini yuborishda standart HTTP metod GET hisoblanadi.

{% code title="Ushbu misol forma ma'lumotlarini yuborishda GET metodidan foydalanadi:" %}
```
<form action="/action_page.php" method="get"> 
```
{% endcode %}

{% code title="Ushbu misol forma ma'lumotlarini yuborishda POST metodidan foydalanadi:" %}
```
<form action="/action_page.php" method="post">
```
{% endcode %}

GET haqida eslatmalar:

* Forma ma'lumotlarining nom va qiymatini birga URL manziliga qo'shadi
* Maxfiy ma'lumotlarni yuborish uchun hech qachon GET dan foydalanmang! (yuborilgan forma ma'lumotlari URL manzilida ko'rinadi!)
* URL uzunligi cheklangan (2048 belgi)
* U foydalanuvchi natijani bookmark sifatida saqlashi mumkin bo'lgan formani yuborish uchun ishlatiladi
* GET maxfiy bo'lmagan ma'lumotlar uchun yaxshi, masalan Google so'rovlari uchun

POST haqida eslatmalar:

* U HTTP so'rovining asosiy qismiga forma ma'lumotlarini **URL manzilda** ko'rsatilmaydigan tarzda qo'shadi
* POST-da yuboriladigan ma'lumotlar hajmi bo'yicha hech qanday cheklovlar yo'q va katta hajmdagi ma'lumotlarni yuborish uchun ishlatilishi mumkin
* POST bilan yuborilgan arizani bookmark sifatida saqlab qo'yib bo‘lmaydi

{% hint style="warning" %}
**Maslahat:** Agar forma ma'lumotlarida maxfiy yoki shaxsiy ma'lumotlar bo'lsa, har doim POST metodidan foydalaning!
{% endhint %}

## Autocomplete atributi

`autocomplete` atributi  formada avtomatik toʻldirishni yoqish yoki oʻchirish ni belgilaydi.

Avtomatik to'ldirish yoqilgan bo'lsa, brauzer foydalanuvchi avval kiritgan qiymatlar asosida avtomatik ravishda qiymatlarni to'ldiradi.

{% code title="Avtomatik toʻldirish yoqilgan forma:" %}
```
<form action="/action_page.php" autocomplete="on"> 
```
{% endcode %}

## Novalidate atributi

`novalidate` atributi mantiqiy (boolean) atributdir.

Formada `novalidate` atributi bo'lsa, forma ma'lumotlari yuborilganda inputga kiritilgan ma'lumotlarni tekshirmaslik kerakligini bildiradi.

{% code title="Novalidate atributiga ega forma" %}
```
<form action="/action_page.php" novalidate> 
```
{% endcode %}

### Barcha \<form> atributlarining ro'yxati

| Xususiyat      | Ta'rif                                                                                                     |
| -------------- | ---------------------------------------------------------------------------------------------------------- |
| accept-charset | Formani yuborish uchun ishlatiladigan belgilar kodlarini belgilaydi                                        |
| action         | Forma yuborilganda forma ma'lumotlarini qayerga yuborish kerakligini belgilaydi                            |
| autocomplete   | Formada avtomatik toʻldirishni yoqish yoki oʻchirishni belgilaydi                                          |
| enctype        | Forma ma'lumotlarini serverga yuborishda qanday kodlash kerakligini belgilaydi (faqat method="post" uchun) |
| method         | Forma ma'lumotlarini yuborishda ishlatiladigan HTTP metodini belgilaydi                                    |
| name           | Forma nomini belgilaydi                                                                                    |
| novalidate     | Forma yuborilganda inputdagi ma'lumotlar tekshirilmasligi kerakligini bildiradi                            |
| rel            | Ulangan resurs va joriy fayl o'rtasidagi munosabatni belgilaydi                                            |
| target         | Formani yuborgandan so'ng olingan javobni qayerda ko'rsatishni belgilaydi                                  |
