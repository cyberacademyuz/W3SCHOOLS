# String template-lar

{% hint style="success" %}
Sinonimlar:

* Template literallar
* Template stringlar
* String templatelar
* Back-Ticlar sintaksisi
{% endhint %}

### Back-Ticlar sintaksisi

Template literallar stringni ifodalash uchun qo'shtirnoq ("") o'rniga back-tic (\`\`) belgilaridan foydalanadi:

```javascript
let text = `Hello World!`;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_templates" %}

### String ichida tinish berilgilari

Template literallar yordamida string ichida bir tirnoqdan ham qoʻsh tirnoqdan ham foydalanishingiz mumkin:

```javascript
let text = `He's often called "Johnny"`;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_templates_quotes" %}

### Bir necha qatorli stringlar

Template literallar bir necha qatorli stringlardan foydalanishga ruxsat beradi:

```javascript
let text =
`The quick
brown fox
jumps over
the lazy dog`;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_templates_multiline" %}

### Interpolyatsiya

Template literallar o'zgaruvchilar va expressionlarni stringlarga interpolyatsiya qilishning osonlashtiradi.

Bu usul string interpolyatsiyasi deb ataladi.

Manabu uning sintaksisi:

```
${...}
```

### O'zgaruvchi bilan ishlatish

Template literallar string ichida o'zgaruvchilardan foydalanish imkonini beradi:

```javascript
let firstName = "John";
let lastName = "Doe";

let text = `Welcome ${firstName}, ${lastName}!`;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_templates_variables" %}

{% hint style="warning" %}
O'zgaruvchilarni asl qiymatlar bilan avtomatik tarzda almashtirish string interpolatsiyasi deb ataladi.
{% endhint %}

### Expressiondan foydalanish

Template literallar string ichida ekspressionlardan doydalanishga ruxsat beradi:

```javascript
let price = 10;
let VAT = 0.25;

let total = `Total: ${(price * (1 + VAT)).toFixed(2)}`;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_templates_expressions" %}

{% hint style="warning" %}
Expressionlarni asl qiymatlar bilan avtomatik ravishda almashtirish string interpolatsiyasi deb ataladi.
{% endhint %}

### HTML templatelar

```javascript
let header = "Templates Literals";
let tags = ["template literals", "javascript", "es6"];

let html = `<h2>${header}</h2><ul>`;
for (const x of tags) {
  html += `<li>${x}</li>`;
}

html += `</ul>`;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_templates_html" %}

### Brauzerni qo'llab-quvvatlash

`Template Literals` ES6 xususiyatidir (JavaScript 2015).

U barcha zamonaviy brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge | Firefox | Safari |       |
| ------ | ---- | ------- | ------ | ----- |
| Chrome | Edge | Firefox | Safari | Opera |
| Yes    | Yes  | Yes     | Yes    | Yes   |

`Template Literallar` Internet Explorer-da qo'llab-quvvatlanmaydi.

{% hint style="warning" %}
### String haqida to'liq ma'lumotnoma

String haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda string haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_string.asp)

Ma'lumotnomada barcha string xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
