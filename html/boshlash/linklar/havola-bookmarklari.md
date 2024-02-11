---
description: >-
  Foydalanuvchilar veb-sahifaning muayyan qismlariga o'tishlari uchun HTML
  havolalaridan bookmarklar yaratish uchun foydalanish mumkin.
---

# Havola bookmarklari

## <mark style="color:green;">HTMLda bookmark yaratish</mark>

Agar veb-sahifa juda uzun bo'lsa bookmarklar foyda beradi.

Bookmark yaratish - Birinchi bookmark yarating va unga havol qo'shing

Havola bosilganida, sahifa pastga yoki yuqoriga harakatlanib bookmark joylashgan joyga boradi.

### Misol:

Eng avval, bookmark yaratish uchun <mark style="color:red;">`id`</mark> attributidan foydalaning:

```html
<h2 id="C4">Chapter 4</h2>
```

Keyin, xuddi shu sahifadan bookmarkga o'tuvchi ("4-bo'limga o'tish") havola qo'shing:

```html
<a href="#C4">Jump to Chapter 4</a>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_bookmark" %}

Bundan tashqari, boshqa sahifadagi bookmarkga o'tuvchi havola ham qo'shishingiz mumkin:

```html
<a href="html_demo.html#C4">Jump to Chapter 4</a>
```

## <mark style="color:green;">Bo'lim xulosasi</mark>

* Sahifada bookmark yaratish uchun <mark style="color:red;">`id`</mark> (id="_qiymat_") atributidan foydalaning.&#x20;
* Boshqa sahifadagi bookmarkga havola yarish uchun <mark style="color:red;">`href`</mark> (href="#_qiymat_") atributidan foydalaning
