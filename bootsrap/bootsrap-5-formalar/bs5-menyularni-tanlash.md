# BS5 Menyularni tanlash

### Menyu ni tanlang

Menyuni tanlang:

<figure><img src="../../.gitbook/assets/image (719).png" alt=""><figcaption></figcaption></figure>

Bir nechta elementli tanlash menyusi (menyudan bir nechta elementlarni tanlash uchun **ctrl** yoki **shift** tugmachasini bosib turgan holda tanlang (yoki sichqoncha bilan elementni tanlab, uni bosib tugan holda tepaga yoki pastga harakatlantiring):

<figure><img src="../../.gitbook/assets/image (689).png" alt=""><figcaption></figcaption></figure>

Agar foydalanuvchiga bir nechta variantlardan birini tanlashga ruxsat bermoqchi bo'lsangiz, tanlash menyularidan foydalaning.

Bootstrap 5 da tanlash menyusuni tuzish uchun `<select>` elementiga `.form-select` classini qo'shing:

```
<select class="form-select">
  <option>1</option>
  <option>2</option>
  <option>3</option>
  <option>4</option>
</select>
```

### Menyu o'lchami

<figure><img src="../../.gitbook/assets/image (681).png" alt=""><figcaption></figcaption></figure>

Menyu o'lchamini o'zgartirish uchun `.form-select-lg` yoki `.form-select-sm` classidan foydalaning:

```
<select class="form-select form-select-lg">
<select class="form-select">
<select class="form-select form-select-sm">
```

### Disabled tanlash menyusi

<figure><img src="../../.gitbook/assets/image (552).png" alt=""><figcaption></figcaption></figure>

Tanlash menyusini o'chirib qo'yish uchun `disabled` atributidan foydalaning:

```
<select class="form-select" disabled>
  <option>1</option>
  <option>2</option>
  <option>3</option>
  <option>4</option>
</select>
```

### Ma'lumotlar ro'yxati

Bootstrap shuningdek, `<input>` elementi uchun oldindan belgilangan varyantlar roʻyxati boʻlgan maʼlumotlar roʻyxatini ham tuzadi:

Ro'yxatdan brauzeringizni tanlang:&#x20;

<figure><img src="../../.gitbook/assets/image (665).png" alt=""><figcaption></figcaption></figure>

```
<label for="browser" class="form-label">Choose your browser from the list:</label>
<input class="form-control" list="browsers" name="browser" id="browser">
<datalist id="browsers">
  <option value="Edge">
  <option value="Firefox">
  <option value="Chrome">
  <option value="Opera">
  <option value="Safari">
</datalist>
```
