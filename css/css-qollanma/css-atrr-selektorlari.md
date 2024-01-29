# CSS Atrr selektorlari

## HTML elementlarga maxsus attributlar orqali stil berish <a href="#html-elementlarga-maxsus-attributlar-bilan-stil-berish" id="html-elementlarga-maxsus-attributlar-bilan-stil-berish"></a>

HTML elementlariga ularning maxsus attributlari yoki atribut qiymatiga qarab stil berish mumkin.

### CSS \[attribute] selektori <a href="#css-attribute-selektor" id="css-attribute-selektor"></a>

`[attribute]` selektori belgilangan atributga ega elementlarni tanlash uchun ishlatiladi.

Quyidagi misolda `target="_blank"` atributiga ega barcha `<a>` elementlarini tanlanadi:

```
a[target] {
  background-color: yellow;
}
```

### CSS \[attribute="value"] selektori <a href="#css-attributevalue-selektor" id="css-attributevalue-selektor"></a>

`[attribute="value"]` selektori belgilangan atribut va qiymatga ega elementlarni tanlash uchun ishlatiladi.

Quyidagi misolda target attributida "\_blank" qiymati  mavjud barcha  `<a>` elementini tanlanadi.

```
a[target="_blank"] {
  background-color: yellow;
}
```

### CSS \[attribute\~="value"] selektori <a href="#css-attribute-value-selector" id="css-attribute-value-selector"></a>

`[attribute~="value"]` selektori berilgan so'zni o'z ichiga olgan atribut qiymatiga ega elementlarni tanlash uchun ishlatiladi.

Quyidagi misolda bo'sh joy bilan ajratilgan so'zlar ro'yxatini o'z ichiga olgan `title` atributiga ega barcha elementlar tanlanadi, ulardan biri "flower"

```
[title~="flower"] {
  border: 5px solid yellow;
}
```

Yuqoridagi misolga `title="flower"`, `title="summer flower"` va `title="flower new"` larga ega elementlar mos keladi, lekin `title="my-flower"` yoki `title="flowers"` mos kelymaydi.

### CSS \[attribute|="value"] selektori <a href="#css-attributevalue-selector" id="css-attributevalue-selector"></a>

`[atribut|="value"]` selektori ko'rsatilgan atributga ega elementlarni tanlash uchun ishlatiladi, ularning qiymati to'liq yozilgan qiymat yoki berilgan qiymatdan keyin chiziqcha (-) bo'lishi ham mumkin.

**Eslatma**: Qiymat **class="top"** kabi to'liq yozilishi yoki unga **class="top-text"** kabi chiziq ( - ) qo'yilishi kerak.

```
[class|="top"] {
  background: yellow;
}
```

### CSS \[attribute^="value"] selektori <a href="#css-attributevalue-selector-2" id="css-attributevalue-selector-2"></a>

`[attribute^="value"]` selektori ko'rsatilgan atributga ega bo'lgan, qiymati belgilangan qiymatdan boshlanadigan elementlarni tanlash uchun ishlatiladi.

Quyidagi misolda class atributi "top" bilan boshlanadigan barcha elementlar tanlanadi:

**Note:** Qiymat to'liq so'z bo'lishi shart emas

```
[class^="top"] {
  background: yellow;
}
```

### CSS \[attribute$="value"] selektori

`[attribute$="value"]` selektori atribut qiymati belgilangan qiymat bilan tugaydigan elementlarni tanlash uchun ishlatiladi.

Quyidagi misoda class atributining qiymati "test" bilan tugaydigan barcha elementlar tanlanadi:

**Eslatma**: Qiymat butun so'z bo'lishi shart emas!

```
[class$="test"] {
  background: yellow;
}
```

### CSS \[attribute\*="value"] selektori <a href="#css-attributevalue-selector-3" id="css-attributevalue-selector-3"></a>

`[atribut*="value"]` selektori atribut qiymati ma'lum qiymatga ega bo'lgan elementlarni tanlash uchun ishlatiladi.

Quyidagi misolda class attributining qiymada "te" so'zi mavjud bo'lgan barcha elementlar tanlanadi:

**Eslatma**: Qiymat butun so'z bo'lishi shart emas!

```
 [class*="te"] {
  background: yellow;
}
```

### Formalarga stil berish <a href="#formalarga-stil-berish" id="formalarga-stil-berish"></a>

Formalarga class yoki id dan foydalanmay still berishda attributlar yordam berishi mumkin.

```
input[type="text"] {
  width: 150px;
  display: block;
  margin-bottom: 10px;
  background-color: yellow;
}

input[type="button"] {
  width: 120px;
  margin-left: 35px;
  display: block;
}
```

Maslahat: CSS yordamida formalarga still berish bo'yicha ko'proq misollarni ko'rish uchun bizning [<mark style="color:green;">CSS Formalar qo'llanmasi</mark>](css-formalar.md) sahifamizga tashrif buyuring.

### CSSning barcha Attribut selektorlari <a href="#barcha-css-attribut-selektorlar" id="barcha-css-attribut-selektorlar"></a>

| Selektor                                                                                          | Misol                  | Misol ta'rifi                                                                       |
| ------------------------------------------------------------------------------------------------- | ---------------------- | ----------------------------------------------------------------------------------- |
| [\[_attribute_\]](https://www.w3schools.com/cssref/sel\_attribute.asp)                            | \[target]              | Attributga qarab olib keladi                                                        |
| [\[_attribute_=_value_\]](https://www.w3schools.com/cssref/sel\_attribute\_value.asp)             | \[target="\_blank"]    | Barcha target="\_blank" qiymatiga ega elementlarni olib keladi                      |
| [\[_attribute_\~=_value_\]](https://www.w3schools.com/cssref/sel\_attribute\_value\_contains.asp) | \[title\~="flower"]    | Barcha "flower" so'zi bor bo'lgan elementlarni olib keladi                          |
| [\[_attribute_\|=_value_\]](https://www.w3schools.com/cssref/sel\_attribute\_value\_lang.asp)     | \[lang\|="en"]         | Barcha "en" qiymati bilan boshlanuvchi lang atributiga ega elementlarni olib keladi |
| [\[_attribute_^=_value_\]](https://www.w3schools.com/cssref/sel\_attr\_begin.asp)                 | a\[href^="https"]      | Har bir https bilan boshlanuvchi \<a> elementni olib keladi                         |
| [\[_attribute_$=_value_\]](https://www.w3schools.com/cssref/sel\_attr\_end.asp)                   | a\[href$=".pdf"]       | Har bir href attributi .pdf bilan tugovchi \<a> elementni olib keladi               |
| [\[_attribute_\*=_value_\]](https://www.w3schools.com/cssref/sel\_attr\_contain.asp)              | a\[href\*="w3schools"] | Har bir w3schools qiymatiga ega \<a> elementni olib keladi                          |
