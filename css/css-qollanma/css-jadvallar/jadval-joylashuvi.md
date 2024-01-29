# Jadval joylashuvi

### Gorizontal joylashuv <a href="#gorizontal-joylashuv" id="gorizontal-joylashuv"></a>

`text-align` xususiyati `<th>` yoki `<td>` da kontentning gorizontal joylashuvini (chap, oʻng yoki o'rtaga) o'zgartiradi.

Standart tarzda, `<th>` elementlarning kontentni o'rtaga, `<td>` elementlarning kontenti esa chapga joylashadi.

`<td>` elementlaring kontentini ham o'rtaga joylashtirish uchun `text-align:center` dan foydalaning:

<figure><img src="../../../.gitbook/assets/image (473).png" alt=""><figcaption></figcaption></figure>

```
td {
  text-align: center;
}
```

`<th>` elementidagi kontentni chap tomonga joylashtirish uchun `text-align:left`dan foydalaning:

<figure><img src="../../../.gitbook/assets/image (447).png" alt=""><figcaption></figcaption></figure>

```
th {
  text-align: left;
}
```

### Vertikal joylashuv <a href="#vertikal-joylashuv" id="vertikal-joylashuv"></a>

`vertical-align` xususiyati orqali `<th>` va `<td>` elementlaridagi kontentning vertikal joylashuvini (tepa, past, o'rta) o'zgartirish mumkin.

Standart holatda, jadvalda vertikal joylashuv o'rtada bo'ladi (ikkala `<th>` va `<td>` elementlarida ham)

Quyidagi misol `<td>` elementlari uchun vertikal matnni pastga joylashtiradi:

<figure><img src="../../../.gitbook/assets/image (299).png" alt=""><figcaption></figcaption></figure>

```
td {
  height: 50px;
  vertical-align: bottom;
}
```
