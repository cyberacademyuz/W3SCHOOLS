# Paragraflar

Paragraf har doim yangi qatordan boshlanadi va odatda matnning **bloki** bo'ladi.

## HTML Paragraflar

HTMLda `<p>` elementi paragrafni ifodalaydi.

Paragraflar har doim yangi qatordan boshlanadi va  brauzerlar avtomatik tarzda paragrafning tepa va pastki qismiga boʻsh joy (**margin**) qoʻshadi.

```html
<p>Bu paragraf.</p>
<p>Bu boshqa paragraf.</p>
```

### HTML Display

Kod ekranda qanday ko'rsatilishini aniq bila olmaysiz.

Katta yoki kichik ekranlarda va o'lchami o'zgartirilgan ekranlarda natijalar har xil bo'ladi.

HTML dagi kodingizga qo'shimcha bo'sh joylar yoki qo'shimcha qatorlar qo'shish orqali uning ko'rinishini o'zgartira olmaysiz.

Sahifa brauzerda ko'rsatilganida, brauzer avtomatik tarzda qo'shimcha bo'sh joylarni va qatorlarni olib tashlaydi:

```html
<p>
Bu paragraf
bir nechta yangi qatorlarni
o'z ichiga oladi.
Ammo brauzer bunga 
e'tibor qilmaydi.
</p>

<p>
Bu paragraf
bir nechta     bo'sh    joylarni
o'z ichiga      oladi
ammo        brauzer
bunga e'tibor    qilmaydi
</p>
```

## HTML Horizontal rule-lar

`<hr>` tegi HTML sahifada gorizontal uzun chiziq sifatida ko'rsatiladi.

`<hr>` elementi HTML sahifada kontentni ajratib turish uchun foydalaniladi.

```html
<h1>Bu 1-sarlavha </h1>
<p>Bu bir matn.</p>
<hr>
<h2>Bu 2-sarlavha</h2>
<p>Bu boshqa bir matn</p>
<hr>
```

`<hr>` tegi bo'sh teg hisoblanadi, ya'ni unda yopiluvchi teg yo'q.

## HTML Qatorni tugatish

HTMLda `<br>` elementi qatorni tugatishni ifodalaydi.

Agar yangi paragrafdan boshlamasdan qatorni to'xtatish (yangi qatorga o'tish)ni hohlasangiz `<br>` dan foydalaning.

```html
<p>Bu<br>to'htatiluvchi satrli<br>paragraf</p>
```

## She'r muammosi

Ushbu she'r ekranda bitta qatorda ko'rsatiladi:

```html
<p>
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
</p>p
```

## Yechim - HTMLning \<pre> elementi

HTMLdagi `<pre>` elementi formatlangan matnni ifodalaydi.

`<pre>` elementi ichidagi matn, belgilangan turdagi shriftda (odatda [Courier](https://www.dafont.com/theme.php?cat=503\&text=Courier))da ko'rsatiladi va u bo'sh joyni ham yangi qatorlarni ham saqlaydi:

```html
<pre>
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
</pre>
```
