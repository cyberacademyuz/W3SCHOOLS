# CSS Outline

Outline - element chegarasidan tashqarida chizilgan chiziq hisoblanadi.

<figure><img src="../../../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>

### CSS Outline <a href="#css-kontur-2" id="css-kontur-2"></a>

Outline - bu elementni "ajratib turishi" uchun chegara tashqarisida, elementlar atrofida chizilgan chiziq.

<figure><img src="../../../.gitbook/assets/image (468).png" alt=""><figcaption></figcaption></figure>

CSS da outline-ning quyidagi xususiyatlari mavjud:

* outline-style
* outline-color
* outline-width
* outline-offset
* outline

{% hint style="warning" %}
**Note:** Outline birderdan farq qiladi! Outline borderga o'xshamagan holda elementning chegarasidan tashqarida chiziladi. Bundan tashqari outline elementning kengligi va balandligiga ta'sir qilamaydi.
{% endhint %}

### CSS Outline style <a href="#css-kontur-stillari" id="css-kontur-stillari"></a>

`outline-style` orqali outline-ning stilini quyidagi qiymatlar asosida o'zgartira olasiz:

* dotted - nuqtali outline yaratadi
* dashed - chiziqchali outline yaratadi
* solid - oddiy outline yaratadi
* double - ikkitali outline yaratadi
* groove - 3D o'yiqli outline yaratadi
* ridge - 3D qirrali outline yaratadi
* inset - 3D ichkariga qaragan outline yaratadi
* outset - 3D tashqariga qaragan outline yaratadi
* none - hech qanday outline yo'q
* hidden - bekitilgan outline yaratadi

Quyidagi misolda `outline-style` qiymatlarining farqalari ko'rsatilgan:

{% code title="outline stillarining farqlarini ko'rsatib berish:" %}
```
p.dotted {outline-style: dotted;}
p.dashed {outline-style: dashed;}
p.solid {outline-style: solid;}
p.double {outline-style: double;}
p.groove {outline-style: groove;}
p.ridge {outline-style: ridge;}
p.inset {outline-style: inset;}
p.outset {outline-style: outset;}
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (349).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Note:** `outline-style` xususiyatidan foydalanmaguncha `outline` xususiyatlarining hech biri hech qanday tasirga ega bo'lmaydi.
{% endhint %}
