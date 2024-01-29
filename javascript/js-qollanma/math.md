# MATH

{% hint style="success" %}
JavaScript Math obyekti raqamlar ustida matematik amallar bajarishga imkon beradi.
{% endhint %}

```
Math.PI;
```

### Math obekti

Boshqa obektlardan farqli o'laroq, Math obektida konstruktor yo'q.

Math obekti statik bo'ladi.

Barcha metodlar va xususiyatlaridan Math obyektini yaratmasdan avval ham foydalanish mumkin.

### Math xususiyatlari

Har qanday Math xususiyati uchun sintaksis: `Math.xususiyat`

JavaScript Math-ning xususiyati sifatida foydalanish mumkin bo'lgan 8 ta matematik konstantalarni taqdim etadi:

```
Math.E        // returns Euler's number
Math.PI       // returns PI
Math.SQRT2    // returns the square root of 2
Math.SQRT1_2  // returns the square root of 1/2
Math.LN2      // returns the natural logarithm of 2
Math.LN10     // returns the natural logarithm of 10
Math.LOG2E    // returns base 2 logarithm of E
Math.LOG10E   // returns base 10 logarithm of E
```

### Math metodlari

Har qanday Math metodi uchun sintaksis: `Math.metod`

### Raqamdan butun son(integer)ga

Raqamni butun songa yaxlitlashning 4 ta umumiy metodi mavjud:

| Math.round(x) | X ni unga eng yaqin butun songa yaxlitlangan holda qaytaradi            |
| ------------- | ----------------------------------------------------------------------- |
| Math.ceil(x)  | X ni unga eng yaqin kattaroq butun songa yaxlitlangan holda qaytaradi   |
| Math.floor(x) | X ni unga eng yaqin kichikroq butun soniga yaxlitlangan holda qaytaradi |
| Math.trunc(x) | x ning butun qismini qaytaradi (ES6 da yangi)                           |

### Math.round()

`Math.round(x)` eng yaqin butun sonni qaytaradi:

```
Math.round(4.6);
Math.round(4.5);
Math.round(4.4);
```

### Math.ceil()

`Math.ceil(x)` eng yaqin butun songa yaxlitlangan x qiymatini qaytaradi :

```
Math.ceil(4.9);
Math.ceil(4.7);
Math.ceil(4.4);
Math.ceil(4.2);
Math.ceil(-4.2);
```

### Math.floor()

`Math.floor(x)` x ning eng yaqin kichikroq butun songa yaxlitlangan qiymatini qaytaradi:

```
Math.floor(4.9);
Math.floor(4.7);
Math.floor(4.4);
Math.floor(4.2);
Math.floor(-4.2);
```

### Math.trunc()

`Math.trunc(x)` x ni o'zini integer sifatida qaytaradi:

```
Math.trunc(4.9);
Math.trunc(4.7);
Math.trunc(4.4);
Math.trunc(4.2);
Math.trunc(-4.2);
```

### Math.sign()

Agar x manfiy, null yoki musbat bo'lsa `Math.sign(x)` qaytariladi:

```
Math.sign(-4);
Math.sign(0);
Math.sign(4);
```

