# CSS Flexbox

<figure><img src="../../../.gitbook/assets/image (367).png" alt=""><figcaption></figcaption></figure>

### CSS Flexbox Layout moduli

Flexbox Layout modulidan oldin 4 ta layout rejimi mavjud edi:

* Block - veb-sahifadagi bo'limlar uchun
* Inline - matn uchun
* Jadval - ikki o'lchovli jadval ma'lumotlari uchun
* Joylangan, elementning aniq joylashuvi uchun

Flexible Box Layout moduli float yoki joylashishni aniqlashdan foydalanmasdan moslashuvchan responsive layout strukturasini loyihalashni osonlashtiradi.

### Brauzerning qo'llab-quvvatlashi

Flexbox xususiyatlari barcha zamonaviy brauzerlarda qo'llab-quvvatlanadi.

| Chrome | Edge | Firefox |    |    |
| ------ | ---- | ------- | -- | -- |
| 29.0   | 11.0 | 22.0    | 10 | 48 |

### Flexbox elementlari

Flexbox modelidan foydalanish uchun avval moslashuvchan konteyner yaratishingiz kerak.

<figure><img src="../../../.gitbook/assets/image (408).png" alt=""><figcaption></figcaption></figure>

Yuqoridagi element uchta moslashuvchan elementga ega flex konteynerni (ko'k maydon) ifodalaydi.

{% code title="Uchta moslashuvchan elementga ega moslashuvchan konteyner:" %}
```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```
{% endcode %}

{% hint style="warning" %}
Keyingi bo'limlarda moslashuvchan konteynerlar va moslashuvchan elementlar haqida ko'proq bilib olasiz.
{% endhint %}
