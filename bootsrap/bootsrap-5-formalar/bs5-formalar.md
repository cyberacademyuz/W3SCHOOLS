# BS5 Formalar

### Stacked forma

`.form-control` classiga ega barcha matnli \<input> va \<textarea> elementlari to'g'ri forma stiliga ega bo'ladi:

<figure><img src="../../.gitbook/assets/image (544).png" alt=""><figcaption></figcaption></figure>

```
<form action="/action_page.php">
  <div class="mb-3 mt-3">
    <label for="email" class="form-label">Email:</label>
    <input type="email" class="form-control" id="email" placeholder="Enter email" name="email">
  </div>
  <div class="mb-3">
    <label for="pwd" class="form-label">Password:</label>
    <input type="password" class="form-control" id="pwd" placeholder="Enter password" name="pswd">
  </div>
  <div class="form-check mb-3">
    <label class="form-check-label">
      <input class="form-check-input" type="checkbox" name="remember"> Remember me
    </label>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

{% hint style="warning" %}
Shuni ham yodda tutingki, biz formaga to'g'ri paddig berilishini ta'minlash uchun har bir label elementiga `.form-label` classini qo'shamiz.

Checkboxlarda har xil belgilash turi mavjud. Ular konteyner elementi atrofida `.form-check` bilan o'ralgan va teglar .form-check-label classiga ega, checkboxlar va radio tugmalari esa `.form-check-input` dan foydalanadi.
{% endhint %}

### Textarea

<figure><img src="../../.gitbook/assets/image (697).png" alt=""><figcaption></figcaption></figure>

```
<label for="comment">Comments:</label>
<textarea class="form-control" rows="5" id="comment" name="text"></textarea>
```

### Forma qatori/Grid (Inline formalar)

<figure><img src="../../.gitbook/assets/image (726).png" alt=""><figcaption></figcaption></figure>

Forma elementlari yonma-yon turishini istasangiz, `.row` va `.col` dan foydalaning:

```
<form>
  <div class="row">
    <div class="col">
      <input type="text" class="form-control" placeholder="Enter email" name="email">
    </div>
    <div class="col">
      <input type="password" class="form-control" placeholder="Enter password" name="pswd">
    </div>
  </div>
</form
```

{% hint style="warning" %}
<mark style="color:green;">Bootstrap Gridlari</mark> bo'limida ustunlar va qatorlar haqida ko'proq bilib olasiz.
{% endhint %}

### Formani o'lchamini boshqarish

<figure><img src="../../.gitbook/assets/image (734).png" alt=""><figcaption></figcaption></figure>

`.form-control`  ning inputlar o'lchamini `.form-control-lg` yoki `.form-control-sm` yordamida o'zgartirishingiz mumkin:

```
<input type="text" class="form-control form-control-lg" placeholder="Large input">
<input type="text" class="form-control" placeholder="Normal input">
<input type="text" class="form-control form-control-sm" placeholder="Small input">
```

### Disabled va Readonly

<figure><img src="../../.gitbook/assets/image (555).png" alt=""><figcaption></figcaption></figure>

Input maydonini o'chirish uchun disabled yoki readonly atributlaridan foydalaning:

```
<input type="text" class="form-control" placeholder="Normal input">
<input type="text" class="form-control" placeholder="Disabled input" disabled>
<input type="text" class="form-control" placeholder="Readonly input" readonly>
```

## Oddiy matn inputlari

<figure><img src="../../.gitbook/assets/image (685).png" alt=""><figcaption></figcaption></figure>

Chegaralarsiz input maydonini yaratish uchun `.form-control-plaintext` classidan foydalaning, lekin margin va paddinni o'zgartirib yubormang:

```
<input type="text" class="form-control-plaintext" placeholder="Plaintext input">
<input type="text" class="form-control" placeholder="Normal input">
```

### Rang tanlagich

![](<../../.gitbook/assets/image (677).png>)

Inputga `type="color"` orqali to'g'ri still berish uchun `.form-control-color` classidan foydalaning:

```
<input type="color" class="form-control form-control-color" value="#CCCCCC">
```
