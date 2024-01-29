# Inputning forma attributlari

Ushbu bo'limda HTMLning `<input>` elementi uchun turli `form*` atributlari tasvirlangan.

### Forma atributlari

Inputning  `form`  atributi  `<input>` elementi uchun forma yaratadi.

Bu atributning qiymati u tegishli bo'lgan \<form> elementining id atributiga teng bo'lishi kerak.

```
HTML formasidan tashqarida joylashgan kiritish maydoni (lekin shaklning bir qismi):

<form action="/action_page.php" id="form1">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <input type="submit" value="Submit">
</form>

<label for="lname">Last name:</label>
<input type="text" id="lname" name="lname" form="form1">
```

### formaction atributi

Inputning `formaction` atributi forma yuborilganda inputni qayta ishlovchi faylning URL manzilini belgilaydi.

**Eslatma:** Bu atribut `<form>`  elementining `action` atributini bekor qiladi.

`formaction` atributi quyidagi input turlari bilan ishlaydi: submit va image.

```
Har xil amallarga ega ikkita yuborish tugmasi boʻlgan HTML formasi:
<form action="/action_page.php">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <input type="submit" value="Submit">
  <input type="submit" formaction="/action_page2.php" value="Submit as Admin">
</form>
```

### formenctype atributi

Inputning `formenctype` atributi forma-ma'lumotlari yuborilganda qanday kodlanishi kerakligini belgilaydi (faqat method="post" turidagi formalar uchun).

**Eslatma:** Bu atribut elementning enctype atributini bekor qiladi `<form>`.

`formenctype` atributi quyidagi input turlari bilan ishlaydi: send va image.

```
Ikkita submit tugmasi bo'lgan forma. Birinchisi forma ma'lumotlarini standart kodlash bilan yuboradi, ikkinchisi "ko'p qismli/forma-ma'lumotlar" sifatida kodlangan shakl-ma'lumotlarni yuboradi:

<form action="/action_page_binary.asp" method="post">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <input type="submit" value="Submit">
  <input type="submit" formenctype="multipart/form-data"
  value="Submit as Multipart/form-data">
</form>
```

### formmethod atributi

Inputning `formmethod` atributi action URL manziliga forma ma'lumotlarini yuborish uchun HTTP metodini belgilaydi.

**Eslatma:** Bu atribut `<form>` elementining metod atributini bekor qiladi.

`formmethod` atributi quyidagi input turlari bilan ishlaydi: send va image.

Forma ma'lumotlari URL o'zgaruvchilari (method="get") yoki HTTP post tranzaksiyasi (metod="post") sifatida yuborilishi mumkin.

**"Get" metodi bo'yicha eslatmalar:**

* Ushbu metod forma ma'lumotlarini URL manziliga nom/qiymat juftliklarida qo'shadi
* Bu metod foydalanuvchi natijani belgilamoqchi bo'lgan formalarni yuborish uchun foydali
* URL manzilga qancha maʼlumot joylashtirishingiz mumkin boʻlgan chegara mavjud (bu brauzerga qarab farq qiladi), shu sababdan barcha forma maʼlumotlari toʻgʻri uzatilishiga ishonch hosil qila olmaysiz.
* Hech qachon maxfiy ma'lumotlarni yuborish uchun "get" metodidan foydalanmang! (parol yoki boshqa maxfiy ma'lumotlar brauzerning manzil satrida ko'rinadi)

**"Post" metodi bo'yicha eslatmalar:**

* Ushbu metod forma ma'lumotlarini HTTP post tranzaksiyasi sifatida yuboradi
* “Post” metodi bilan yuborilgan formalarni bookmark qilib bo‘lmaydi
* "Post" metodi "get" dan ko'ra mustahkamroq va xavfsizroqdir va "post" dagi ma'lumotlar hajmi cheklovlarga ega emas.

```
Ikkita yuborish tugmasi bo'lgan shakl. Birinchisi, forma ma'lumotlarini method="get" bilan yuboradi. Ikkinchisi form-ma'lumotlarini method="post" bilan yuboradi:

<form action="/action_page.php" method="get">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <input type="submit" value="Submit using GET">
  <input type="submit" formmethod="post" value="Submit using POST">
</form>
```

### Formtarget atributi

Inputning `formtarget` atributi forma yuborilgandan keyin olingan javobni qayerda ko'rsatishni ko'rsatadigan nom yoki kalit so'zni belgilaydi.

**Eslatma:** Bu atribut `<form>` elementining `target` atributini bekor qiladi.

`formtarget` atributi quyidagi input turlari bilan ishlaydi: send va image.

```
Turli maqsadli oynalarga ega boʻlgan ikkita yuborish tugmasi boʻlgan shakl:

<form action="/action_page.php">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <input type="submit" value="Submit">
  <input type="submit" formtarget="_blank" value="Submit to a new window/tab">
</form>
```

### Formnovalidate atributi

Inputning `formnovalidate` atributi \<input> elementi yuborilganda tasdiqlanmasligi kerakligini bildiradi.

**Eslatma:** Bu atribut `<form>` elementining `novalidate` atributini bekor qiladi.

`formnovalidate` atributi quyidagi inpur turlari bilan ishlaydi: send.

```
Ikkita yuborish tugmasi bo'lgan shakl (tasdiqlangan va tasdiqlanmagan):

<form action="/action_page.php">
  <label for="email">Enter your email:</label>
  <input type="email" id="email" name="email"><br><br>
  <input type="submit" value="Submit">
  <input type="submit" formnovalidate="formnovalidate"
  value="Submit without validation">
</form>
```

### Novalidate atributi

`novalidate` atributi `<form>` elementining atributi hisoblanadi.

Agar novalidate  atributi kiritilsa, u barcha forma ma'lumotlari yuborilganda tasdiqlanmasligi kerakligini bildiradi.

```
Taqdim etilganda hech qanday shakl ma'lumotlari tasdiqlanmasligi kerakligini belgilang:

<form action="/action_page.php" novalidate>
  <label for="email">Enter your email:</label>
  <input type="email" id="email" name="email"><br><br>
  <input type="submit" value="Submit">
</form>
```

### HTMLning form va input elementlari

| Teg                                                                                                                                     | Ta'rif                              |
| --------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| [\<form>](https://www-w3schools-com.translate.goog/tags/tag\_form.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)   | Defines an HTML form for user input |
| [\<input>](https://www-w3schools-com.translate.goog/tags/tag\_input.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Defines an input control            |

HTMLdagi barcha teglarning toʻliq roʻyxatini olish uchun bizning [HTML teg maʼlumotnomamizga](https://www-w3schools-com.translate.goog/tags/default.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) tashrif buyuring.
