# Border qisqarmasi

### CSS Border qisqartmasi <a href="#css-border-qisqartmasi" id="css-border-qisqartmasi"></a>

Avvalgi sahifada ko'rganingizdek, chegaralar bilan ishlashda ko'plab xususiyatlarni hisobga olish kerak.

CSSning <mark style="color:red;">`border`</mark> qisqartmasi sizga barcha chegaralarning induvidual qiymatlarini bir qatorda yozishga imkon beradi.

<mark style="color:red;">`border`</mark> qisqartmasi chegaraning quyidagi xususiyatlari uchun qisqartma xususiyat hisoblanadi:

* <mark style="color:red;">`border-width`</mark>
* <mark style="color:red;">`border-style`</mark> (talab qilinadigan)
* <mark style="color:red;">`border-color`</mark>

{% tabs %}
{% tab title="CSS" %}
```css
p {
  border: 5px solid red;
}
```

Natijasi:

<figure><img src="../../../.gitbook/assets/image (174).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_border" %}
{% endtab %}
{% endtabs %}

Bundan tashqari, faqat bir tomon uchun barcha individual chegara xususiyatlarini berishingiz mumkin:

{% tabs %}
{% tab title="CSS" %}
#### Chap tomon chegarasi:

```css
p {
  border-left: 6px solid red;
}
```

Natijasi:

<figure><img src="../../../.gitbook/assets/image (159).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_border_left" %}
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Ruby" %}
#### Pastki chegara:

```css
p {
  border-bottom: 6px solid red;
}
```

<figure><img src="../../../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_border_bottom" %}
{% endtab %}
{% endtabs %}
