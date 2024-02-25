# Matn oralig'i

## <mark style="color:green;">Matn oralig'i</mark> <a href="#matn-oraligi" id="matn-oraligi"></a>

Ushbu bo'limda quyidagi xususiyatlar haqida bilib olasiz:

* <mark style="color:red;">`text-indent`</mark>
* <mark style="color:red;">`letter-spacing`</mark>
* <mark style="color:red;">`line-height`</mark>
* <mark style="color:red;">`word-spacing`</mark>
* <mark style="color:red;">`white-space`</mark>

## <mark style="color:green;">Matn indentatsiyasi</mark> <a href="#text-indentation" id="text-indentation"></a>

<mark style="color:red;">`text-indent`</mark> xususiyati matnning birinchi qatorini xatboshi sifati joy tashlash uchun ishlatiladi:

{% tabs %}
{% tab title="CSS" %}
```css
p {
  text-indent: 50px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-indent" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Letter Spacing</mark>

<mark style="color:red;">`letter-spacing`</mark> xususiyati matndagi belgilar (harflar) orasidagi masofani belgilash uchun ishlatiladi.

Ushbu misolda belgilar orasidagi masofani kattalashtirilish va kichraytirilishni qanday qilish ko'rsatilgan:

{% tabs %}
{% tab title="CSS" %}
```css
h1 {
  letter-spacing: 5px;
}

h2 {
  letter-spacing: -2px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_letter-spacing" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Line height</mark> <a href="#line-height" id="line-height"></a>

<mark style="color:red;">`line-height`</mark> xususiyati qatorlar orasidagi masofani belgilaydi:

{% tabs %}
{% tab title="CSS" %}
```css
p.small {
  line-height: 0.8;
}

p.big {
  line-height: 1.8;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_line-height" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Word spacing</mark> <a href="#soz-oraligi" id="soz-oraligi"></a>

<mark style="color:red;">`word-spacing`</mark> xususiyati matndagi so'zlar oralg'ini belgilash uchun ishlatiladi.

Quyidagi misolda so'zlar orasidagi masofa kattalashtirilish va kichraytirilishni qanday qilish ko'rsatilgan:

{% tabs %}
{% tab title="CSS" %}
```css
p.one {
  word-spacing: 10px;
}

p.two {
  word-spacing: -2px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text_word-spacing" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">White space</mark> <a href="#white-space" id="white-space"></a>

<mark style="color:red;">`white-space`</mark> xususiyati element matnidagi bo'sh joy va qator tashlashlarni boshqarishga yordam beradi.

Ushbu misolda element ichidagi matnni keyingi qatorga tushishini cheklash ko'rsatiladi:

{% tabs %}
{% tab title="CSS" %}
```css
p {
  white-space: nowrap;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text_white-space" %}
{% endtab %}
{% endtabs %}

### <mark style="color:green;">CSSning barcha matn orasini ochishga aloqador xususiyatlari</mark> <a href="#css-barcha-matn-oraligi-xususiyatlari" id="css-barcha-matn-oraligi-xususiyatlari"></a>

| Xususiyat                                                                       | Ta'rif                                                          |
| ------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| [letter-spacing](https://www.w3schools.com/cssref/pr\_text\_letter-spacing.asp) | Matndagi belgilar orasidagi masofani belgilaydi                 |
| [line-height](https://www.w3schools.com/cssref/pr\_dim\_line-height.asp)        | Qatorlar orasidagi masofani belgilaydi                          |
| [text-indent](https://www.w3schools.com/cssref/pr\_text\_text-indent.asp)       | Matn blokidagi birinchi qatorning chekinishini belgilaydi       |
| [white-space](https://www.w3schools.com/cssref/pr\_text\_white-space.asp)       | Element ichidagi bo'sh joy qanday ishlov berilishini belgilaydi |
| [word-spacing](https://www.w3schools.com/cssref/pr\_text\_word-spacing.asp)     | Matndagi so'zlar orasidagi masofani belgilaydi                  |
