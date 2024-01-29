# Jadval stili

### Jadval Paddingi <a href="#jadval-paddingi" id="jadval-paddingi"></a>

Jadvaldagi kontent va chegara orasidagi bo'sh joyni boshqarish qilish uchun `<th>` va `<td>` elementlariga `padding` xususiyatini qo'shish kerak bo'ladi

<figure><img src="../../../.gitbook/assets/image (501).png" alt=""><figcaption></figcaption></figure>

```
th, td {
  padding: 15px;
  text-align: left;
}
```

### Gorizontal ajratgichlar <a href="#gorizontal-ajratgichlar" id="gorizontal-ajratgichlar"></a>

<figure><img src="../../../.gitbook/assets/image (318).png" alt=""><figcaption></figcaption></figure>

Gorizontal ajratgichlar hosil qilish uchun `border-bottom` xususiyatini qo'shing

```
th, td {
  border-bottom: 1px solid #ddd;
}
```

### Hoverli jadval <a href="#harakatlanuvchi-jadval" id="harakatlanuvchi-jadval"></a>

Sichqonchani kursorini jadval ustida harkatlantirganda jadval qatorlarini ajratib ko'rsatish uchun \<tr>elementida `:hover` selektoridan foydalaning:

<figure><img src="../../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

```
tr:hover {background-color: coral;}
```

### Chiziqli jadvallar <a href="#chiziqli-jadvallar" id="chiziqli-jadvallar"></a>

<figure><img src="../../../.gitbook/assets/image (466).png" alt=""><figcaption></figcaption></figure>

Zebraga o'xshagan jadvallar yaratish uchun `:nth-child()` selektoridan foydalanib ularning har bir juft (yoki toq)larining orqa foniga rang bering.

```
tr:nth-child(even) {background-color: #f2f2f2;}
```

### Jadval rangi <a href="#jadval-rangi" id="jadval-rangi"></a>

Quyidagi misolda qanday qilib  `<th>` elementining orqafoniga va matniga rang berish ko'rsatib berilgan:

<figure><img src="../../../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

```
th {
  background-color: #04AA6D;
  color: white;
}
```
