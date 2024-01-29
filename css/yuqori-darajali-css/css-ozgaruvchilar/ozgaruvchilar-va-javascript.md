# O'zgaruvchilar va javascript

### O'zgaruvchilarni JavaScript orqali o'zgartirish

CSS o'zgaruvchilari DOMga murojaat qilish huquqiga ega, ya'ni ularni JavaScript orqali o'zgartirishingiz mumkin.

Bu yerda oldingi sahifalarda ko'rsatilgan misoldagi `--blue` o'zgaruvchisini ekranda ko'rsatish va o'zgartirish uchun javascript kodidan keltirilgan. Agar JavaScript-ni yaxshi bilmasangiz, xavotir olmang. JavaScript qo'llanmamiz orqali JavaScript haqida batafsil ma'lumot olishingiz mumkin:

```
<script>
// Get the root element
var r = document.querySelector(':root');

// Create a function for getting a variable value
function myFunction_get() {
  // Get the styles (properties and values) for the root
  var rs = getComputedStyle(r);
  // Alert the value of the --blue variable
  alert("The value of --blue is: " + rs.getPropertyValue('--blue'));
}

// Create a function for setting a variable value
function myFunction_set() {
  // Set the value of variable --blue to another value (in this case "lightblue")
  r.style.setProperty('--blue', 'lightblue');
}
</script>
```

### Brauzerning qo'llab-quvvatlashi

Jadvaldagi raqamlar `var()` funksiyani to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

| Funksiya | Chrome | Edge | Firefox | Safari | Opera |
| -------- | ------ | ---- | ------- | ------ | ----- |
| var()    | 49.0   | 15.0 | 31.0    | 9.1    | 36.0  |

### CSS var() funksiyasi

| Xususiyat                                                                                                                               | Ta'rif                              |
| --------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| [var()](https://www-w3schools-com.translate.goog/cssref/func\_var.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Inserts the value of a CSS variable |
