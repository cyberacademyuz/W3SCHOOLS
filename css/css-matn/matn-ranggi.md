# Matn ranggi

CSS da matnni formatlash uchun juda ko'p xususiyatlar mavjud.

<figure><img src="../../../.gitbook/assets/image (444).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:green;">Matn rangi</mark> <a href="#matn-rangi" id="matn-rangi"></a>

<mark style="color:red;">`color`</mark> xususiyati matn rangini berish uchun ishlatiladi. Rang quyidagi qiymatlar asosida beriladi:

* rang nomi bilan - "red" kabi
* HEX qiymat bilan - "#ff0000" kabi
* RGB qiymat bilan - "rgb(255,0,0)" kabi

Berish mumkin bo'lgan barcha ranglarni ko'rish uchun CSS Ranglari sahifasiga o'ting.

Sahifadagi matnlarning default rangi body selektori ichida beriladi:

{% tabs %}
{% tab title="CSS" %}
```css
body {
  color: blue;
}

h1 {
  color: green;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_color" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Matn rangi va orqafon rangi</mark> <a href="#matn-rangi-va-fon-rangi" id="matn-rangi-va-fon-rangi"></a>

Ushbu misolda matn rangini ham, orqafon rangini ham beramiz:

{% tabs %}
{% tab title="CSS" %}
```css
body {
  background-color: lightgrey;
  color: blue;
}

h1 {
  background-color: black;
  color: white;
}

div {
  background-color: blue;
  color: white;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_color_bg" %}
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
**Muhim:** Ko'rish bilan bog'liq muammosi bo'lgan odamlar uchun kontrastning balanligi muhim hisoblanadi. Shuning uchun, har doim matn rangi va orqafon rangi (yoki orqafon rasmi) o'rtasidagi kontrast yaxshi ekanligiga e'tibor qiling!
{% endhint %}

## <mark style="color:green;">CSS Matn rangi xususiyati</mark> <a href="#css-matn-rangi-xususiyati" id="css-matn-rangi-xususiyati"></a>

| Xususiyat                                                     | Ta'rif                  |
| ------------------------------------------------------------- | ----------------------- |
| [color](https://www.w3schools.com/cssref/pr\_text\_color.asp) | Matn rangini belgilaydi |
