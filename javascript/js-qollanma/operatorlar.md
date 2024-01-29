# Operatorlar

{% hint style="success" %}
Qo'shish operatori <mark style="color:blue;">➕</mark> raqamlarni qo'shadi

Tayinlash operatori <mark style="color:blue;">🟰</mark> o'zgaruvchiga qiymat beradi.

![](../../.gitbook/assets/img\_operators.jpg)
{% endhint %}

## Javascriptda tayinlash

```javascript
let x = 10;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_equal" %}

{% code title="Qiymat belgilashga misollar" %}
```javascript
// x ga 5 qiymatini belgilash
let x = 5;
// y ga 2 qiymatini belgilash
let y = 2;
// z ga x + y qiymatini belgilash
let z = x + y;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper" %}

## Javascriptda qo'shish

Qo'shish operatori ( `+`) raqamlarni qo'shadi:

{% code title="Qo'shish" %}
```javascript
let x = 5;
let y = 2;
let z = x + y;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_add" %}

## Javascript ko'paytirish

Ko'paytirish operatori (`*`) raqamlarni ko'paytiradi.

{% code title="Ko'paytirish" %}
```javascript
let x = 5;
let y = 2;
let z = x * y;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_mult" %}

### JavaScript operatorlarining turlari

JavaScript operatorlarining har xil turlari mavjud:

* Arifmetik operatorlar
* Tayinlash operatorlari
* Taqqoslash operatorlari
* Mantiqiy operatorlar
* Shartli operatorlar
* Type operatorlari

### Arifmetik operatorlar

Arifmetik operatorlar raqamlar ustida arifmetik amallar bajarish uchun ishlatiladi:

<pre class="language-javascript" data-title="Arifmetik operatorlarga misol"><code class="lang-javascript"><strong>let a = 3;
</strong>let x = (100 + 50) * a;
</code></pre>

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_arithmetic_expressions" %}

| Operator | Tarif             |
| -------- | ----------------- |
| +        | Qo'shish          |
| -        | Ayirish           |
| \*       | Ko'paytirish      |
| \*\*     | Darajaga oshirish |
| /        | Bo'lish           |
| %        | Qoldiqli bo'lish  |
| ++       | Oshirish          |
| --       | Kamaytirish       |

{% hint style="warning" %}
## Eslatma

Arifmetik operatorlar [JS Arifmetika](arifmetik-amallar.md) bo'limida to'liq tushuntirilgan.
{% endhint %}

### JavaScript tayinlash operatorlari

Tayinlash operatorlari JavaScript o'zgaruvchilariga qiymat tayinlaydi.

**Qo'shishni tayinlash operatori**  (`+=`) o'zgaruvchiga qiymat qo'shadi.

<pre class="language-javascript" data-title="Tayinlash:"><code class="lang-javascript">let x = 10;
<strong>x += 5;
</strong></code></pre>

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_plusequal" %}

| Operator | Misol     | Bu bilan bir xil |
| -------- | --------- | ---------------- |
| =        | x = y     | x = y            |
| +=       | x += y    | x = x + y        |
| -=       | x -= y    | x = x - y        |
| \*=      | x \*= y   | x = x \* y       |
| /=       | x /= y    | x = x / y        |
| %=       | x %= y    | x = x % y        |
| \*\*=    | x \*\*= y | x = x \*\* y     |

