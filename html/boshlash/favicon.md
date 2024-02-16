---
description: >-
  Favikon - bu brauzer yorlig'ida sahifa sarlavhasi yonida ko'rsatiladigan
  kichik rasm.
---

# Favicon

## <mark style="color:green;">HTML-ga Favikonni qanday qo'shish mumkin</mark>

O'zingizga yoqqan har qanday rasmdan favikon sifatida foydalanishingiz mumkin. Bundan tashqari, [**favicon.cc**](https://www.favicon.cc) kabi saytlarda ham o'z favikoningizni yaratishingiz mumkin.

{% hint style="warning" %}
**Maslahat:** Favikon kichik rasm, shuning uchun u yuqori kontrastli oddiy rasm bo'lishi kerak.
{% endhint %}

Favikon rasm brauzerning tab sahifa sarlavhasining chap tomonida ko'rsatiladi, masalan:

<figure><img src="../../.gitbook/assets/image (328).png" alt=""><figcaption></figcaption></figure>

Veb-saytingizga favikon qo'yish uchun favikonni veb-serveringizning asosiy papkasiga joylashtiring yoki asosiy papkada boshqa bir **img** nomli **papka** yarating va favikon rasmni o'sha yerga joylashtiring. Favikon rasmining keng tarqalgan nomi "favicon.ico" hisoblanadi.

Keyin "index.html" faylingizga <mark style="color:red;">`<title>`</mark> elementidan so'ng <mark style="color:red;">`<link>`</mark> elementini qo'shing, masalan:

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Page Title</title>
  <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html> 
```

Endi "index.html" faylini saqlab qo'ying va uni brauzeringizga qayta oching. Brauzeringiz tab qismi endi sahifa sarlavhasining chap tomonida favikon rasmingizni ko'rsatishi kerak.

### Favicon fayl formatini qo'llab-quvvatlanishi

Quyidagi jadvalda favikon rasmning fayl formatini qo'llab-quvvatlovchi brauzer va formatlar ko'rsatilgan:

| Brauzer | ICO | PNG | GIF | JPEG | SVG |
| ------- | --- | --- | --- | ---- | --- |
| Edge    | Ha  | Ha  | Ha  | Ha   | Ha  |
| Chrome  | Ha  | Ha  | Ha  | Ha   | Ha  |
| Firefox | Ha  | Ha  | Ha  | Ha   | Ha  |
| Opera   | Ha  | Ha  | Ha  | Ha   | Ha  |
| Safari  | Ha  | Ha  | Ha  | Ha   | Ha  |

### Bo'lim xulosasi

* Favikon kiritish uchun HTMLning <mark style="color:red;">`<link>`</mark> elementidan foydalaning

## HTML havola teglari

| Teg     | Ta'rif                                                  |
| ------- | ------------------------------------------------------- |
| \<link> | Sahifa va tashqi resurs o'rtasini bog'lashni ifodalaydi |
