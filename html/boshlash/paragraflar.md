---
description: Paragraf har doim yangi qatordan boshlanadi va odatda matnning bloki bo'ladi.
---

# Paragraflar

## <mark style="color:green;">HTML Paragraflar</mark>

HTMLda <mark style="color:red;">`<p>`</mark> elementi paragrafni ifodalaydi.

Paragraflar har doim yangi qatordan boshlanadi va brauzerlar avtomatik tarzda paragrafning tepa va pastki qismiga boʻsh joy (**margin**) qoʻshadi.

{% tabs %}
{% tab title="HTML" %}
```html
<p>Bu paragraf.</p>
<p>Bu boshqa paragraf.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_paragraphs1" %}
{% endtab %}
{% endtabs %}

### <mark style="color:green;">Ekranda ko'rsatilishi</mark>

Kod ekranda qanday ko'rsatilishini aniq bila olmaysiz.

Katta yoki kichik ekranlarda va o'lchami o'zgartirilgan ekranlarda natijalar har xil bo'ladi.

HTML dagi kodingizga qo'shimcha bo'sh joylar yoki qo'shimcha qatorlar qo'shish orqali uning ko'rinishini o'zgartira olmaysiz.

Sahifa brauzerda ko'rsatilganida, brauzer avtomatik tarzda qo'shimcha bo'sh joylarni va qatorlarni olib tashlaydi:

{% tabs %}
{% tab title="HTML" %}
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

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_paragraphs2" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Horizontal rule</mark>

<mark style="color:red;">`<hr>`</mark> tegi HTML sahifada gorizontal uzun chiziq sifatida ko'rsatiladi.

<mark style="color:red;">`<hr>`</mark> elementi HTML sahifada kontentni ajratib turish uchun foydalaniladi.

{% tabs %}
{% tab title="HTML" %}
```html
<h1>Bu 1-sarlavha </h1>
<p>Bu bir matn.</p>
<hr>
<h2>Bu 2-sarlavha</h2>
<p>Bu boshqa bir matn</p>
<hr>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_headings_hr" %}
{% endtab %}
{% endtabs %}

<mark style="color:red;">`<hr>`</mark> tegi bo'sh teg hisoblanadi, ya'ni unda yopiluvchi teg yo'q.

## <mark style="color:green;">HTML Qatorni tugatish</mark>

HTMLda <mark style="color:red;">`<br>`</mark> elementi qatorni tugatishni ifodalaydi.

Agar yangi paragrafdan boshlamasdan qatorni to'xtatish (yangi qatorga o'tish)ni hohlasangiz <mark style="color:red;">`<br>`</mark> dan foydalaning.

{% tabs %}
{% tab title="HTML" %}
```html
<p>Bu<br>to'htatiluvchi satrli<br>paragraf</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_paragraphs" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">She'r muammosi</mark>

Ushbu she'r ekranda bitta qatorda ko'rsatiladi:

{% tabs %}
{% tab title="HTML" %}
```html
<p>
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_poem" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Yechim - HTMLning \<pre> elementi</mark>

HTMLdagi <mark style="color:red;">`<pre>`</mark> elementi formatlangan matnni ifodalaydi.

<mark style="color:red;">`<pre>`</mark> elementi ichidagi matn, belgilangan turdagi shriftda (odatda [Courier](https://www.dafont.com/theme.php?cat=503\&text=Courier))da ko'rsatiladi va u bo'sh joyni ham yangi qatorlarni ham saqlaydi:

{% tabs %}
{% tab title="HTML" %}
```html
<pre>
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
</pre>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_pre" %}
{% endtab %}
{% endtabs %}
