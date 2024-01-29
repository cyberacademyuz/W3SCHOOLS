# CSS Matematik funksiyalari

CSS matematik funksiyalari matematik amallarni xususiyat qiymatlari sifatida ishlatishga imkon beradi. Quyida  `calc()`, `max()` va `min()` funksiyalarini tushuntiramiz.

### calc() funksiyasi <a href="#calc-funksiyasi" id="calc-funksiyasi"></a>

`calc()` funksiyasi xususiyat qiymatida hisoblash imkoniyatini beradi:

#### CSS Sintaksisi <a href="#css-sintaksisi" id="css-sintaksisi"></a>

```
calc(expression)
```

| Qiymat  | Ta'rif                                                                                                                           |
| ------- | -------------------------------------------------------------------------------------------------------------------------------- |
| _ifoda_ | <p>Majburiy. Matematik ifoda. Natija xususiyat qiymati sifatida ishlatiladi.<br>Quyidagi amallar bajarilishi mumkin: + - * /</p> |

{% code title="<div> elementining kengligini hisoblash uchun calc() dan foydalaning:" %}
```
#div1 {
  position: absolute;
  left: 50px;
  width: calc(100% - 100px);
  border: 1px solid black;
  background-color: yellow;
  padding: 5px;
}
```
{% endcode %}

### max() funksiyasi <a href="#max-funksiyasi" id="max-funksiyasi"></a>

`max()` funksiyasi xususiyatning qiymati sifatida vergul bilan ajratilgan qiymatlar ro'yxatidagi eng katta qiymatdan foydalanadi.

#### CSS sintaksisi <a href="#css-sintaksisi-2" id="css-sintaksisi-2"></a>

```
max(value1, value2, ...)
```

| Qiymat                  | Ta'rif                                                                                   |
| ----------------------- | ---------------------------------------------------------------------------------------- |
| _value1_, _value2_, ... | Majburiy. Vergul bilan ajratilgan qiymatlar ro'yxatidagi eng katta qiymatdan foydalanadi |

Misolimizga qarasak:

{% code title="#div1 ning kengligini  50% va 300px dan qaysi biri eng kattasi bo'lsa o'shani belgilash uchun max() dan foydalanish:" %}
```
#div1 {
  background-color: yellow;
  height: 100px;
  width: max(50%, 300px);
}
```
{% endcode %}

### min() funksiyasi <a href="#min-funksiyasi" id="min-funksiyasi"></a>

min() funksiyasi xususiyatning qiymati sifatida vergul bilan ajratilgan qiymatlar ro'yxatidagi eng kichik qiymatdan foydalanadi.

#### CSS sintaksisi <a href="#css-sintaksisi-3" id="css-sintaksisi-3"></a>

```
min(value1, value2, ...)
```

| Qiymat                  | Description                                                                               |
| ----------------------- | ----------------------------------------------------------------------------------------- |
| _value1_, _value2_, ... | Majburiy. Vergul bilan ajratilgan qiymatlar ro'yxatidagi eng kichik qiymatdan foydalanadi |

Misolimizga qarasak:

{% code title="#div1 ning kengligini  50% va 300px dan qaysi biri eng kichigi bo'lsa o'shani belgilash uchun max() dan foydalanish:" %}
```
#div1 {
  background-color: yellow;
  height: 100px;
  width: min(50%, 300px);
}
```
{% endcode %}

### CSSning barcha matematik funksiyalari <a href="#barcha-css-matematik-funksiyalari" id="barcha-css-matematik-funksiyalari"></a>

| Funksiya                                                  | Ta'rif                                                                          |
| --------------------------------------------------------- | ------------------------------------------------------------------------------- |
| [calc()](https://www.w3schools.com/cssref/func\_calc.asp) | Hisoblashlarni CSS qiymatlari sifatida ishlatishga ruxsat beradi                |
| [max()](https://www.w3schools.com/cssref/func\_max.asp)   | Vergul bilan ajratilgan qiymatlar ro'yxatidagi eng katta qiymatdan foydalanadi  |
| [min()](https://www.w3schools.com/cssref/func\_min.asp)   | Vergul bilan ajratilgan qiymatlar ro'yxatidagi eng kichik qiymatdan foydalanadi |
