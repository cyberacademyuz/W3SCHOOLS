# Konussimon gradient

### CSS Konussimon gradientlar <a href="#css-konusli-gradientlar" id="css-konusli-gradientlar"></a>

Konussimon gradient - bu markaziy nuqta atrofida ranglar orqali aylanma shakldagi gradient.

Konussimon gradient yaratish uchun kamida ikkita rang belgilashingiz kerak.

#### Sintaksis <a href="#sintaksis" id="sintaksis"></a>

```
background-image: conic-gradient([burchakdan] [at position,] color [daraja], color [daraja], ...);
```

standart holatda uning burchagi **0deg** va joylashuvi o'rtada bo'ladi.

Agar daraja ko'rsatilmagan bo'lsa, ranglar markaziy nuqta atrofida teng ravishda tarqaladi.

### Konussimon gradient: 3 xil rangda <a href="#konusli-gradient-3-xil-rangda" id="konusli-gradient-3-xil-rangda"></a>

Quyidagi misolda 3 xil rangli konussimon gradient ko'rsatilgan:

![](<../../../.gitbook/assets/image (843).png>)

```
#grad {
  background-image: conic-gradient(red, yellow, green);
}
```

### Konussimon gradient: 5 xil rangda <a href="#konusli-gradient-5-ta-rangda" id="konusli-gradient-5-ta-rangda"></a>

Quyidagi misolda 5 xil rangli konussimon gradient ko'rsatilgan:

![](<../../../.gitbook/assets/image (841).png>)

```
#grad {
  background-image: conic-gradient(red, yellow, green, blue, black);
}
```

### Konussimon gradient: 3 xil rangli va darajali <a href="#konusli-gradient-3-xil-rang-va-darajalar" id="konusli-gradient-3-xil-rang-va-darajalar"></a>

Quyidagi misolda 3 xil rangli va har bir rang uchun o'z darajasi berilgan konussimon gradient ko'rsatilgan:

![](<../../../.gitbook/assets/image (811).png>)

```
#grad {
  background-image: conic-gradient(red 45deg, yellow 90deg, green 210deg);
}
```

### Pirog diagrammalarini yaratish <a href="#pirog-diagrammalarini-yaratish" id="pirog-diagrammalarini-yaratish"></a>

Konusning gradientini pirogga o'xshatish uchun `border-radiusini: 50%` dan foydalaning:

![](<../../../.gitbook/assets/image (281).png>)

```
#grad {
  background-image: conic-gradient(red, yellow, green, blue, black);
  border-radius: 50%;
}
```

Mana yana bir, barcha ranglari o'zining darajasiga ega bo'lgan doiraviy diagramma:

![](<../../../.gitbook/assets/image (768).png>)

```
#grad {
  background-image: conic-gradient(red 0deg, red 90deg, yellow 90deg, yellow 180deg, green 180deg, green 270deg, blue 270deg);
  border-radius: 50%;
}
```

## Burchakdan boshlangan konussimon gradienti

\[burchakdan] butun konussimon gradient aylantiriladigan burchakni belgilaydi.

Quyidagi misolda 90 graduslik burchakka ega bo'lgan konussimon gradient ko'rsatilgan:

![](<../../../.gitbook/assets/image (763).png>)

```
#grad {
  background-image: conic-gradient(from 90deg, red, yellow, green);
}
```

### Belgilangan markaziy joylashuvga ega konussimon gradient <a href="#belgilangan-markaz-holatiga-ega-konusli-gradient" id="belgilangan-markaz-holatiga-ega-konusli-gradient"></a>

\[joylashuv] konussimon gradientning markazini belgilaydi.

Quyidagi misolda markaziy joylashuvi 60% 45% bo'lgan konussimon gradient ko'rsatilgan:

![](<../../../.gitbook/assets/image (793).png>)

```
#grad {
  background-image: conic-gradient(at 60% 45%, red, yellow, green);
}
```

### Takrorlanuvchi konussimon gradientlar <a href="#takrorlanuvchi-konusli-gradientlar" id="takrorlanuvchi-konusli-gradientlar"></a>

Konusning gradientini takrorlash uchun `repeating-conic-gradient()` funksiyasidan foydalaniladi:

![](<../../../.gitbook/assets/image (256).png>)

```
#grad {
  background-image: repeating-conic-gradient(red 10%, yellow 20%);
  border-radius: 50%;
}
```

Mana, rangning boshlanish nuqtasi va rangning to'xtash nuqtalari bilan takrorlanuvchi konussimon gradient:

![](<../../../.gitbook/assets/image (361).png>)

```
#grad {
  background-image: repeating-conic-gradient(red 0deg 10deg, yellow 10deg 20deg, blue 20deg 30deg);
  border-radius: 50%;
}
```

### CSS Gradient funksiyalari <a href="#css-gradient-funksiyalari" id="css-gradient-funksiyalari"></a>

Quyidagi jadvalda CSSning gradient funksiyalari keltirilgan:

| Funksiya                                                                                            | Ta'rif                                                                                          |
| --------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [conic-gradient()](https://www.w3schools.com/cssref/func\_conic-gradient.asp)                       | Konussimon gradient hosil qiladi. Kamida ikkita rangni bo'lishi kerak (markaziy nuqta atrofida) |
| [linear-gradient()](https://www.w3schools.com/cssref/func\_linear-gradient.asp)                     | Chiziqli gradient hosil qiladi. Kamida ikkita rang bo'lishi kerak (yuqoridan pastga)            |
| [radial-gradient()](https://www.w3schools.com/cssref/func\_radial-gradient.asp)                     | Radial gradient hosil qiladi. Kamida ikkita rang bo'lishi kerak (o'rtadan burchaklarga)         |
| [repeating-conic-gradient()](https://www.w3schools.com/cssref/func\_repeating-conic-gradient.asp)   | Konussimon gradientni takrorlaydi                                                               |
| [repeating-linear-gradient()](https://www.w3schools.com/cssref/func\_repeating-linear-gradient.asp) | Chiziqli gradientni takrorlaydi                                                                 |
| [repeating-radial-gradient()](https://www.w3schools.com/cssref/func\_repeating-radial-gradient.asp) | Radial gradientni takrorlaydi                                                                   |
