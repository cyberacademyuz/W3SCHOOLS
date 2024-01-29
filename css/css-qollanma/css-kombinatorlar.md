# CSS Kombinatorlar

### CSS Kombinatorlar <a href="#css-kombinatorlar" id="css-kombinatorlar"></a>

{% hint style="warning" %}
Kombinator - selektorlar o'rtasidagi munosabatni tushuntiruvchi narsa.
{% endhint %}

CSS selektori bitta oddiy selektordan tashqari, ko'proq selektorga ham ega bo'lishi mumkin. Selektorlar orasiga kombinatorlar kiritishimiz bo'ladi.

CSS da to'rt xil kombinatorlar mavjud:

* Keyingi (avlod) elementni belgilovchi selektor (space)
* Element ichidagi bola elementni belgilovchi selektor (>)
* Yonidagi qo'shni elementni belgilovchi selektor (+)
* Umumiy yonma yon elementlarni belgilovchi selektor (\~)

### Keyingi elementni belgilovchi selektor <a href="#keyingi-elementni-belgilovchi-selektor" id="keyingi-elementni-belgilovchi-selektor"></a>

Descendant (avlod) selektori bellgilangan elementdan keyin kelgan barcha elementlarni belgilaydi

Quyidagi misolda `<div>` elementlari ichidagi barcha `<p>` elementlari tanlanadi:

```
div p {
  background-color: yellow;
}
```

### Child selektori (>) <a href="#child-selektor" id="child-selektor"></a>

Child selektor tanlangan elementning barcha bola elementlarini tanlaydi.

Quyidagi misolda `<div>` elementiga tegishli bo'lgan barcha `<p>` elementlar tanlanadi:

```
 div > p {
  background-color: yellow;
}
```

### Qo'shni sibling element selektori (+) <a href="#yonma-yon-qoshni-elementni-belgilovchi-selektor" id="yonma-yon-qoshni-elementni-belgilovchi-selektor"></a>

Yonidagi qo'shni elementni belgilovchi selektor tanlangan elementdan keyin kelgan elementni tanlaydi.

Yonma-yon yozilgan elementlar bitta ota elementga ega bo'lishi kerak.

Quyidagi misolda `<div>` elementidan keyin kelgan barcha `<p>` elementlar tanlanadi:

```
div + p {
  background-color: yellow;
}
```

### Umumiy sibling selektori (\~) <a href="#umumiy-yonma-yon-elementlarni-belgilovchi-selektor" id="umumiy-yonma-yon-elementlarni-belgilovchi-selektor"></a>

Umumiy  sibling selektori belgilangan elementdan keyin kelgan barcha sibling elementlarni tanlaydi.

Quyidagi misolda `<div>` elementlari bilan qo'shni bo'lgan barcha `<p>` elementlari tanlangan:

```
 div ~ p {
  background-color: yellow;
}
```

### CSSning barcha kombinator selektorlari <a href="#barcha-css-kombinator-selektorlari" id="barcha-css-kombinator-selektorlari"></a>

| Selektor                                                                        | Misol   | Misol tavsifi                                                        |
| ------------------------------------------------------------------------------- | ------- | -------------------------------------------------------------------- |
| [_element element_](https://www.w3schools.com/cssref/sel\_element\_element.asp) | div p   | \<div> element ichidagi barcha p elementlarni belgilaydi             |
| [_element>element_](https://www.w3schools.com/cssref/sel\_element\_gt.asp)      | div > p | \<div> elementi parent bo'lgan barcha \<p> elementlarini belgilaydi, |
| [_element+element_](https://www.w3schools.com/cssref/sel\_element\_pluss.asp)   | div + p | \<div> elementidan keyin joylashgan barcha elementlarni belgilaydi   |
| [_element1\~element2_](https://www.w3schools.com/cssref/sel\_gen\_sibling.asp)  | p \~ ul | Oldinda \<p> elementi joylashgan har bir \<ul> elementni tanlaydi    |
