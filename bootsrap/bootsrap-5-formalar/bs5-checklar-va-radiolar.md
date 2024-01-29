# BS5 Checklar va Radiolar

### Checkboxlar

Agar foydalanuvchi berib qo'yilgan variantlar ro'yxatidan istalgancha variant tanlashi kerak bo'lsa, checkboxlardan foydalaniladi.

![](<../../.gitbook/assets/image (707).png>)

```
<div class="form-check">
  <input class="form-check-input" type="checkbox" id="check1" name="option1" value="something" checked>
  <label class="form-check-label">Option 1</label>
</div>
```

**Misolni tushuntirish**

Checkboxlarga still berish, labellar va checkboxlarni to'g'ri margin bilan ta'minlash uchun `class="form-check"`  classiga ega o'rab turuvchi elementdan foydalaning.

Keyin, `.form-check-label` classini label elementlariga qo'shing va `.form-check` konteyneri ichidagi checkboxlarga to'g'ri still berish uchun `.form-check-input` classini qo'shing.

Ma'lum bir checkboxni standart tarzda tanlangan qilib qo'yish uchun `checked` atributidan foydalaning.

### Radio tugmalari

Agar foydalanuvchi berib qo'yilgan variantlar ro'yxatidan faqat bittasini tanlashi kerak bo'lsa, radio-lardan foydalaniladi.

![](<../../.gitbook/assets/image (672).png>)

```
<div class="form-check">
  <input type="radio" class="form-check-input" id="radio1" name="optradio" value="option1" checked>Option 1
  <label class="form-check-label" for="radio1"></label>
</div>
<div class="form-check">
  <input type="radio" class="form-check-input" id="radio2" name="optradio" value="option2">Option 2
  <label class="form-check-label" for="radio2"></label>
</div>
<div class="form-check">
  <input type="radio" class="form-check-input" disabled>Option 3
  <label class="form-check-label"></label>
</div>
```

### Kalitlarni almashtirish

Agar checkboxni toggle tugmasi sifatida tuzish kerak bo'lsa, `.form-switch` classiini `.form-check` konteyneri bilan birga foydalaning:

![](<../../.gitbook/assets/image (553).png>)

```
<div class="form-check form-switch">
  <input class="form-check-input" type="checkbox" id="mySwitch" name="darkmode" value="yes" checked>
  <label class="form-check-label" for="mySwitch">Dark Mode</label>
</div>
```
