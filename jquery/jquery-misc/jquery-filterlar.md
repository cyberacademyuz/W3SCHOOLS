# jQuery Filterlar

jQueryni ishlatgan holda maxsus elementlarni filterlashingiz/qidirishingiz mumkin.

### Jadvallarni filterlash <a href="#jadvallarni-filterlash" id="jadvallarni-filterlash"></a>

Jadvaldagi elementlar uchun katta-kichik harflarsiz qidiruvni amalga oshirish uchun:

Jadvalda ismlar, familiyalar yoki elektron pochta xabarlarini qidirish uchun input maydoniga biror narsani kiriting:

![](<../../.gitbook/assets/image (127).png>)

| Ism  | Familya   | Email               |
| ---- | --------- | ------------------- |
| John | Doe       | john@example.com    |
| Mary | Moe       | mary@mail.com       |
| July | Dooley    | july@greatstuff.com |
| Anja | Ravendale | a\_r@test.com       |

**jQuery:**

```
 <script>
$(document).ready(function(){
  $("#myInput").on("keyup", function() {
    var value = $(this).val().toLowerCase();
    $("#myTable tr").filter(function() {
      $(this).toggle($(this).text().toLowerCase().indexOf(value) > -1)
    });
  });
});
</script> 
```

**Misolni tushuntirish:** Input maydoni qiymatiga mos keladigan matn qiymatlari mavjudligini tekshirish uchun jQuery-dan har bir jadval qatorlari bo'ylab harkatlanish uchun foydalanamiz. `toggle()` metodi qidiruvga mos kelmaydigan qatorni (displey: none) yashiradi. Matnni kichik harfga aylantirish uchun `toLowerCase()` DOM metodidan foydalanamiz, bu esa qidiruv registrini osonlashtiradi (qidiruvda "John", "John" va hatto "JOHN" ga ruxsat beradi).

### Ro'yhatlarni filterlash <a href="#royhatlarni-filterlash" id="royhatlarni-filterlash"></a>

Ro'yhatlardagi elementlar uchun katta-kichik harflarsiz qidiruvni amalga oshirish uchun:

![](<../../.gitbook/assets/image (173).png>)

* Birinchi element
* Ikkinchi element
* Uchinchi element
* To'rtinchi

### Har qanaqa narsani filterlash <a href="#har-qanaqa-narsani-filterlash" id="har-qanaqa-narsani-filterlash"></a>

`<div>` elementi uchun katta-kichik harflarsiz qidiruvni amalga oshirish uchun:

<figure><img src="../../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>
