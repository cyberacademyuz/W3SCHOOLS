# Grid Konteyner

<figure><img src="../../.gitbook/assets/image (462).png" alt=""><figcaption></figcaption></figure>

## Grid konteyner

HTML elementi grid konteyneri sifatida ishlashi uchun `display` xususiyatni `grid` yoki `inline-grid` qilishingiz kerak.

Grid konteynerlari ustunlar va qatorlar ichiga joylashtirilgan grid elementlaridan iborat.

## Grid-template-columns xususiyati

`grid-template-columns` xususiyati grid layoutidagi ustunlar sonini belgilaydi va u har bir ustunning kengligini berishi mumkin.

Uning qiymati bo'sh joy bilan ajratilgan ro'yxat shaklida bo'lib, har bir qiymat tegishli ustunning kengligini belgilaydi.

Agar grid layouti 4 ta ustundan iborat bo'lishini istasangiz, 4 ta ustunning kengligini belgilang yoki barcha ustunlar bir xil kenglikda bo'lishi kerak bo'lsa, barchasiga "auto" qiymatini bering.

{% code title="4 ta ustunli grid yaratish:" %}
```
.grid-container {
  display: grid;
  grid-template-columns: auto auto auto auto;
}
```
{% endcode %}

{% hint style="warning" %}
**Eslatma**: Agar 4 ta ustunli gridda 4 tadan ko'p element boʻlsa, grid elementlarni joylashtirish uchun avtomatik tarzda yangi qator qoʻshadi.
{% endhint %}

`grid-template-columns` xususiyatidan ustunlar o'lchamini (kengligini) belgilash uchun ham foydalanish mumkin.

{% code title="4 ta ustun uchun o'lcham berish:" %}
```
.grid-container {
  display: grid;
  grid-template-columns: 80px 200px auto 40px;
}
```
{% endcode %}

### grid-template-rows xususiyati

`grid-template-rows` xususiyati har bir qatorning balandligini belgilaydi.

<figure><img src="../../.gitbook/assets/image (387).png" alt=""><figcaption></figcaption></figure>

Uning qiymati bo'sh joy bilan ajratilgan ro'yxat shaklida bo'lib, undagi har bir qiymat tegishli qatorning balandligini belgilaydi:

```
.grid-container {
  display: grid;
  grid-template-rows: 80px 200px;
}
```

### justify-content xususiyati

`justify-content` xususiyati konteyner ichidagi butun gridni biror tomonga to'g'irlash uchun ishlatiladi.

<figure><img src="../../.gitbook/assets/image (739).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Eslatma**:`justify-content` xususiyati ishlashi uchun gridning umumiy kengligi konteyner kengligidan kichkina bo'lishi kerak.
{% endhint %}

```
.grid-container {
  display: grid;
  justify-content: space-evenly;
}
```

```
.grid-container {
  display: grid;
  justify-content: space-around;
}
```

```
.grid-container {
  display: grid;
  justify-content: space-between;
}
```

```
.grid-container {
  display: grid;
  justify-content: center;
}
```

```
.grid-container {
  display: grid;
  justify-content: start;
}
```

```
.grid-container {
  display: grid;
  justify-content: end;
}
```

### align-content xususiyati

`align-content` xususiyati konteyner ichidagi butun gridni _vertikal tarzda_ biror tomonga to'g'irlash uchun ishlatiladi.

<figure><img src="../../.gitbook/assets/image (406).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Eslatma**:`align-content` xususiyati ishlashi uchun gridning umumiy balandligi konteyner balandligidan kichkina bo'lishi kerak.
{% endhint %}

```
.grid-container {
  display: grid;
  height: 400px;
  align-content: center;
}
```

```
.grid-container {
  display: grid;
  height: 400px;
  align-content: space-evenly;
}
```

```
.grid-container {
  display: grid;
  height: 400px;
  align-content: space-around;
}
```

```
.grid-container {
  display: grid;
  height: 400px;
  align-content: space-between;
}
```

```
.grid-container {
  display: grid;
  height: 400px;
  align-content: start;
}
```

```
.grid-container {
  display: grid;
  height: 400px;
  align-content: end;
}
```