{% hint style="warning" %}
Tayinlash operatorlari [JS ](https://www.w3schools.com/js/js\_arithmetic.asp)[Tayinlash](tayinlash.md) bo'limida to'liq tushuntirilgan.
{% endhint %}

### Taqqoslash operatorlari

| Operator | Ta'rif                         |
| -------- | ------------------------------ |
| ==       | ga teng                        |
| ===      | qiymati ham turi ham teng      |
| !=       | teng emas                      |
| !==      | qiymati ham turi ham teng emas |
| >        | dan katta                      |
| <        | dan kichik                     |
| >=       | dan katta yoki teng            |
| <=       | dan kichik yoki teng           |
| ?        | ternary operator               |

{% hint style="warning" %}
## Eslatma

Taqqoslash operatorlar [JS solishtirish ](taqqoslash.md)bo'limida to'liq tushuntirilgan.
{% endhint %}

### Stringni taqqoslash

Barcha taqqoslash operatorlarini stringlar ustida ham amalga oshirish mumkin

{% code fullWidth="false" %}
```javascript
let text1 = "A";
let text2 = "B";
let result = text1 < text2;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_string_comparison" %}

Stringlar alifbo tartibida taqqoslanishiga e'tibor bering:

```javascript
let text1 = "20";
let text2 = "5";
let result = text1 < text2;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_string_comparison1" %}

### Stringlarni qo'shish

`+` operatoridan stringlarni qo'shish (birlashtirish) uchun ham foydalanish mumkin.

```javascript
let text1 = "John";
let text2 = "Doe";
let text3 = text1 + " " + text2;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_string_comparison" %}

`+=` operatoridan stringlarni qo'shish (birlashtirish) uchun ham ishlatilishi mumkin:

{% hint style="info" %}
<pre class="language-javascript"><code class="lang-javascript"><strong>let text1 = "What a very";
</strong><strong>text1 += " nice day";
</strong></code></pre>

text1 ning natijasi quyidagicha bo'ladi:

<pre><code><strong>What a very nice day
</strong></code></pre>
{% endhint %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_concat4" %}

{% hint style="warning" %}
## Eslatma

Stringlardan foydalanganda`+`operatori birlashtiruvchi operator deb ataladi.
{% endhint %}

### Stringlar va raqamlarni qo'shish

Ikki raqamni qo'shish raqamlarning yig'indisini qaytaradi, lekin raqam va stringni qo'shish string qaytaradi:

{% hint style="info" %}
<pre class="language-javascript"><code class="lang-javascript"><strong>let x = 5 + 5;
</strong><strong>let y = "5" + 5;
</strong><strong>let z = "Hello" + 5;
</strong></code></pre>

_`x`_, _`y`_ va _`z`_ ning natijasi quyidagicha bo'ladi:

<pre><code><strong>10
</strong><strong>55
</strong><strong>Hello5
</strong></code></pre>
{% endhint %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_concat5" %}

{% hint style="warning" %}
## Eslatma

Agar siz raqam va stringni bir biriga qo'shsangiz, natija string  bo'ladi!
{% endhint %}

### JavaScript mantiqiy operatorlari

| Operator | Ta'rif |
| -------- | ------ |
| &&       | va     |
| \|\|     | yoki   |
| !        | emas   |

{% hint style="warning" %}
## Eslatma

Mantiqiy operatorlar [JS solishtirish ](taqqoslash.md)bo'limida to'liq tushuntirilgan.
{% endhint %}

### Type operatorlar

| Operator   | Ta'rif                                                                |
| ---------- | --------------------------------------------------------------------- |
| typeof     | O'zgaruvchi turini qaytaradi                                          |
| instanceof | Agar obyekt obyekt turining namunasi bo'lsa, true qiymatini qaytaradi |

{% hint style="warning" %}
## Eslatma

Tur operatorlari [turlarni konvertatsiyalash](turni-ozgartirish.md) bo'limida to'liq tushuntirilgan.
{% endhint %}

### Bitwise operatorlar

Bit operatorlari 32 bitli raqamlarda ishlaydi.

Jarayondagi har qanday raqamli operand 32 bitli raqamga aylantiriladi. Natija yana JavaScript raqamiga aylantiriladi.

| Operator | Ta'rif               | Misol   | Bu bilan bir xil | Result | Decimal |
| -------- | -------------------- | ------- | ---------------- | ------ | ------- |
| &        | VA                   | 5 & 1   | 0101 & 0001      | 0001   |  1      |
| \|       | YOKI                 | 5 \| 1  | 0101 \| 0001     | 0101   |  5      |
| \~       | EMAS                 | \~ 5    |  \~0101          | 1010   |  10     |
| ^        | XOR                  | 5 ^ 1   | 0101 ^ 0001      | 0100   |  4      |
| <<       | left shift           | 5 << 1  | 0101 << 1        | 1010   |  10     |
| >>       | right shift          | 5 >> 1  | 0101 >> 1        | 0010   |   2     |
| >>>      | unsigned right shift | 5 >>> 1 | 0101 >>> 1       | 0010   |   2     |

{% hint style="warning" %}
Yuqoridagi misollarda 4 bitli unsigned misollar qo'llanilgan. Ammo JavaScript 32 bitli unsigned  raqamlardan foydalanadi.

Shu sababli, JavaScript-da \~ 5 10 ni qaytarmaydi. U -6 ni qaytaradi.\
\~00000000000000000000000000000101 1111111111111111111111111111010ni qaytaradi&#x20;

Bitwise operatorlar [JS Bitwise](bitwise.md) bo'limida to'liq tushuntirilgan.
{% endhint %}
