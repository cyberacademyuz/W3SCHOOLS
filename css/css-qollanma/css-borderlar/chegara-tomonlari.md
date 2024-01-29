# Chegara tomonlari

### CSS Border - individual tomonlar <a href="#css-border-individual-yonlari" id="css-border-individual-yonlari"></a>

Oldingi misolalrdan har bir tomon uchun har xil chegara berish mumkinligini ko'rdingiz.

CSS-da chegaralarning har birini alohida tanlash uchun xususiyatlar ham mavjud (top, right, bottom va left):

```
p {
  border-top-style: dotted;
  border-right-style: solid;
  border-bottom-style: dotted;
  border-left-style: solid;
}
```

<figure><img src="../../../.gitbook/assets/image (152).png" alt=""><figcaption></figcaption></figure>

Yuqoridagi misol xuddi shunday natija chiqaradi:

```
p {
  border-style: dotted solid;
}
```

Bular mana bunday ishlaydi:

Agar `border-style` xususiyatida 4 ta qiymat bo'lsa:

* **border-style: dotted solid double dashed**;
  * tepa chegara nuqtali bo'ladi
  * o'ng chegara oddiy&#x20;
  * pastki chegara ikkitalik&#x20;
  * chap chegara chiziqchali

Agar `border-style` xususiyatida 3 ta qiymat bo'lsa:

* **border-style: dotted solid double;**
  * tepa chegara nuqtali&#x20;
  * o'ng va chap chegara oddiy&#x20;
  * pastki chegara ikkitalik&#x20;

Agar border-style xususiatida 2 ta qiymat bo'lsa:

*   **border-style: dotted solid;**

    * tepa va pastki chegara nuqtali&#x20;
    * o'ng va chap chegara oddiy&#x20;



Agar border-style xususiyatida 1 ta qiymat bo'lsa:

*   **border-style: dotted;**

    * barcha chegara tomonlari nuqtali



```
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

{% hint style="warning" %}
`border-style` xususiyati misolida ko'rsatgan usullarimiz, `border-width` va `border-color` xususiyatlarida ham ishlaydi.
{% endhint %}
