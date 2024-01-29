# Sass @extend va meros olish

## Sass `@extend` direktivasi

`@extend` direktivasi CSS xususiyatlari to'plamini bir selektordan boshqasiga almashish imkonini beradi.

`@extend` direktivasi deyarli bir xil stilli elementlarga ega bo'lganingizda foydali bo'ladi, ular faqat ba'zi kichik tafsilotlardagina farqlanadi.

Quyidagi misolda birinchi, tugmalar uchun asosiy stillni yaratiib olamiz (bu still ba'zi tugmalar uchun foydalaniladi). Keyin, "Report" tugmasi uchun yana bir still va "Yuborish" tugmasi uchun boshqa still yaratamiz. "Report" va "Yuborish" tugmalari ham `@extend` direktivasi orqali `.button-basic` classidan barcha CSS xususiyatlarini meros qilib oladi. Bundan tashqari, ularning o'ziga xos ranglari belgilanadi:

```
.button-basic  {
  border: none;
  padding: 15px 30px;
  text-align: center;
  font-size: 16px;
  cursor: pointer;
}

.button-report  {
  @extend .button-basic;
  background-color: red;
}

.button-submit  {
  @extend .button-basic;
  background-color: green;
  color: white;
}
```

Kompilatsiyadan so'ng CSS kod mana bunday ko'rinishda bo'ladi:

```
.button-basic, .button-report, .button-submit {
  border: none;
  padding: 15px 30px;
  text-align: center;
  font-size: 16px;
  cursor: pointer;
}

.button-report  {
  background-color: red;
}

.button-submit  {
  background-color: green;
  color: white;
}
```

`@extend` direktivasidan foydalanib, HTML kodingizdagi element uchun bir nechta classlar belgilashingiz shart emas, masalan: `<button class="button-basic button-report">Report this</button>`. Ikkala stillar to'plamini olish uchun `.button-report` classini berish kifoya.

`@extend` direktivasi Sass kodingizni DRY prinsipida saqlashga yordam beradi.