{% hint style="warning" %}
Math.trunc() va Math.sign() [JavaScript 2015-ES6](https://www.w3schools.com/js/js\_es6.asp) ga qo'shildi.
{% endhint %}

### Math.pow()

`Math.pow(x, y)` x qiymatining y darajasini qaytaradi:

```
Math.pow(8, 2);
```

### Math.sqrt()

`Math.sqrt(x)` x ning kvadrat ildizini qaytaradi:

```
Math.sqrt(64);
```

### Math.abs()

`Math.abs(x)` x ning absalyut qiymatini qaytaradi:

```
Math.abs(-4.7);
```

### Math.sin()

`Math.sin(x)` x burchakning sinusini (-1 va 1 orasidagi qiymat) qaytaradi (radianlarda berilgan).

Agar siz radian o'rniga darajalarni ishlatmoqchi bo'lsangiz, darajalarni radianga aylantirishingiz kerak:

Radianlardagi burchak = gradusdagi burchak x PI / 180.

```
Math.sin(90 * Math.PI / 180);     // 1 qaytaradi (90 darajaning sinusi)
```

### Math.cos()

`Math.cos(x)` x burchagining kosinusini (-1 va 1 orasidagi qiymat) qaytaradi (radianlarda berilgan).

Agar siz radian o'rniga darajalarni ishlatmoqchi bo'lsangiz, darajalarni radianga aylantirishingiz kerak:

Radianlardagi burchak = gradusdagi burchak x PI / 180.

```
Math.cos(0 * Math.PI / 180);     // 1 qaytaradi (90 darajaning sinusi)
```

### Math.min() va Math.max()

`Math.min()` va `Math.max()` argumentlar ro'yxatidagi eng kichik yoki eng katta qiymatni topish uchun ishlatilishi mumkin:

```
Math.min(0, 150, 30, 20, -8, -200);
```

```
Math.max(0, 150, 30, 20, -8, -200);
```

### Math.random()

`Math.random()` 0  va 1 orasidagi tasodifiy sonni qaytaradi:

```
Math.random();
```

{% hint style="warning" %}
Ushbu qo'llanmaning keyingi bo'limida `Math.random()` haqida ko'proq bilib olasiz.
{% endhint %}

### Math.log() metodi

`Math.log(x)` x ning natural logarifmini qaytaradi.

Tabiiy logarifm ma'lum bir o'sish darajasiga erishish uchun zarur bo'lgan vaqtni qaytaradi:

```
Math.log(1);
```

```
Math.log(2);
```

```
Math.log(3);
```

Math.E va Math.log() bir biriga o'xshaydi.

{% code title="10 ni olish uchun Math.E ni necha marta ko'paytirishimiz kerak ?" %}
```
Math.log(10); 
```
{% endcode %}

### Math.log2() metodi

`Math.log2(x)` x ning 2 ta logarifmini qaytaradi.

{% code title="8 ni olish uchun 2 ni necha marta ko'paytirishimiz kerak?" %}
```
Math.log2(8); 
```
{% endcode %}

### Math.log10() metodi

`Math.log10(x)` x ning 10 ta logarifmini qaytaradi.

{% code title="1000 ni olish uchun 10 ni necha marta ko'paytirishimiz kerak ?" %}
```
Math.log10(1000);
```
{% endcode %}

### Math metodlari

| Method                                                                 | Description                                                                   |
| ---------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [abs(x)](https://www.w3schools.com/jsref/jsref\_abs.asp)               | Returns the absolute value of x                                               |
| [acos(x)](https://www.w3schools.com/jsref/jsref\_acos.asp)             | Returns the arccosine of x, in radians                                        |
| [acosh(x)](https://www.w3schools.com/jsref/jsref\_acosh.asp)           | Returns the hyperbolic arccosine of x                                         |
| [asin(x)](https://www.w3schools.com/jsref/jsref\_asin.asp)             | Returns the arcsine of x, in radians                                          |
| [asinh(x)](https://www.w3schools.com/jsref/jsref\_asinh.asp)           | Returns the hyperbolic arcsine of x                                           |
| [atan(x)](https://www.w3schools.com/jsref/jsref\_atan.asp)             | Returns the arctangent of x as a numeric value between -PI/2 and PI/2 radians |
| [atan2(y, x)](https://www.w3schools.com/jsref/jsref\_atan2.asp)        | Returns the arctangent of the quotient of its arguments                       |
| [atanh(x)](https://www.w3schools.com/jsref/jsref\_atanh.asp)           | Returns the hyperbolic arctangent of x                                        |
| [cbrt(x)](https://www.w3schools.com/jsref/jsref\_cbrt.asp)             | Returns the cubic root of x                                                   |
| [ceil(x)](https://www.w3schools.com/jsref/jsref\_ceil.asp)             | Returns x, rounded upwards to the nearest integer                             |
| [cos(x)](https://www.w3schools.com/jsref/jsref\_cos.asp)               | Returns the cosine of x (x is in radians)                                     |
| [cosh(x)](https://www.w3schools.com/jsref/jsref\_cosh.asp)             | Returns the hyperbolic cosine of x                                            |
| [exp(x)](https://www.w3schools.com/jsref/jsref\_exp.asp)               | Returns the value of Ex                                                       |
| [floor(x)](https://www.w3schools.com/jsref/jsref\_floor.asp)           | Returns x, rounded downwards to the nearest integer                           |
| [log(x)](https://www.w3schools.com/jsref/jsref\_log.asp)               | Returns the natural logarithm (base E) of x                                   |
| [max(x, y, z, ..., n)](https://www.w3schools.com/jsref/jsref\_max.asp) | Returns the number with the highest value                                     |
| [min(x, y, z, ..., n)](https://www.w3schools.com/jsref/jsref\_min.asp) | Returns the number with the lowest value                                      |
| [pow(x, y)](https://www.w3schools.com/jsref/jsref\_pow.asp)            | Returns the value of x to the power of y                                      |
| [random()](https://www.w3schools.com/jsref/jsref\_random.asp)          | Returns a random number between 0 and 1                                       |
| [round(x)](https://www.w3schools.com/jsref/jsref\_round.asp)           | Rounds x to the nearest integer                                               |
| [sign(x)](https://www.w3schools.com/jsref/jsref\_sign.asp)             | Returns if x is negative, null or positive (-1, 0, 1)                         |
| [sin(x)](https://www.w3schools.com/jsref/jsref\_sin.asp)               | Returns the sine of x (x is in radians)                                       |
| [sinh(x)](https://www.w3schools.com/jsref/jsref\_sinh.asp)             | Returns the hyperbolic sine of x                                              |
| [sqrt(x)](https://www.w3schools.com/jsref/jsref\_sqrt.asp)             | Returns the square root of x                                                  |
| [tan(x)](https://www.w3schools.com/jsref/jsref\_tan.asp)               | Returns the tangent of an angle                                               |
| [tanh(x)](https://www.w3schools.com/jsref/jsref\_tanh.asp)             | Returns the hyperbolic tangent of a number                                    |
| [trunc(x)](https://www.w3schools.com/jsref/jsref\_trunc.asp)           | Returns the integer part of a number (x)                                      |

{% hint style="warning" %}
### Math haqida to'liq ma'lumotnoma

Math haqida to'liq ma'lumotnomani ko'rish uchun bizning [Math obekti haqida to'liq ma'lumotnoma](https://www.w3schools.com/jsref/jsref\_obj\_math.asp) sahifamizga o'ting:

Ma'lumotnomada Mathning barcha xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
