# WEB Formalar API

### Cheklovni tekshirish DOM metodlari

| Xususiyat           | Ta'rif                                                            |
| ------------------- | ----------------------------------------------------------------- |
| checkValidity()     | Agar input elementida toʻgʻri maʼlumot kiritilsa, true qaytaradi. |
| setCustomValidity() | Input elementining validationMessage xususiyatini o‘rnatadi.      |

Agar input maydonida noto'g'ri ma'lumot kiritilsa, xabarni ko'rsating:

{% code title="checkValidity() metodi" %}
```
<input id="id1" type="number" min="100" max="300" required>
<button onclick="myFunction()">OK</button>

<p id="demo"></p>

<script>
function myFunction() {
  const inpObj = document.getElementById("id1");
  if (!inpObj.checkValidity()) {
    document.getElementById("demo").innerHTML = inpObj.validationMessage;
  }
}
</script>
```
{% endcode %}

### Cheklovni tekshirish DOM xususiyatlari

| Xususiyat         | Ta'rif                                                                                |
| ----------------- | ------------------------------------------------------------------------------------- |
| validity          | Input elementining to'g'riligi bilan bog'liq boolean xususiyatlarni o'z ichiga oladi. |
| validationMessage | Validatsiya noto'g'ri bo'lsa, brauzer ko'rsatadigan xabarni o'z ichiga oladi.         |
| willValidate      | Input elementi tekshirilishi yoki tekshirilmasligini bildiradi.                       |

### Validatsiya xususiyatlari

Input elementining validatsiya xususiyati ma'lumotlarning to'g'riligi bilan bog'liq bir qator xususiyatlarni o'z ichiga oladi**:**

| Xususiyat       | Ta'rif                                                                                            |
| --------------- | ------------------------------------------------------------------------------------------------- |
| customError     | Agar maxsus validatsiya xabari berilgan boʻlsa, “true” qiymatini oʻrnatish.                       |
| patternMismatch | Agar element qiymati uning pattern atributiga mos kelmasa, true qiymatini o‘rnatish.              |
| rangeOverflow   | Agar element qiymati uning max atributidan katta bo‘lsa, true qiymatini o‘rnatish.                |
| rangeUnderflow  | Agar element qiymati uning min atributidan katta bo‘lsa, true qiymatini o‘rnatish.                |
| stepMismatch    | Agar element qiymati uning step atributi bo‘yicha noto‘g‘ri bo‘lsa, true qiymatini o‘rnatish      |
| tooLong         | Agar element qiymati uning maxLength atributidan oshsa, true qiymatini o‘rnatish.                 |
| typeMismatch    | Agar element qiymati uning type atributi bo‘yicha noto‘g‘ri bo‘lsa, true qiymatini o‘rnatish.     |
| valueMissing    | Agar element (kerakli atributga ega) hech qanday qiymatga ega bo'lmasa, true qiymatini o'rnatish. |
| valid           | Elementning qiymati to'g'ri bo'lsa, true qiymatini o'rnatish.                                     |

### Misollar

Agar input maydonidagi raqam 100 dan katta bo'lsa (inputning  `max` atributi), xabar ko'rsatish:

{% code title=" rangeOverflow xususiyati" %}
```
<input id="id1" type="number" max="100">
<button onclick="myFunction()">OK</button>

<p id="demo"></p>

<script>
function myFunction() {
  let text = "Value OK";
  if (document.getElementById("id1").validity.rangeOverflow) {
    text = "Value too large";
  }
}
</script>
```
{% endcode %}

Agar input maydonidagi raqam 100 dan kichik bo'lsa (inputning `min` atributi), xabar ko'rsatish:

{% code title="rangeUnderflow xususiyati" %}
```
<input id="id1" type="number" min="100">
<button onclick="myFunction()">OK</button>

<p id="demo"></p>

<script>
function myFunction() {
  let text = "Value OK";
  if (document.getElementById("id1").validity.rangeUnderflow) {
    text = "Value too small";
  }
}
</script>
```
{% endcode %}
