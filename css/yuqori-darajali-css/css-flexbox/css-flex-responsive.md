# CSS Flex responsive

### Responsiv Flexbox

CSSning <mark style="color:green;">Media querielar</mark> bo'limida turli ekran o'lchamlari va qurilmalarga har xil layoutlar yaratish uchun media querielardan foydalanishingiz mumkinligini o'rgandingiz.

<figure><img src="../../../.gitbook/assets/image (525).png" alt=""><figcaption></figcaption></figure>

Misol uchun, agar ko'p uchraydigan ekran o'lchamlari uchun ikki ustunli layout va kichik ekran o'lchamlari uchun (masalan, telefonlar va planshetlar) bir ustunli layout yaratmoqchi bo'lsangiz, ma'lum bir to'xtash nuqtasida `flex-direction`ni `row`dan `column`ga o'zgartirishingiz mumkin (quyidagi misolda 800px):

```
.flex-container {
  display: flex;
  flex-direction: row;
}

/* Responsive layout - makes a one column layout instead of a two-column layout */
@media (max-width: 800px) {
  .flex-container {
    flex-direction: column;
  }
}
```

Turli ekran o'lchamlariga moslashadigan har xil layout yaratishning yana bir usuli, moslashuvchan  elementlardagi flex xususiyatlarining foizini o'zgartirishdir. Ushbu misoldagi kod ishlashi uchun flex konteynerida `flex-wrap: wrap;` borligiga e'tibor bering:

```
.flex-container {
  display: flex;
  flex-wrap: wrap;
}

.flex-item-left {
  flex: 50%;
}

.flex-item-right {
  flex: 50%;
}

/* Responsive layout - makes a one column layout instead of a two-column layout */
@media (max-width: 800px) {
  .flex-item-right, .flex-item-left {
    flex: 100%;
  }
}
```

### Flexbox yordamida moslashuvchan rasmlar galereyasi

Ekran o'lchamiga qarab to'rt, ikki yoki butun ekran kengligida ko'rsatiladigan moslashuvchan rasmlar galereyasini yaratish uchun flexbox-dan foydalaning:

<figure><img src="../../../.gitbook/assets/image (508).png" alt=""><figcaption></figcaption></figure>

### Flexbox-dan foydalangan holda moslashuvchan veb-sayt tuzish

Moslashuvchan navbar va moslashuvchan kontentdan iboradi responsive sayt yaratish uchun flexbox-dan foydalaning:

<figure><img src="../../../.gitbook/assets/image (390).png" alt=""><figcaption></figcaption></figure>
