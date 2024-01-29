# CSS Rang kalit so'zlari

Ushbu sahifada `transparent`, `currentcolor` va `inherit` kalit so'zlari tushuntiriladi.

### Transparent kalit so'zi <a href="#transparent-kalitsozi" id="transparent-kalitsozi"></a>

`transparent` kalit so'zi rangni shaffof qilish uchun ishlatiladi. Bu ko'pincha element uchun shaffof background rang yaratishda ishlatiladi.

{% code title="Bu yerda <div> elementining orqafon rangi to'liq shaffof bo'ladi va orqafon rasmi quyidagilar orqali namoyon bo'ladi:" %}
```
body {
  background-image: url("paper.gif");
}

div {
  background-color: transparent;
}
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** `transparent` kalit so'zi rgba(0,0,0,0) ga teng. RGBA rang qiymatlari alfa kanali orqali RGB rang qiymatlarining kengaytmasi bo'lib, u rang uchun shaffoflikni belgilaydi. Bu haqida [CSS RGB ranglar](css-ranglar.md#rgba-ranglar) va [CSS Ranglar](../css-qollanma/css-ranglar/) bo'limimizda batafsil o'qing.
{% endhint %}

### currentcolor kalit so'zi <a href="#currentcolor-kalitsozi" id="currentcolor-kalitsozi"></a>

`currentcolor` kalit so'zi elementning `color` xususiyatining joriy qiymatini saqlaydigan o'zgaruvchiga o'xshaydi.

Agar ma'lum bir rangni elementga yoki sahifaga mos bo'lishini istasangiz, ushbu kalit so'z foydali bo'lishi mumkin.

{% code title="Ushbu misolda <div> elementining border rangi ko'k bo'ladi, chunki <div> elementining matn rangi ko'k:" %}
```
div {
  color: blue;
  border: 10px solid currentcolor;
}
```
{% endcode %}

{% code title="Ushbu misolda body elementining rangi <div>ning orqafon rangiga currentcolor qiymati asosida o'rnatiladi:" %}
```
body {
  color: purple;
}

div {
  background-color: currentcolor;
}
```
{% endcode %}

{% code title="Ushbu misolda body elementining rang qiymati <div>ning border rangi va soya rangiga currentcolor qiymati asosida o'rnatiladi:" %}
```
body {
 color: green;
}

div {
  box-shadow: 0px 0px 15px currentcolor;
  border: 5px solid currentcolor;
}
```
{% endcode %}

### Inherit kalit so'zi <a href="#inherit-kalitsozi" id="inherit-kalitsozi"></a>

`inherit` kalit so'zi xususiyat o'z qiymatini asosiy elementidan meros qilib olishi kerakligini bildiradi.

`inherit` kalit so'zi istalgan CSS xususiyati uchun va istalgan HTML elementida ishlatilishi mumkin.

```
div {
  border: 2px solid red;
}

span {
  border: inherit;
}
```
