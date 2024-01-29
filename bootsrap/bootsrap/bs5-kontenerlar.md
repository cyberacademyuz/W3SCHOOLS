# BS5 Kontenerlar

### Bootstrap 5 konteynerlari

Oldingi bo'limda bilib oldingizdek, Bootstrap sayt tarkibini oʻrab turish uchun konteyner talab qiladi.

Konteynerlar ularning ichidagi tarkibni to'ldirish uchun ishlatiladi va ikkita konteyner klassi mavjud:

1. `.container` classi moslashuvchan kenglikdagi konteyner taqdim qiladi
2. `.container-fluid` classi ko'rish oynasining butun kengligini qamrab oluvchi to'liq kenglikdagi konteyner taqdim etadi

<figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

### Fixed konteyner

Moslashuvchan, belgilangan kenglikdagi konteyner yaratish uchun `.container` classidan foydalaning.

E'tibor bering, uning kengligi (`max-width`) turli ekran o'lchamlarida o'zgaradi:

|           | <p>Juda kichik<br>&#x3C;576px</p> | <p>Kichik<br>≥576px</p> | <p>Oʻrtacha<br>≥768px</p> | <p>Katta<br>≥992px</p> | <p>Juda katta<br>≥1200px</p> | <p>XXL<br>≥1400px</p> |
| --------- | --------------------------------- | ----------------------- | ------------------------- | ---------------------- | ---------------------------- | --------------------- |
| max-width | 100%                              | 540px                   | 720px                     | 960px                  | 1140px                       | 1320px                |

Quyidagi misolni oching va brauzer oynasining hajmio'lchamini o'zgartiring, shunda konteyner kengligi turli to'xtash nuqtalarida o'zgaradi:

```
<div class="container">
  <h1>My First Bootstrap Page</h1>
  <p>This is some text.</p>
</div>
```

{% hint style="warning" %}
XXL o'lchami (≥1400px) Bootstrap 5-da yangi qo'shilgan o'lcham**, Bootstrap 4**-dagi eng katta to'xtash nuqtasi **Extra large (≥1200px).**
{% endhint %}

### Fluid kenteyner

To'liq kenglikdagi konteyner yaratish uchun `.container-fluid` classidan foydalaning, u har doim ekranning butun kengligini qamrab oladi (`width`har doim `100%`):

```
<div class="container-fluid">
  <h1>My First Bootstrap Page</h1>
  <p>This is some text.</p>
</div>
```

### Konteyner Padding

Standart holatda, konteynerlar chap va o'ng tomon uchun paddinglarga ega, ammo tepa va pastki paddingga ega emas. Shuning uchun ko'pincha **extra padding**lar va **margin**lar kabi **spacing utilita**laridan sahifani yanada yaxshi ko'rinishga keltirish uchun foydalanamiz. Masalan, `.pt-5` "tepaga katta padding qo'shish" degan ma'noni anglatadi:

```
<div class="container pt-5"></div>
```

### Konteyner chegarasi va rangi

Chegaralar va ranglar kabi boshqa yordamchi utilitalar ham konteynerlar bilan birgalikda ishlatiladi:

<figure><img src="../../.gitbook/assets/image (618).png" alt=""><figcaption></figcaption></figure>

```
<div class="container p-5 my-5 border"></div>

<div class="container p-5 my-5 bg-dark text-white"></div>

<div class="container p-5 my-5 bg-primary text-white"></div>
```

{% hint style="warning" %}
Ranglar va chegara utilitalari haqida keyingi bo'limda ko'proq bilib olasiz.
{% endhint %}

### Moslashuvchan konteynerlar

Konteyner qachon moslashishi kerakligini belgilash uchun `.container-sm|md|lg|xl` classlaridan ham foydalanishingiz mumkin .

Konteynerning `max-width` qiymati turli ekran o'lchamlari/viewportlarda o'zgaradi:

| Class            | Juda kichik <576px | Kichik ≥576px | Oʻrtacha ≥768px | Katta ≥992px | Juda katta ≥1200px | XXL ≥1400px |
| ---------------- | ------------------ | ------------- | --------------- | ------------ | ------------------ | ----------- |
| `.container-sm`  | 100%               | 540px         | 720px           | 960px        | 1140px             | 1320px      |
| `.container-md`  | 100%               | 100%          | 720px           | 960px        | 1140px             | 1320px      |
| `.container-lg`  | 100%               | 100%          | 100%            | 960px        | 1140px             | 1320px      |
| `.container-xl`  | 100%               | 100%          | 100%            | 100%         | 1140px             | 1320px      |
| `.container-xxl` | 100%               | 100%          | 100%            | 100%         | 100%               | 1320px      |

```html
<div class="container-sm">.container-sm</div>
<div class="container-md">.container-md</div>
<div class="container-lg">.container-lg</div>
<div class="container-xl">.container-xl</div>
<div class="container-xxl">.container-xxl</div>
```

### Bilasizmi ?

W3.CSS Bootstrap 5 uchun ajoyib alternativ hisoblanadi.

Agar W3.CSS-ni o'rganmoqchi bo'lsangiz, bizning [W3.CSS qo'llanma](https://www.w3schools.com/w3css/default.asp)mizga o'ting.
