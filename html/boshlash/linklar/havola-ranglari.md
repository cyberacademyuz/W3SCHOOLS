---
description: >-
  HTML havolalariga o'tilgan, o'tilmagan holatini yoki bosib turilganiga qarab
  boshqa rangda ko'rsatish mumkin.
---

# Havola ranglari

## <mark style="color:green;">HTML Havola ranglari</mark>

Standart tarzda, havolalar barcha brauzerlarda quyidagicha ko'rinadi:

* Kirilmagan havola ranggi ko'k va tagida chizilgan
* Kirilgan havola ranggi binafsha rang va tagida chizilgan
* Havol ustiga bosilganda ranggi qizil va tagida chizilgan

Siz havolaning holat ranglarini CSS dan foydalanib o'zgartirishingiz mumkin.

{% code title="Bu yerda tashrif buyurilmagan  havola yashil rangda bo'ladi, tagiga chizilmaydi. Tashrif buyurilgan havola pushti rangda bo'ladi, tagiga chizilmaydi. Active havola sariq rangda va tagiga chizilgan bo'ladi. Bundan tashqari, sichqonchani havola ustiga olib borganda (a: hover) u qizil rangga aylanadi va tagiga chiziladi:" %}
```html
<style>
a:link {
  color: green;
  background-color: transparent;
  text-decoration: none;
}

a:visited {
  color: pink;
  background-color: transparent;
  text-decoration: none;
}

a:hover {
  color: red;
  background-color: transparent;
  text-decoration: underline;
}

a:active {
  color: yellow;
  background-color: transparent;
  text-decoration: underline;
}
</style>
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_colors" %}

## <mark style="color:green;">Havola tugmalari</mark>

Bundan tashqari havolalarga CSS orqali stil berish orqali tugma ko'rinishiga olib kelish mumkin.

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

</div>

```html
<style>
a:link, a:visited {
  background-color: #f44336;
  color: white;
  padding: 15px 25px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
}

a:hover, a:active {
  background-color: red;
}
</style>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_button" %}

## HTML havola teglari

| Teg  | Tavsif               |
| ---- | -------------------- |
| \<a> | Giperhavola yaratish |
