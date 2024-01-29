# JSON va XML

JSON ham, XML ham veb-serverdan ma'lumot olish uchun ishlatilishi mumkin.

Quyida keltirilgan JSON va XML ga aloqador misollarning ikkalasi ham massiv orqali 3 ta xodimdan iborat `emplyees` obyektini tuzadi:

{% code title="JSONga misol" %}
```
{"employees":[
  { "firstName":"John", "lastName":"Doe" },
  { "firstName":"Anna", "lastName":"Smith" },
  { "firstName":"Peter", "lastName":"Jones" }
]}
```
{% endcode %}

{% code title="XMLga misol:" %}
```
employees>
  <employee>
    <firstName>John</firstName> <lastName>Doe</lastName>
  </employee>
  <employee>
    <firstName>Anna</firstName> <lastName>Smith</lastName>
  </employee>
  <employee>
    <firstName>Peter</firstName> <lastName>Jones</lastName>
  </employee>
</employees>
```
{% endcode %}

### &#x20;JSON XMLga o'xshaydi, chunki

* JSON ham, XML ham "o'zini tavsiflovchi" (odam tomonidan o'qilishi mumkin)
* JSON ham, XML ham ierarxik hisoblanadi (qiymatlar ichidagi qiymatlar)
* JSON ham, XML ham ko'plab dasturlash tillari tomonidan parse qilinishi va ishlatilishi mumkin
* JSON ham, XML ham `XMLHttpRequest` bilan olinishi mumkin

### JSON XML dan farq qiladi, chunki

* JSON yopiluvchi tegdan foydalanmaydi
* JSON qisqaroq
* JSONda o'qish va yozish tezroq
* JSON massivlardan foydalanishi mumkin

Eng katta farq:

&#x20;XML **XML parser** yordamida parse qilinadi. JSON JavaScriptning standart funksiyasi orqali parse qiladi.

### Nima uchun JSON XML dan yaxshiroq?

{% hint style="warning" %}
XMLni parse qilish JSONga qaraganda ancha qiyin.\
JSON JavaScript obyektlari bilan ishlash uchun moslashgan.
{% endhint %}

AJAX ilovalari uchun JSON XMLga qaraganda tezroq va osonroqdir tuziladi:

XML dan foydalanish

* XML hujjatini oling
* Hujjatni tskil qilish uchun XML DOMdan foydalaning
* Qiymatlarni ajratib oling va o'zgaruvchilarda saqlang

JSON yordamida

* JSON stringini oling
* JSON.Parse orqali JSON stringlarini parse qiling
