---
description: >-
  HTML havolalariga o'tilgan, o'tilmagan holatini yoki bosib turilganiga qarab
  boshqa rangda ko'rsatish mumkin.
---

# Havola ranglari

## HTML Havola ranglari

Standart tarzda, havolalar barcha brauzerlarda quyidagicha ko'rinadi:

* Kirilmagan havola ranggi ko'k va tagida chizilgan
* Kirilgan havola ranggi binafsha rang va tagida chizilgan
* Havol ustiga bosilganda ranggi qizil va tagida chizilgan

Siz havolaning holat ranglarini CSS dan foydalanib o'zgartirishingiz mumkin.

{% code title="Bu yerda tashrif buyurilmagan  havola yashil rangda bo'ladi, tagiga chizilmaydi. Tashrif buyurilgan havola pushti rangda bo'ladi, tagiga chizilmaydi. Active havola sariq rangda va tagiga chizilgan bo'ladi. Bundan tashqari, sichqonchani havola ustiga olib borganda (a: hover) u qizil rangga aylanadi va tagiga chiziladi:" %}
```
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

## Havola tugmalari

Bundan tashqari havolalarga CSS orqali stil berish orqali tugma ko'rinishiga olib kelish mumkin.

```
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

## HTML havola teglari

| Teg  | Tavsif               |
| ---- | -------------------- |
| \<a> | Giperhavola yaratish |
