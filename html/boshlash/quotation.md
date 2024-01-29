# Quotation

Ushbu bo'limda HTMLdagi `<blockquote>`, `<q>`, `<abbr>`, `<address>`, `<cite>` va `<bdo>` elementlarini ko'rib chiqamiz.

## Iqtiboslar uchun HTMLdagi \<blockquote> elementi

HTMLning `<blockquote>` elementi boshqa manbadan olingan iqtibosni ifodalaydi.

Brauzerlar odatda `<blockquote>` elementlarini cheklashadi.

```
<p>Here is a quote from WWF's website:</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
For 60 years, WWF has worked to help people and nature thrive. As the world's leading conservation organization, WWF works in nearly 100 countries. At every level, we collaborate with people around the world to develop and deliver innovative solutions that protect communities, wildlife, and the places in which they live.
</blockquote>
```

## Qisqa iqtiboslar uchun HTMLdagi \<q> elementi

HTMLning `<q>` tegi qisqa iqtiboslarni ifodalaydi.

Brauzerlar odatda iqtiboslarni qo'shtirnoq ichiga oladi:

```
<p>WWF's goal is to: <q>Build a future where people live in harmony with nature.</q></p>
```

## Qisqartmalar uchun HTMLdagi \<abbr> elementi

HTMLning `<abbr>` elementi "HTML", "CSS", "MR", "Dr", "ASAP", "ATM" kabi qisqartmalarni ifodalaydi.

Qisqartmalarni belgilash brauzerlar, tarjima tizimlari va qidiruv tizimlari uchun foydali ma'lumotlarni berishi mumkin.

**Maslahat**: Sichqonchani element ustida olib borganingizda qisqartma tavsifini ko'rsatish uchun `title` atributidan foydalaning.&#x20;

```
<p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
```

## Kontakt ma'lumotlar uchun HTMLdagi \<address> elementi

HTMLning `<address>` tegi hujjat yoki maqolaning muallifi yoki egasining kontakt ma'lumotlari uchun qo'llaniladi.

Kontakt ma'lumotlarida pochta manzili, URL, telefon raqam, ijtimoq tarmoq sahifalari va boshqalar bo'lishi mumkin.

`<address>` elementining ichidagi matn odatda _kursiv_ tarzda ko'rsatiladi.

```
<address>
Written by John Doe.<br>
Visit us at:<br>
Example.com<br>
Box 564, Disneyland<br>
USA
</address>
```

## Ijodiy ish nomlari uchun HTMLdagi \<cite> elementi

&#x20;HTMLning `<cite>` elementi kitob, sher, musiqa, kino, surat va boshqa shu kabi ijodiy ishlarning nomlarini ifodalashda ishladiladi.

**Eslatma:** Biror shaxsning ismi ijodiy ish nomiga kirmaydi

`<cite>` elementi ichidagi matn odatda _kursiv_ tarzda ko'rsatiladi.

```
<p><cite>The Scream</cite> by Edvard Munch. Painted in 1893.</p>
```

## Matnni teskari qilish uchun HTMLning \<bdo> elementi

BDO - **Bi-Directional Override** degan ma'noni bildiradi.

HTMLning `<bdo>` elementi matnni teskari yozish uchun ishlatiladi.

```
<bdo dir="rtl">This text will be written from right to left</bdo>
```

## HTMLning iqtibos elementlari

| Teg           | Tavsif                                                |
| ------------- | ----------------------------------------------------- |
| \<abbr>       | Qisqartmalarni ifodalaydi                             |
| \<address>    | Maqola muallifining kontakt ma'lumotlarini ifodalaydi |
| \<bdo>        | Matnni teskari ko'rsatishni ifodalaydi                |
| \<blockquote> | Boshqa manbadan olingan iqtibosni ifodalaydi          |
| \<cite>       | Ijodiy ish nomini ifodalaydi                          |
| \<q>          | Qisqa iqtibosni ifodalaydi                            |

