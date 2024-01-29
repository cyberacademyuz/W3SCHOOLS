# Font google

### Google fonts <a href="#google-fonts" id="google-fonts"></a>

Agar HTML dagi standard fontlardan foydalanishni istamasangiz, unda Google Fonts dan foydalanishingiz mumkin.

Google Fontsdan foydalanish bepul va mingdan ortiq shriftlarga ega,

### Google Fonts dan foydalanish <a href="#google-fonts-dan-foydalanish" id="google-fonts-dan-foydalanish"></a>

Buning uchun shunchaki `<head>` bo'limiga style sheet link qo'ying va CSS da shriftga murojaat qiling.

{% code title="Bu yerda Google Fonts-dagi "Sofiya" nomli shriftdan foydalanmoqchimiz:" %}
```
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia">
<style>
body {
  font-family: "Sofia", sans-serif;
}
</style>
</head>
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (476).png" alt=""><figcaption></figcaption></figure>

{% code title="Bu yerda Google Fonts-dagi "Trirong" nomli shriftdan foydalanmoqchimiz:" %}
```
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Trirong">
<style>
body {
  font-family: "Trirong", serif;
}
</style>
</head>
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

{% code title="Bu yerda Google Fonts-dagi "Audiowide" nomli shriftdan foydalanmoqchimiz:" %}
```
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Audiowide">
<style>
body {
  font-family: "Audiowide", sans-serif;
}
</style>
</head>
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (517).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Eslatma:** CSS da shriftdan belgilayotganingizda, har doim kamida bitta fallback shriftidan foydalanig (har ehtimolga qarshi). Shunday qilib bu shriftlar ro'yhatining oxiriga ham umumiy shrift oilasini (masalan, serif yoki sans-serif) qo'shishingiz kerak.
{% endhint %}

Google fontsda mavjud barcha shriftlar roʻyxatini ko'rish uchun “<mark style="color:green;">Qanday qilinadi – Google Fonts qoʻllanmasi</mark>" sahifamizga o'ting.

### Bir nechta Google Fonts dan foydalanish <a href="#bir-nechta-google-font-dan-foydalanish" id="bir-nechta-google-font-dan-foydalanish"></a>

Google fontsdagi bir nechta shriftlardan foydalanish uchun, shunchaki shrift nomlarining orasini | belgisi bilan ajrating.

{% code title="Bir nechta fontlarni ishlatiishga request jo'natish" %}
```
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Audiowide|Sofia|Trirong">
<style>
h1.a {font-family: "Audiowide", sans-serif;}
h1.b {font-family: "Sofia", sans-serif;}
h1.c {font-family: "Trirong", serif;}
</style>
</head>
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (316).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Note:** Sahifangizda bir nechta shriftlardan foydalanish, sahifaning yuklanish tezligiga ta'sir qilishi mumkin! Shu sabab ehtiyot bo'ling!
{% endhint %}

### Google Fonts shriftlariga still berish <a href="#google-font-larni-bezash" id="google-font-larni-bezash"></a>

Albatta Google fonts shriftlariga ham o'zingiz xohlagandek still berishingiz mumkin.

{% code title="Sofia fontini bezash:" %}
```
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia">
<style>
body {
  font-family: "Sofia", sans-serif;
  font-size: 30px;
  text-shadow: 3px 3px 3px #ababab;
}
</style>
</head>
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (472).png" alt=""><figcaption></figcaption></figure>

### Font effektlarini yoqish <a href="#font-effektlarini-yoqish" id="font-effektlarini-yoqish"></a>

Google foydalanishingiz mumkin bo'lgan turli xil shrift effektlarini ham yaratdi.

Bunday effektlardan foydalanish uchun avval Google API-ning ohiriga `effect=effectname` ni qo'shamiz va maxsus effekt bermoqchi bo'lgan elementimizga maxsus class nomini beramiz. Class nomi har doim `font-effect-` bilan boshlanadi va `effectname` bilan tugaydi.

{% code title=""Sofia" fontiga olov effektini qo'shamiz:" %}
```
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia&effect=fire">
<style>
body {
  font-family: "Sofia", sans-serif;
  font-size: 30px;
}
</style>
</head>
<body>

<h1 class="font-effect-fire">Sofia on Fire</h1>

</body>
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (91).png" alt=""><figcaption></figcaption></figure>

Turli effektlardan bir vaqtda foydalanish uchun Google APIdagi effekt nomlarini chiziq belgisi | bilan ajratib chiqing:

{% code title="Sofia shriftiga bir qancha effekt qo'shish:" %}
```
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia&effect=neon|outline|emboss|shadow-multiple">
<style>
body {
  font-family: "Sofia", sans-serif;
  font-size: 30px;
}
</style>
</head>
<body>

<h1 class="font-effect-neon">Neon Effect</h1>
<h1 class="font-effect-outline">Outline Effect</h1>
<h1 class="font-effect-emboss">Emboss Effect</h1>
<h1 class="font-effect-shadow-multiple">Multiple Shadow Effect</h1>

</body>
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (483).png" alt=""><figcaption></figcaption></figure>
