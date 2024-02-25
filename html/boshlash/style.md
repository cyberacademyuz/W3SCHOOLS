# Style

HTMLning <mark style="color:red;">`style`</mark> atributi elementlarga rang, shrift, o'lcham kabi stillar berish uchun foydalaniladi.

## <mark style="color:green;">HTMLning</mark> <mark style="color:green;">`style`</mark> <mark style="color:green;">atributi</mark>

HTML elementlariga stil berish <mark style="color:red;">`style`</mark> atributi yordamida amalga oshiriladi.

<mark style="color:red;">`style`</mark> atributining sintaksisi quyidagi ko'rinishda bo'ladi.

```html
<tagname style="property:value;">
```

**Property** CSS xususiyati. **Value** esa xususiyatning qiymati.

{% hint style="warning" %}
Siz bu qo'llanmada CSS haqida ko'p narsa o'rganasiz.
{% endhint %}

## <mark style="color:green;">Background color</mark>

CSSning <mark style="color:red;">`background-color`</mark> xususiyati HTML elementining orqa fon rangini o'zgartiradi.

{% tabs %}
{% tab title="HTML" %}
Sahifa uchun orqa fon rangiga powderblue rangini berish

```html
<body style="background-color:powderblue;">

<h1>Bu sarlavha</h1>
<p>Bu paragraf</p>

</body>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_styles_background-color" %}
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="HTML" %}
Ikkita turli element uchun orqa fon rang berish:

```html
<body>

<h1 style="background-color:powderblue;">Bu sarlavha</h1>
<p style="background-color:tomato;">Bu paragrad</p>

</body>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_styles_background-color2" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Matn rangi</mark>

CSSning <mark style="color:red;">`color`</mark> xususiyati HTML elementning matn rangini o'zgartiadi.

{% tabs %}
{% tab title="HTML" %}
```html
<h1 style="color:blue;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_styles_color" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Shriftlar</mark>

CSSning <mark style="color:red;">`font-family`</mark> xususiyati HTML elementida foydalaniladigan shriftni belgilaydi.

{% tabs %}
{% tab title="HTML" %}
```html
<h1 style="font-family:verdana;">This is a heading</h1>
<p style="font-family:courier;">This is a paragraph.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_styles_font-family" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Matn o'lchami</mark>

CSSning <mark style="color:red;">`font-size`</mark> xususiyati HTML elementidagi matnning o'lchamini o'zgartiadi.

{% tabs %}
{% tab title="HTML" %}
```html
<h1 style="font-size:300%;">This is a heading</h1>
<p style="font-size:160%;">This is a paragraph.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_styles_font-size" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Matn joylashuvi</mark>

CSSning <mark style="color:red;">`text-align`</mark> xususiyati HTML elementidagi matnning tarzdagi joylashuvini belgilaydi.

{% tabs %}
{% tab title="HTML" %}
```html
<h1 style="text-align:center;">Centered Heading</h1>
<p style="text-align:center;">Centered paragraph.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_styles_text-align" %}
{% endtab %}
{% endtabs %}

### <mark style="color:green;">Xulosa</mark>

* HTML elementlariga stil berish uchun <mark style="color:red;">`style`</mark> atributidan foydalaniladi.
* Orqa fon rangini berish uchun <mark style="color:red;">`background-color`</mark> dan foydalaniladi.
* Matn rangini berish uchun <mark style="color:red;">`color`</mark> dan foydalaniladi.
* Matn shriftini berish uchun <mark style="color:red;">`font-family`</mark> dan foydalaniladi.
* Matn o'lchamini belgilash uchun <mark style="color:red;">`font-size`</mark> dan foydalaniladi.
* Matnning gorizontal joylashuvini belgilash uchun <mark style="color:red;">`text-align`</mark> dan foydalaniladi.
