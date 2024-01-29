# Scope

{% hint style="success" %}
Scopelar oʻzgaruvchilarning koʻrinish doirasini belgilaydi.&#x20;

Javascriptda 3 turdagi scope mavjud:

* Blok scope
* Funktsiya scope
* Global scope
{% endhint %}

### Blok scope

Block scope - Ec6 (2015) dan oldin Javascriptda faqatgina Global scope va function scope boʻlgan.

EC6 2ta muhim let va const kalit soʻzlarini taqdim qildi.

Ushbu ikki kalit so'z JavaScript-da blok scopeni taqdim qiladi.

{ } blokida e'lon qilingan o'zgaruvchilarga blokdan tashqarida turib murojaat qilish mumkin emas:

```
{
  let x = 2;
}
// x can NOT be used here
```

`var` kalit soʻzi bilan eʼlon qilingan oʻzgaruvchi block scopega ega boʻlmaydi.

{ } blokida e'lon qilingan o'zgaruvchilarga blokdan tashqarida turib murojaat qilish mumkin:

```
{
  var x = 2;
}
// x CAN be used here
```

### Lokal scope

JavaScript funktsiyasi ichida e'lon qilingan o'zgaruvchilar funktsiya uchun lokal oʻzgarvchi bo'ladi.

```
// code here can NOT use carName

function myFunction() {
  let carName = "Volvo";
  // code here CAN use carName
}

// code here can NOT use carName
```

{% hint style="warning" %}
Local oʻzgaruvchilar funksiya scopiga ega boʻladi.

Ularga faqat funksiya ichda murojaat qilish mumkin
{% endhint %}

Lokal o'zgaruvchilar faqat ularning funktsiyalari ichida tan olinganligi sababli, bir xil nomdagi o'zgaruvchilarni boshqa funktsiyalar ichida ishlatilish mumkin.

Lokal o'zgaruvchilar funktsiya ishga tushganda yaratiladi va funktsiya tugallangandan keyin o'chiriladi.

### Funksiya scope

JavaScript funksiya doirasiga ega: Har bir funksiya yangi scope yaratadi.

Funktsiya ichida eʼlon qilingan o'zgaruvchilarga funksiya tashqarisidan murojaat qilish mumkin emas.

`var`, `let` va `const` bilan e'lon qilingan o'zgaruvchilar funktsiya ichida e'lon qilinganda bir xil.

Bularning barchasi Funktsiya doirasiga ega:

```
function myFunction() {
  var carName = "Volvo";   // Function Scope
}
```

```
function myFunction() {
  let carName = "Volvo";   // Function Scope
}
```

```
function myFunction() {
  const carName = "Volvo";   // Function Scope
}
```

### Global o'zgaruvchilar

Funksiya tashqarisida eʼlon qilingan oʻzgaruvchilar global oʻzgaruvchi boʻladi

```
let carName = "Volvo";
// code here can use carName

function myFunction() {
// code here can also use carName
}
```

{% hint style="warning" %}
Global oʻzgaruvchi global scopega ega boʻladi.

Veb-sahifadagi barcha skriptlar va funksiyalar unga murojaat qilishi mumkin
{% endhint %}

### Global scope

**Global scopeda** e'lon qilingan o'zgaruvchilar (har qanday funktsiyadan tashqari) **Global Scope ga** ega .

Global o'zgaruvchilarga JavaScript dasturining istalgan joyidan murojaat qilish mumkin.

`Var`, `let` va `const` bilan e'lon qilingan o'zgaruvchilar blokdan tashqarida e'lon qilinganda juda o'xshashdir.

Bularning barchasi global scopega ega:

```
var x = 2;       // Global scopelet
```

```
x = 2;       // Global scopeconst
```

```
x = 2;       // Global scope
```

### JavaScript o'zgaruvchilari

JavaScript-da obyektlar va funktsiyalar ham o'zgaruvchilardir

{% hint style="warning" %}
Scope kodning turli qismlarida o'zgaruvchilarga, obektlar va funktsiyalarga murojaat qilish imkoniyatini belgilaydi.
{% endhint %}

### Avtomatik global

Agar siz e'lon qilinmagan o'zgaruvchiga qiymat bersangiz, u avtomatik ravishda GLOBAL o'zgaruvchiga aylanadi.

Ushbu misoldagi kod, oʻzgaruvchi qiymati funktsiya ichida tayinlangan bo'lsa ham, carName nomli global o'zgaruvchi e'lon qiladi.

```
myFunction();

// code here can use carName

function myFunction() {
  carName = "Volvo";
}
```

### Strict mode

Barcha zamonaviy brauzerlar JavaScript-ni "Strict Mode" da ishga tushirishni qo'llab-quvvatlaydi.

Ushbu qo'llanmaning keyingi boʻlimida qat'iy rejimdan qanday foydalanish haqida batafsil bilib olasiz.

{% hint style="danger" %}
"Qat'iy rejim" da e'lon qilinmagan o'zgaruvchilar yuqoridagi kabi avtomatik tarzda global oʻzgaruvchiga aylanmaydi.
{% endhint %}

### HTMLdagi global o'zgaruvchilar

JavaScript bilan global scope JavaScriptning muhitidir.

HTMLda global scope windowning obyekti hisoblanadi.

`var` kalit so'zi bilan e'lon qilingan global o'zgaruvchilar window obyektiga tegishli:

```
var carName = "Volvo";
// code here can use window.carName
```

Let kalit so'zi bilan eʼlon qilingan global o'zgaruvchilar window obyektiga tegishli emas:

```
let carName = "Volvo";
// code here can not use window.carName
```

### Ogohlantirish

{% hint style="danger" %}
Agar xohlamasangiz, global o'zgaruvchi yaratmang.

Sizning global o'zgaruvchilaringiz (yoki funksiyalaringiz) window o'zgaruvchilari (yoki funksiyalar) oʻniga qayta yozishi mumkin.

Har qanday funksiya, shu jumladan window obyekti global o'zgaruvchilaringiz va funktsiyalaringizni qayta yozishi mumkin.
{% endhint %}

### JavaScript o'zgaruvchilarning ishlash muddati

Javascript oʻzgaruvchilarining ishlash muddati uni eʼlon qilingan vaqtdan boshlanadi.

Funksiya (ichki) oʻzgaruvchilari funksiya ishga tushganida eʼlon qilinadi.

Brauzerda, brauzer oynasini yoki tabni yopganingizda oʻzgaruvchilar oʻchiriladi.

### Funktsiya argumentlari

Funksiya argumenlari (parametrlar) funksiya ichidagi lokal oʻzgaruvchilar kab ishlaydi.
