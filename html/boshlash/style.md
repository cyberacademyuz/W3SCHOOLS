# Style

HTMLdagi style attributidan elementlarga rang, shrift, o'lcham kabi stillar berish uchun foydalaniladi.

## HTMLning Style attributi

HTML elementlariga stil berish style attributi yordamida amalga oshiriladi.

Style attributining sintaksisi quyidagi ko'rinishda bo'ladi.

```html
<tagname style="property:value;">
```

**Property** CSSdagi xususiyat. **Value** esa css dagi qiymat.

{% hint style="warning" %}
Siz bu qo'llanmada CSS haqida ko'p narsa o'rganasiz.
{% endhint %}

## Background color

CSSdagi `background-color` xususiyati HTML elementining orqa fon rangini belgilaydi.

#### Sahifa uchun orqa fon ranggini **powderblue** deb belgilash:

```html
<body style="background-color:powderblue;">

<h1>Bu sarlavha</h1>
<p>Bu paragraf</p>

</body>
```

#### Ikkita turli element uchun orqa fon rang berish

```html
<body>

<h1 style="background-color:powderblue;">Bu sarlavha</h1>
<p style="background-color:tomato;">Bu paragrad</p>

</body>
```

## Matn rangi

CSS da `color` xususiyati HTML elementning matn rangini belgilaydi.

```
<h1 style="color:blue;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>
```

## Shriftlar

CSSning  `font-family` xususiyati HTML elementida foydalaniladigan shriftni belgilaydi.

```
<h1 style="font-family:verdana;">This is a heading</h1>
<p style="font-family:courier;">This is a paragraph.</p>
```

## Matn o'lchami

CSSning  `font-size` xususiyati HTML elementidagi matnning o'lchamini belgilaydi.

```
<h1 style="font-size:300%;">This is a heading</h1>
<p style="font-size:160%;">This is a paragraph.</p>
```

## Matn joylashuvi

CSSning  `text-align` xususiyati HTML elementidagi matnning gorizontal o'rnini belgilaydi.

```
<h1 style="text-align:center;">Centered Heading</h1>
<p style="text-align:center;">Centered paragraph.</p>
```

### Xulosa

* HTML elementlariga stil berish uchun `style` attributidan foydalaniladi.
* Orqa fon rangni berish uchun background-color dan foydalaniladi.
* Matn rangini berish uchun `color` dan foydalaniladi.
* Matn shriftini berish uchun `font-family` dan foydalaniladi.
* Matn o'lchamini belgilash uchun `font-size` dan foydalaniladi.
* Matnning gorizontal joylashuvini belgilash uchun `text-align` dan foydalaniladi.

