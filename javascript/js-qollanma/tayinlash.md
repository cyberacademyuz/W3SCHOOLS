# Tayinlash

## Javascrip tayinlash operatorlari

Tayinlash opertorlari javascript o'zgaruvchisiga qimat tayinlaydi.

| Operator | Misol     | Xuddi bu kabi |
| -------- | --------- | ------------- |
| =        | x = y     | x = y         |
| +=       | x += y    | x = x + y     |
| -=       | x -= y    | x = x - y     |
| \*=      | x \*= y   | x = x \* y    |
| /=       | x /= y    | x = x / y     |
| %=       | x %= y    | x = x % y     |
| \*\*=    | x \*\*= y | x = x \*\* y  |

### Shiftni tayinlash operatorlari

| Operator | Misol    | Xuddi bu kabi |
| -------- | -------- | ------------- |
| <<=      | x <<= y  | x = x << y    |
| >>=      | x >>= y  | x = x >> y    |
| >>>=     | x >>>= y | x = x >>> y   |

### Bit bo'yicha tayinlash operatorlari

| Operator | Misol   | Xuddi bu kabi |
| -------- | ------- | ------------- |
| &=       | x &= y  | x = x & y     |
| ^=       | x ^= y  | x = x ^ y     |
| \|=      | x \|= y | x = x \| y    |

### Mantiqiy tayinlash operatorlari

| Operator | Misol     | Xuddi bu kabi      |
| -------- | --------- | ------------------ |
| &&=      | x &&= y   | x = x && (x = y)   |
| \|\|=    | x \|\|= y | x = x \|\| (x = y) |
| ??=      | x ??= y   | x = x ?? (x = y)   |

{% hint style="warning" %}
### Eslatma

Mantiqiy tayisnlash operatorlari [ES2020 ](../js-versiyalari/js-2020.md)hisoblanadi.
{% endhint %}

## = operatori

Oddiy tayinlash operatori o'zgaruvchiga qiymat beradi.

{% code title="Oddiy tayinlash operatoriga misollar" %}
```javascript
let x = 10;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_equal" %}

```javascript
let x = 10 + y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_equal2" %}

### += operatori

Qo'shishni tayinlash operatori o'zgaruvchiga qiymat qo'shadi.

{% code title="Qo'shishni tayinlash operatoriga misollar" %}
```javascript
let x = 10;
x += 5;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_plusequal" %}

```javascript
let text = "Hello"; text += " World";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_plusequal2" %}

### -= operatori

Ayirishni tayinlash operatori o'zgaruvchidan qiymatni ayiradi.

{% code title="Ayirishni tayinlash operatoriga misollar" %}
```javascript
let x = 10;
x -= 5;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_minequal" %}

### \*= operatori

Ko'paytiruvni tayinlash operatori o'zgaruvchini ko'paytiradi.

{% code title="Ko'paytirishni tayinlash operatoriga misollar" %}
```javascript
let x = 10;
x *= 5;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_multequal" %}

### \*\*= operatori

Daraja oshirishni tayinlash operatori o'zgaruvchini operandning darajasiga oshiradi.

```javascript
let x = 10;
x **= 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_exponential" %}

### /= operatori

Bo'lisni tayinlash operatori o'zgaruvchini ajratadi.

```javascript
let x = 10;
x /= 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_divequal" %}

### %= operatori

Qoldiqni tayinlash operatori o'zgaruvchiga qoldiqni tayinlaydi.

```javascript
let x = 10;
x %= 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_modequal" %}

### <<= operatori

keft shift tayinlash operatori o'zgaruvchini chapga siljitadi.

```javascript
let x = -100;
x <<= 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_left_shift" %}

### >>= Operator

Right shift tayinlash operatori o'zgaruvchini o'ngga siljitadi (signed).

```javascript
let x = -100;
x >>= 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_right_shift" %}

### >>>= operator

Unsigned Right Shift tayinlash operatori o'zgaruvchini (imzosiz) o'ngga siljitadi.

```javascript
let x = -100;
x >>>= 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_unsigned_right_shift" %}

### &= operatori

Bitwise AND tayinlash operatori ikkita operandda bitli AND amalini bajaradi va natijani o‘zgaruvchiga tayinlaydi.

```javascript
let x = 10;
x &= 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_bitwise_and" %}

### |= operatori

Bitwise OR tayinlash operatori ikkita operandda bitli OR amalinin bajaradi va natijani o'zgaruvchiga tayinlaydi.

```javascript
let x = 10;
x |= 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_bitwise_or" %}

### ^= operatori

Bitwise XOR tayinlash operatori ikkita operandda bitli XOR amalini bajaradi va natijani o'zgaruvchiga tayinlaydi.

```javascript
let x = 10;
x ^= 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_bitwise_xor" %}

### &&= operatori

Mantiqiy AND tayinlash operatori ikkita qiymat orasida ishlatiladi.

Agar birinchi qiymat rost bo'lsa, ikkinchi qiymat tayinlanadi.

```javascript
let x = 10;
x &&= 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_logical_and_and" %}

{% hint style="warning" %}
`&&=` operatori [ES2020](../js-versiyalari/js-2020.md) xususiyati hisoblanadi.
{% endhint %}

### ||= operatori

Mantiqiy OR tayinlash operatori ikkita qiymat orasida ishlatiladi.

Agar birinchi qiymat noto'g'ri bo'lsa, ikkinchi qiymat tayinlanadi.

```javascript
let x = 10;
x ||= 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_logical_or_or" %}

{% hint style="warning" %}
`||=` operatori [ES2020](../js-versiyalari/js-2020.md) xususiyati hisoblanadi.
{% endhint %}

### ??= operatori

Nullish birlashtiruvchi tayinlash operatori ikkita qiymat o'rtasida ishlatiladi.

Agar birinchi qiymat undefined yoki null bo'lsa, ikkinchi qiymat tayinlanadi.

```javascript
let x = 10;
x ??= 5;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_assign_nullish" %}

{% hint style="warning" %}
&#x20;`??=`operator [ES2020](../js-versiyalari/js-2020.md)[ ](https://www.w3schools.com/js/js\_2020.asp)xususiyati hisoblanadi.
{% endhint %}
