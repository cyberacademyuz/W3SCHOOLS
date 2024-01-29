# CSS Rasmni aks ettirish

### CSS Rasm refleksiyasi <a href="#css-rasm-refleksiyasi" id="css-rasm-refleksiyasi"></a>

Ushbu bo'limda rasmni qanday aks ettirishni o'rganasiz.

![](../../.gitbook/assets/img\_tree.png)

### CSS Rasm refleksiyalari <a href="#css-rasm-refleksiyalari" id="css-rasm-refleksiyalari"></a>

CSS da rasm refleksiyasini amalga oshirish uchun `box-reflect` xususiyatidan foydalaniladi.

`box-reflect` xususiyatining qiymatlari: `below`, `above`, `left` yoki `right` bo'lishi mumkin.

### Brauzerning qo'llab quvvatlashi <a href="#brauzer-qollab-quvvatlashi" id="brauzer-qollab-quvvatlashi"></a>

Jadvaldagi raqamlar xususiyatni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

Raqamlardan keyingi `-webkit-` prefiksi bilan ishlaydigan birinchi versiya ko'rsatilgan.

| Property    | Chrome       | Edge          | Firefox       | Safari       | Opera         |
| ----------- | ------------ | ------------- | ------------- | ------------ | ------------- |
| box-reflect | 4.0 -webkit- | 79.0 -webkit- | Not supported | 4.0 -webkit- | 15.0 -webkit- |

### Misollar <a href="#misollar" id="misollar"></a>

{% code title="Bu yerda rasm ostida refleksiya yaratishni xohlaymiz:" %}
```
img {
  -webkit-box-reflect: below;
}
```
{% endcode %}

{% code title="Bu yerda biz rasm o'ng tomonida refleksiya yaratishni xohlaymiz:" %}
```
img {
  -webkit-box-reflect: right;
}
```
{% endcode %}

### CSS Aks ettirish offseti <a href="#css-refleksiya-ofseti" id="css-refleksiya-ofseti"></a>

Rasm va aksning orasidagi bo'sh joyni belgilash uchun `box-reflect` xususiyatiga bo'sh joy o'lchamini qo'shing.

{% code title=" Rasm tagidagi rasmning aksi orasida 20px joy ochish:" %}
```
img {
  -webkit-box-reflect: below 20px;
}
```
{% endcode %}

### CSS Gradient bilan aks ettirish <a href="#css-refleksiya-gradient-bilan" id="css-refleksiya-gradient-bilan"></a>

Shuningdek, aks ettirishda kamayashi effektini yaratishimiz mumkin.

{% code title="Rasmning aksiga fade-out effektini berish:" %}
```
img {
  -webkit-box-reflect: below 0px linear-gradient(to bottom, rgba(0,0,0,0.0), rgba(0,0,0,0.4));
}
```
{% endcode %}
