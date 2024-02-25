# CSS Izohlar

CSS izohlari browserda ko'rinmaydi, lekin kodingizni tushunarli qilishga yordam beradi.

## <mark style="color:green;">CSS Izohlar</mark> <a href="#css-izohlari-2" id="css-izohlari-2"></a>

Izohlar kodni qanday ishlashini tushuntirishga yordam beradi va keyinchalik manbaa kodini o'zgartirmoqchi bo'lganingizda ko'mak berishi mumkin.

Izohlar browserlar tomonidan qabul qilinmayd.

CSSning izohlari <mark style="color:red;">`<style>`</mark> elementi ichida yoziladi va <mark style="color:red;">`/*`</mark> bilan boshlanib <mark style="color:red;">`*/`</mark> bilan tugaydi:

{% tabs %}
{% tab title="CSS" %}
```css
/* This is a single-line comment */
p {
  color: red;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_comments" %}
{% endtab %}
{% endtabs %}

Kodning istalgan joyiga izoh qo'shishingiz mumkin:

{% tabs %}
{% tab title="CSS" %}
```css
p {
  color: red;  /* Matn rangini qizil qilish */
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_comments2" %}
{% endtab %}
{% endtabs %}

Hatto kod qatorining o'rtasida ham izohdan foydalanish mumkin:

{% tabs %}
{% tab title="CSS" %}
```css
p {
  color: /*red*/blue; 
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_comments2_2" %}
{% endtab %}
{% endtabs %}

Izohlarni uzunroq qilib yozishingiz ham mumkin:

{% tabs %}
{% tab title="CSS" %}
```css
/* This is
a multi-line
comment */

p {
  color: red;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_comments3" %}
{% endtab %}
{% endtabs %}

## HTML va CSS izohlari <a href="#html-va-css-izohlari" id="html-va-css-izohlari"></a>

HTML darsligida <mark style="color:red;">`<!--...-->`</mark> orqali izoh qo'shishingiz mumkinligini o'rgangan edingiz.

Quyidagi misolda, HTML va CSS izohlarini birlashtiramizmessage = "hello world"

{% tabs %}
{% tab title="CSS" %}
```html
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

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_comments4" %}
{% endtab %}
{% endtabs %}
