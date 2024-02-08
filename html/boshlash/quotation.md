# Quotation

Ushbu bo'limda HTMLning <mark style="color:red;">`<blockquote>`</mark>, <mark style="color:red;">`<q>`</mark>, <mark style="color:red;">`<abbr>`</mark>, <mark style="color:red;">`<address>`</mark>, <mark style="color:red;">`<cite>`</mark> va <mark style="color:red;">`<bdo>`</mark> elementlarini ko'rib chiqamiz.

## <mark style="color:green;">Iqtiboslar uchun HTMLning</mark> <mark style="color:green;"></mark><mark style="color:green;">`<blockquote>`</mark> <mark style="color:green;"></mark><mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<blockquote>`</mark> elementi boshqa manbadan olingan iqtibosni ifodalaydi.

Brauzerlar odatda <mark style="color:red;">`<blockquote>`</mark> elementlarini cheklashadi.

```html
<p>Here is a quote from WWF's website:</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
For 60 years, WWF has worked to help people and nature thrive. As the world's leading conservation organization, WWF works in nearly 100 countries. At every level, we collaborate with people around the world to develop and deliver innovative solutions that protect communities, wildlife, and the places in which they live.
</blockquote>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_blockquote" %}

## <mark style="color:green;">Qisqa iqtiboslar uchun HTMLdagi</mark> <mark style="color:green;"></mark><mark style="color:green;">`<q>`</mark> <mark style="color:green;"></mark><mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<q>`</mark> tegi qisqa iqtiboslarni ifodalaydi.

Brauzerlar odatda iqtiboslarni qo'shtirnoq ichiga oladi:

```html
<p>WWF's goal is to: <q>Build a future where people live in harmony with nature.</q></p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_q" %}

## <mark style="color:green;">Qisqartmalar uchun HTMLdagi</mark> <mark style="color:green;"></mark><mark style="color:green;">`<abbr>`</mark> <mark style="color:green;"></mark><mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<abbr>`</mark> elementi "**HTML**", "**CSS**", "**MR**", "**Dr**", "**ASAP**", "**ATM**" kabi qisqartmalarni ifodalaydi.

Qisqartmalarni belgilash brauzerlar, tarjima tizimlari va qidiruv tizimlariga foydali ma'lumotlarni berishi mumkin.

**Maslahat**: Sichqonchani element ustida olib borganingizda qisqacha tavsif ko'rsatish uchun <mark style="color:red;">`title`</mark> atributidan foydalaning.&#x20;

```html
<p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_abbr" %}

## <mark style="color:green;">Kontakt ma'lumotlar uchun HTMLdagi \<address> elementi</mark>

HTMLning <mark style="color:red;">`<address>`</mark> tegi hujjat yoki maqolaning muallifi yoki egasining kontakt ma'lumotlari uchun qo'llaniladi.

Kontakt ma'lumotlarida pochta manzil, URL, telefon raqam, ijtimoq tarmoq sahifalari va boshqalar bo'lishi mumkin.

<mark style="color:red;">`<address>`</mark> elementining ichidagi matn odatda _kursiv_ tarzda ko'rsatiladi.

```html
<address>
Written by John Doe.<br>
Visit us at:<br>
Example.com<br>
Box 564, Disneyland<br>
USA
</address>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_address" %}

## <mark style="color:green;">Ijodiy ish nomlari uchun HTMLdagi</mark> <mark style="color:green;"></mark><mark style="color:green;">`<cite>`</mark> <mark style="color:green;"></mark><mark style="color:green;">elementi</mark>

&#x20;HTMLning <mark style="color:red;">`<cite>`</mark> elementi kitob, sher, musiqa, kino, surat va boshqa shu kabi ijodiy ishlarning nomlarini ifodalashda ishladiladi.

**Eslatma:** Biror shaxsning ismi ijodiy ish nomiga kirmaydi

<mark style="color:red;">`<cite>`</mark> elementi ichidagi matn odatda _kursiv_ tarzda ko'rsatiladi.

```html
<p><cite>The Scream</cite> by Edvard Munch. Painted in 1893.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_cite" %}

## <mark style="color:green;">Matnni teskari qilish uchun HTMLning</mark> <mark style="color:green;"></mark><mark style="color:green;">`<bdo>`</mark> <mark style="color:green;"></mark><mark style="color:green;">elementi</mark>

BDO - **Bi-Directional Override** degan ma'noni bildiradi.

HTMLning <mark style="color:red;">`<bdo>`</mark> elementi matnni teskari yozish uchun ishlatiladi.

```html
<bdo dir="rtl">This text will be written from right to left</bdo>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_bdo" %}

## <mark style="color:green;">HTMLning iqtibos elementlari</mark>

| Teg           | Tavsif                                                |
| ------------- | ----------------------------------------------------- |
| \<abbr>       | Qisqartmalarni ifodalaydi                             |
| \<address>    | Maqola muallifining kontakt ma'lumotlarini ifodalaydi |
| \<bdo>        | Matnni teskari ko'rsatishni ifodalaydi                |
| \<blockquote> | Boshqa manbadan olingan iqtibosni ifodalaydi          |
| \<cite>       | Ijodiy ish nomini ifodalaydi                          |
| \<q>          | Qisqa iqtibosni ifodalaydi                            |

