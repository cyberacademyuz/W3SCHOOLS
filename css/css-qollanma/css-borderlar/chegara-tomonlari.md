# Chegara tomonlari

## <mark style="color:green;">CSS Border - individual tomonlar</mark> <a href="#css-border-individual-yonlari" id="css-border-individual-yonlari"></a>

Oldingi misolalrdan har bir tomon uchun har xil chegara berish mumkinligini ko'rdingiz.

CSS-da chegaralarning har birini alohida tanlash uchun xususiyatlar ham mavjud (top, right, bottom va left):

{% tabs %}
{% tab title="CSS" %}
```css
p {
  border-top-style: dotted;
  border-right-style: solid;
  border-bottom-style: dotted;
  border-left-style: solid;
}
```

Result:

<figure><img src="../../../.gitbook/assets/image (152).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_border-side" %}
{% endtab %}
{% endtabs %}

Yuqoridagi misol xuddi shunday natija chiqaradi:

{% tabs %}
{% tab title="CSS" %}
```css
p {
  border-style: dotted solid;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_border-side2" %}
{% endtab %}
{% endtabs %}

Bular mana bunday ishlaydi:

Agar <mark style="color:red;">`border-style`</mark> xususiyatida 4 ta qiymat bo'lsa:

* **border-style: dotted solid double dashed**;
  * tepa chegara nuqtali bo'ladi
  * o'ng chegara oddiy&#x20;
  * pastki chegara ikkitalik&#x20;
  * chap chegara chiziqchali

Agar <mark style="color:red;">`border-style`</mark> xususiyatida 3 ta qiymat bo'lsa:

* **border-style: dotted solid double;**
  * tepa chegara nuqtali&#x20;
  * o'ng va chap chegara oddiy&#x20;
  * pastki chegara ikkitalik&#x20;

Agar <mark style="color:red;">`border-style`</mark> xususiatida 2ta qiymat bo'lsa:

* **border-style: dotted solid;**
  * tepa va pastki chegara nuqtali&#x20;
  * o'ng va chap chegara oddiy&#x20;

Agar <mark style="color:red;">`border-style`</mark> xususiyatida 1 ta qiymat bo'lsa:

* **border-style: dotted;**
  * barcha chegara tomonlari nuqtali

{% tabs %}
{% tab title="CSS" %}
```css
/* To'rtta qiymatli */
p {
  border-style: dotted solid double dashed;
}

/* Uchta qiymatli */
p {
  border-style: dotted solid double;
}

/* Ikkita qiymatli */
p {
  border-style: dotted solid;
}

/* Bitta qiymatli */
p {
  border-style: dotted;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_border-side3" %}
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
`border-style` xususiyati misolida ko'rsatgan usullarimiz, `border-width` va `border-color` xususiyatlarida ham ishlaydi.
{% endhint %}
