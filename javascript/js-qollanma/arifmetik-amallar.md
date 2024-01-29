# Arifmetik amallar

### JavaScript arifmetik operatorlari

Arifmetik operatorlar raqamlar (harf yoki o'zgaruvchilar) bo'yicha arifmetik amallar bajaradi.

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

## Arifmetik amallar

Odatda arifmetik amal ikki raqam ustida ishlaydi.

Ikki raqam aynan raqamning o'zi bo'lishi mumkin:

```javascript
let x = 100 + 50;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_arithmetic_operation" %}

yoki o'zgaruvchi bo'lishi mumkin:

```javascript
let x = a + b;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_arithmetic_variables" %}

yoki expressionlar bo'lishi mumkin:

```javascript
let x = (100 + 50) * a;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_arithmetic_expressions" %}

### Operatorlar va operandlar

Raqamlar (arifmetik amalda) **operandlar** deb ataladi.

Amal (ikki operand o'rtasida bajarilishi kerak) **operator** tomonidan belgilanadi

<table><thead><tr><th width="263.3333333333333">Operand</th><th>Operator</th><th>Operand</th></tr></thead><tbody><tr><td>100</td><td>+</td><td>50</td></tr></tbody></table>

### Qo'shish

**Qo'shish** operatori (`+`) raqamlarni qo'shadi:

```javascript
let x = 5;
let y = 2;
let z = x + y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_add" %}

### Ayirish

**Ayirish** operatori (`-`) raqamlarni ayiradi.

```javascript
let x = 5;
let y = 2;
let z = x - y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_sub" %}

### Ko'paytirish

**Ko'paytirish** operatori (`*`) raqamlarni ko'paytiradi.

```javascript
let x = 5;
let y = 2;
let z = x * y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_mult" %}

### Bo'lish

**Bo'lish** operatori (`/`) raqamlarni bo'ladi.

```javascript
let x = 5;
let y = 2;
let z = x / y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_div" %}

### Qoldiqli bo'lish

Qoldiqli bo'lish operatori (`%`) raqamlar bo'linganda  ularning qoldig'ini qaytaradi.

```javascript
let x = 5;
let y = 2;
let z = x % y;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_mod" %}

{% hint style="warning" %}
Arifmetikada ikkita butun sonni bo'lish bo'linma va qoldiqni hosil qiladi.

Matematikada qoldiqli bo'lish amalining natijasi bo'lish amalidan qaytgan qiymatning qoldiq qismidir.
{% endhint %}

### Oshirish

**Oshirish** operatori (`++`) raqamlarni oshiradi.

```javascript
let x = 5;
x++;
let z = x;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_increment" %}

### Kamaytirish

**Kamaytirish** operatori (`--`) raqamlarni kamaytiradi.

```javascript
let x = 5;
x--;
let z = x;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_decrement" %}

### Darajaga orttirish

**Darajaga orttirish** operatori (`**`) birinchi operandni ikkinchi operandning darajasiga orttiradi.

```javascript
let x = 5;
let z = x *-* 2;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_arithmetric_exponent1" %}

x \*\* y xuddi `Math.pow(x,y)` ning natijasi kabi natija qaytaradi:

```javascript
let x = 5;
let z = Math.pow(x,2);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_arithmetric_exponent2" %}

### Operator ustunligi

Operator ustunligi arifmetik ifodada amallarning bajarilish tartibini belgilaydi.

```javascript
let x = 100 + 50 * 3;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_arithmetic_precedence1" %}

Yuqoridagi misolning natijasi 150 \* 3 bilan bir xilmi yoki 100 + 150 bilan bir xilmi ?

Birinchi qo'shish yoki ko'paytirish amalga oshiriladimi ?

Maktab matematikasida bo'lgani kabi, birinchi navbatda ko'paytirish amalga oshiriladi.

Ko'paytirish (`*`) va bo'lish (`/`) qo'shish (`+`) va ayirish (`-`) ga qaraganda yuqoriroq ustunlikka ega**.**

Va (maktab matematikasidagi kabi) qavslar yordamida  bu ustunlikni o'zgartirish mumkin.

Qavslardan foydalanganda avval qavs ichidagi amallar hisoblanadi:

```javascript
let x = (100 + 50) * 3;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_arithmetic_precedence2" %}

Agar ko'p amallar bir xil ustunlikka ega bo'lsa (qo'shish va ayirish yoki ko'paytirish va bo'lish kabi), ular chapdan o'ngga hisoblanadi:

```javascript
let x = 100 + 50 - 3;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_arithmetic_precedence4" %}

```javascript
let x = 100 / 50 * 3;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_arithmetic_precedence3" %}

{% hint style="warning" %}
### Eslatma

Operator ustunligi haqida toʻliq roʻyxatini ko'rish uchun quyidagi sahifaga oʻting:

[Operatorlarning ustunlik qiymatlari](ustunlik.md).
{% endhint %}
