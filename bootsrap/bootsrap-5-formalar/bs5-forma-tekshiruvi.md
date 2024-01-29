# BS5 Forma tekshiruvi

### Formani tasdiqlash

<figure><img src="../../.gitbook/assets/image (442).png" alt=""><figcaption></figcaption></figure>

Foydalanuvchilarga feedbacklar berish uchun turli tekshiruv classlaridan foydalanishingiz mumkin. Formani yuborishdan oldin yoki yuborgandan keyin tekshiruv boʻyicha feedback berish uchun `<form>` elementiga `.was-validated` yoki `.needs-validation` classini qoʻshing. Formada nima yetishmayotganligini ko'rsatish uchun input maydonlarida yashil (to'g'ri) yoki qizil (noto'g'ri) rangli chegara chizig'i bo'ladi. Shuningdek, foydalanuvchiga nima yetishmayotganini yoki formani yuborishdan oldin yana nima qilish kerakligini aytish uchun `.valid-feedback` yoki `.invalid-feedback` classini classini qo‘shishingiz mumkin.

{% code title="Ushbu misolda biz .was-validatedshaklni yuborishdan oldin nima etishmayotganini ko'rsatish uchun foydalanamiz:" %}
```
<form action="/action_page.php" class="was-validated">
  <div class="mb-3 mt-3">
    <label for="uname" class="form-label">Username:</label>
    <input type="text" class="form-control" id="uname" placeholder="Enter username" name="uname" required>
    <div class="valid-feedback">Valid.</div>
    <div class="invalid-feedback">Please fill out this field.</div>
  </div>
  <div class="mb-3">
    <label for="pwd" class="form-label">Password:</label>
    <input type="password" class="form-control" id="pwd" placeholder="Enter password" name="pswd" required>
    <div class="valid-feedback">Valid.</div>
    <div class="invalid-feedback">Please fill out this field.</div>
  </div>
  <div class="form-check mb-3">
    <input class="form-check-input" type="checkbox" id="myCheck" name="remember" required>
    <label class="form-check-label" for="myCheck">I agree on blabla.</label>
    <div class="valid-feedback">Valid.</div>
    <div class="invalid-feedback">Check this checkbox to continue.</div>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
```
{% endcode %}
