# DOM Formalar

### Forma tekshiruvi

HTML formasini tekshirish JavaScript orqali amalga oshirilishi mumkin.

Agar forma maydoni (fname) bo'm bo'sh bo'lsa, bu funksiya ogohlantirish habarini ko'rsatadi va forma yuborilishiga yo'l qo'ymaslik uchun "false" qaytaradi:

```
function validateForm() {
  let x = document.forms["myForm"]["fname"].value;
  if (x == "") {
    alert("Name must be filled out");
    return false;
  }
}
```

Forma topshirilganda funksiya chaqirilishi mumkin:

```
<form name="myForm" action="/action_page.php" onsubmit="return validateForm()" method="post">
Name: <input type="text" name="fname">
<input type="submit" value="Submit">
</form>
```

### JavaScript raqamli inputni tekshirishi mumkin

JavaScript ko'pincha raqamli inputni tekshirish uchun ishlatiladi:

Iltimos, 1 dan 10 gacha raqam kiriting

### HTML formasini avtomatik tekshirish

HTML formasini tekshirish brauzer tomonidan avtomatik tarzda amalga oshirilishi mumkin:

Agar forma maydoni (fname) bo'm bo'sh bo'lsa, `required` atributi ushbu formani yuborishga to'sqinlik qiladi:

```
<form action="/action_page.php" method="post">
  <input type="text" name="fname" required>
  <input type="submit" value="Submit">
</form>
```

{% hint style="warning" %}
HTML formasini avtomatik tekshirish Internet Explorer 9 yoki undan oldingi versiyalarida ishlamaydi.
{% endhint %}

### Ma'lumotlarni tekshirish

Ma'lumotlarni tekshirish - bu foydalanuvchi kiritgan ma'lumotlarning hatosiz, to'g'ri va foydali bo'lishini ta'minlash jarayonidir.

Tekshiruv vazifalari:

* foydalanuvchi barcha kerakli maydonlarni to'ldirganmi ?
* foydalanuvchi joriy sanani kiritganmi ?
* foydalanuvchi raqamli inputga matn kiritganmi ?

Ko'pincha ma'lumotlarni tekshirishdan maqsad foydalanuvchining ma'lumotlarni to'g'ri kiritishini ta'minlashdir.

Tasdiqlash ko'plab turli xil usullar bilan tekshirilishi va turli yo'llar bilan ishlatilishi mumkin.

**Server tekshiruvi** berilgan ma'lumot serverga yuborilgandan so'ng veb-server tomonidan amalga oshiriladi.

**Client tekshiruvi** veb-brauzer tomonidan kiritilgan ma'lumotlar veb-serverga yuborilishidan oldin amalga oshiriladi.

### HTML Cheklovni tekshirish

HTML5 **cheklovni tekshirish** deb nomlangan yangi HTML tekshirish kontseptsiyasini taqdim qildi.

HTMLning cheklovlarni tekshirishi quyidagilarga asoslanadi:

* **HTMLning input atributlarida**gi cheklovni tekshirish&#x20;
* **CSS psevdoselektorlarida**gi cheklovni tekshirish&#x20;
* **DOM xususiyatlari va metodlari**dagi cheklovni tekshirish&#x20;

## **HTMLning input atributlarida**gi cheklovni tekshirish

| Atribut  | Ta'rif                                                        |
| -------- | ------------------------------------------------------------- |
| disabled | Input elementini o'chirib qo'yish kerakligini bildiradi       |
| max      | Input elementining maksimal qiymatini belgilaydi              |
| min      | Input elementining minimal qiymatini belgilaydi               |
| pattern  | Input elementining pettern qiymatini belgilaydi               |
| required | Input maydoniga biror ma'lumot kiritish kerakligini bildiradi |
| type     | Input elementining turini belgilaydi                          |

Toʻliq roʻyxatni ko'rish uchun **HTMLning Input atributlari** sahigafasiga oʻting.

### CSS psevdoselektorlaridagi cheklovlarni tekshirish&#x20;

| Selektor  | Ta'rif                                                            |
| --------- | ----------------------------------------------------------------- |
| :disabled | "disabled" atributiga ega barcha input elementlarini tanlaydi     |
| :invalid  | Noto'g'ri qiymatlarga ega input elementlarini tanlaydi            |
| :optional | "required" atribut berilmagan barcha input elementlarini tanlaydi |
| :required | "required" atributiga ega barcha input elementlarini tanlaydi     |
| :valid    | To'g'ri qiymat kiritilgan input elementlarini tanlaydi            |

Toʻliq roʻyxatni ko'rish uchun **CSS Pseudo Classelari** sahifasifaga o'ting.
