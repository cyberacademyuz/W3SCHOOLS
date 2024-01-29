# BS5 Float labellar

### Floatli labellar / animatsiyali labellar

Labellardan foydalanilganda ular odatda input maydonining tepasida ko'rinadi:

<figure><img src="../../.gitbook/assets/image (193).png" alt=""><figcaption></figcaption></figure>

Floatli labellar orqali labelni input maydonining ichiga yozishingiz va input maydonini bosganingizda uni harakatlantirishingiz mumkin:

<figure><img src="../../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>

```
<div class="form-floating mb-3 mt-3">
  <input type="text" class="form-control" id="email" placeholder="Enter email" name="email">
  <label for="email">Email</label>
</div>

<div class="form-floating mt-3 mb-3">
  <input type="text" class="form-control" id="pwd" placeholder="Enter password" name="pswd">
  <label for="pwd">Password</label>
</div>
```

{% hint style="warning" %}
**Floatli labellar bo'yicha eslatmalar:** `<label>` elementlari `<input>` elementidan keyin kelishi kerak va `placeholder` atributi har bir `<input>` elementi uchun talab qilinadi (hatto u ko'rsatilmagan bo'lsa ham).
{% endhint %}

### Textarea

Bundan tashqari, u textarealar uchun ham ishlaydi:

<figure><img src="../../.gitbook/assets/image (178).png" alt=""><figcaption></figcaption></figure>

```
<div class="form-floating">
  <textarea class="form-control" id="comment" name="text" placeholder="Comment goes here"></textarea>
  <label for="comment">Comments</label>
</div>
```

### Tanlash menyusi

Bundan tashqari, tanlash menyularida ham "floatli labellardan" dan foydalanishingiz mumkin. Biroq, ular harkatlanmaydi. Label har doim yuqori chap burchakda, tanlash menyusining ichida bo'ladi:

<figure><img src="../../.gitbook/assets/image (300).png" alt=""><figcaption></figcaption></figure>

```
<div class="form-floating">
  <select class="form-select" id="sel1" name="sellist">
    <option>1</option>
    <option>2</option>
    <option>3</option>
    <option>4</option>
  </select>
  <label for="sel1" class="form-label">Select list (select one):</label>
</div>
```
