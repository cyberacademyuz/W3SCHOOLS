# CSS Izohlar

CSS izohlari browserda ko'rinmaydi, lekin kodingizni tushunarli qilishga yordam beradi.

### CSS Izohlar <a href="#css-izohlari-2" id="css-izohlari-2"></a>

Izohlar kodni qanday ishlashini tushuntirishga yordam beradi va keyinchalik manbaa kodini o'zgartirmoqchi bo'lganingizda ko'mak berishi mumkin.

Izohlar browserlar tomonidan qabul qilinmayd.

CSSning izohlari `<style>` elementi ichida yoziladi va `/*` bilan boshlanib `*/` bilan tugaydi:

```
/* This is a single-line comment */
p {
  color: red;
}
```

Kodning istalgan joyiga izoh qo'shishingiz mumkin:

```
p {
  color: red;  /* Set text color to red */
}
```

Izohlarni uzun qilib yozishingiz ham mumkin:

```
/* This is
a multi-line
comment */

p {
  color: red;
}
```

### HTML va CSS izohlari <a href="#html-va-css-izohlari" id="html-va-css-izohlari"></a>

HTML darsligida `<!--...-->` orqali izoh qo'shishingiz mumkinligini o'rgangan edingiz.

Quyidagi misolda, HTML va CSS izohlarini birlashtiramiz:

```
<!DOCTYPE html>
<html>
<head>
<style>
p {
  color: red; /* Set text color to red */
}
</style>
</head>
<body>

<h2>My Heading</h2>

<!-- These paragraphs will be red -->
<p>Hello World!</p>
<p>This paragraph is styled with CSS.</p>
<p>CSS comments are not shown in the output.</p>

</body>
</html>
```
