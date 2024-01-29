---
description: >-
  Foydalanuvchilar veb-sahifaning muayyan qismlariga o'tishlari uchun HTML
  havolalaridan bookmarklar yaratish uchun foydalanish mumkin.
---

# Havola bookmarklari

## HTMLda bookmark yaratish

Agar veb-sahifa juda uzun bo'lsa bookmarklar foyda beradi.

Bookmark yaratish - Birinchi bookmark yarating va unga havol qo'shing

Havola bosilganida, sahifa pastga yoki yuqoriga harakatlanib bookmark joylashgan joyga boradi.

### Misol:

Eng avval, bookmark yaratish uchun `id` attributidan foydalaning:

```
<h2 id="C4">Chapter 4</h2>
```

Keyin, xuddi shu sahifadan bookmarkga o'tuvchi ("4-bo'limga o'tish") havola qo'shing:

{% code title="Misol" %}
```
<a href="#C4">Jump to Chapter 4</a>
```
{% endcode %}

Bundan tashqari, boshqa sahifadagi bookmarkga o'tuvchi havola ham qo'shishingiz mumkin:

```
<a href="html_demo.html#C4">Jump to Chapter 4</a>
```

## Bo'lim xulosasi

* Sahifada bookmark yaratish uchun `id` (id="_qiymat_") atributidan foydalaning.&#x20;
* Boshqa sahifadagi bookmarkga havola yarish uchun `href` (href="#_qiymat_") atributidan foydalaning
