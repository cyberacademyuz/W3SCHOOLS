# Text shadow

## <mark style="color:green;">Matn soyasi</mark> <a href="#matn-soyasi" id="matn-soyasi"></a>

<mark style="color:red;">`text-shadow`</mark> xususiyati matnga soya qo'shadi.

Eng oddiy foydalanish usulida gorizontal soyani (2px) va vertikal soyani (2px) qilib belgilaysiz:

![](<../../../.gitbook/assets/image (450).png>)

{% tabs %}
{% tab title="CSS" %}
```css
h1 {
  text-shadow: 2px 2px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-shadow1" %}
{% endtab %}
{% endtabs %}

Keling endi, rang qo'shamiz, masalan qizil:

![](<../../../.gitbook/assets/image (144).png>)

{% tabs %}
{% tab title="CSS" %}
```css
h1 {
  text-shadow: 2px 2px red;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-shadow2" %}
{% endtab %}
{% endtabs %}

Undi unga ozgina blur effectini qo'shamiz:

![](<../../../.gitbook/assets/image (522).png>)

{% tabs %}
{% tab title="CSS" %}
```css
h1 {
  text-shadow: 2px 2px 5px red;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-shadow2" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Text Shadowga misollar</mark> <a href="#text-shadow-ga-misollar" id="text-shadow-ga-misollar"></a>

{% tabs %}
{% tab title="Ruby" %}
Oq rang matn soyasi:

```css
h1 {
  color: white;
  text-shadow: 2px 2px 4px #000000;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-shadow4" %}
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="CSS" %}
Matnga qizil neonli soya berish:

```css
h1 {
  text-shadow: 0 0 3px #ff0000;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-shadow5" %}
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="CSS" %}
Matnga qizil va ko'k neonli soya berish:

```css
h1 {
  text-shadow: 0 0 3px #ff0000, 0 0 5px #0000ff;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-shadow6" %}
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="CSS" %}
```css
h1 {
  color: white;
  text-shadow: 1px 1px 2px black, 0 0 25px blue, 0 0 5px darkblue;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_text-shadow7" %}
{% endtab %}
{% endtabs %}



{% hint style="warning" %}
**Maslahat:** Matnning shrifti, o'lchami va stillarni qanday qilib o'zgartirishni bilmoqchi bo'lsangiz bizning CSS Fonts sahifamizga o'ting

**Maslahat:** Matnga ko'proq effekt qo'shishni o'rganmoqchi bo'lsangiz CSS Text Effects sahifamizga o'ting
{% endhint %}

## <mark style="color:green;">CSSning Text Shadow xususiyati</mark> <a href="#the-css-text-shadow-property" id="the-css-text-shadow-property"></a>

| Xususiyat                                                                 | Ta'rif                       |
| ------------------------------------------------------------------------- | ---------------------------- |
| [text-shadow](https://www.w3schools.com/cssref/css3\_pr\_text-shadow.asp) | Matnga soya effektini beradi |
