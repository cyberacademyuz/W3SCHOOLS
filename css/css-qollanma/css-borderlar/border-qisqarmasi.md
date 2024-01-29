# Border qisqarmasi

### CSS Border qisqartmasi <a href="#css-border-qisqartmasi" id="css-border-qisqartmasi"></a>

Avvalgi sahifada ko'rganingizdek, chegaralar bilan ishlashda ko'plab xususiyatlarni hisobga olish kerak.

CSSning `border` qisqartmasi sizga barcha chegaralarning induvidual qiymatlarini bir qatorda yozishga imkon beradi.

`border` qisqartmasi chegaraning quyidagi xususiyatlari uchun qisqartma xususiyat hisoblanadi:

* border-width
* border-style (talab qilinadigan)
* border-color

```
p {
  border: 5px solid red;
}
```

<figure><img src="../../../.gitbook/assets/image (174).png" alt=""><figcaption></figcaption></figure>

Bundan tashqari, faqat bir tomon uchun barcha individual chegara xususiyatlarini berishingiz mumkin:

{% code title="Chap chegara:" %}
```
p {
  border-left: 6px solid red;
}
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (159).png" alt=""><figcaption></figcaption></figure>

#### Pastki chegara <a href="#pastki-border" id="pastki-border"></a>

```
p {
  border-bottom: 6px solid red;
}
```

<figure><img src="../../../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>
