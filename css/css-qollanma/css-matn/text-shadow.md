# Text shadow

### Matn soyasi <a href="#matn-soyasi" id="matn-soyasi"></a>

`text-shadow` xususiyati matnga soya qo'shadi.

Eng oddiy foydalanish usulida gorizontal soyani (2px) va vertikal soyani (2px) qilib belgilaysiz:

![](<../../../.gitbook/assets/image (450).png>)

```
h1 {
  text-shadow: 2px 2px;
}
```

Keling endi, rang qo'shamiz, masalan qizil:

![](<../../../.gitbook/assets/image (144).png>)

```
h1 {
  text-shadow: 2px 2px red;
}
```

Undi unga ozgina blur effectini qo'shamiz:

![](<../../../.gitbook/assets/image (522).png>)

```
h1 {
  text-shadow: 2px 2px 5px red;
}
```

### Text Shadow ga misollar <a href="#text-shadow-ga-misollar" id="text-shadow-ga-misollar"></a>

{% code title="Oq rangli matnda soya:" %}
```
h1 {
  color: white;
  text-shadow: 2px 2px 4px #000000;
}
```
{% endcode %}

{% code title="Matnga qizil neonli soya berish:" %}
```
h1 {
  text-shadow: 0 0 3px #ff0000;
}
```
{% endcode %}

{% code title="Matnga qizil va ko'k neonli soya berish:" %}
```
h1 {
  text-shadow: 0 0 3px #ff0000, 0 0 5px #0000ff;
}
```
{% endcode %}

```
h1 {
  color: white;
  text-shadow: 1px 1px 2px black, 0 0 25px blue, 0 0 5px darkblue;
}
```

{% hint style="warning" %}
**Maslahat:** Matnning shrifti, o'lchami va stillarni qanday qilib o'zgartirishni bilmoqchi bo'lsangiz bizning CSS Fonts sahifamizga o'ting

**Maslahat:** Matnga ko'proq effekt qo'shishni o'rganmoqchi bo'lsangiz CSS Text Effects sahifamizga o'ting
{% endhint %}

### CSSning Text Shadow xususiyati <a href="#the-css-text-shadow-property" id="the-css-text-shadow-property"></a>

| Xususiyat                                                                 | Ta'rif                       |
| ------------------------------------------------------------------------- | ---------------------------- |
| [text-shadow](https://www.w3schools.com/cssref/css3\_pr\_text-shadow.asp) | Matnga soya effektini beradi |
