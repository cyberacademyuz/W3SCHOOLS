---
description: >-
  HTML jadvallarining har bir ustunida, qatorida yoki bir nechta
  ustunlar/qatorlarida sarlavhalar bo'lishi mumkin.
---

# Jadval sarlavhalari

<figure><img src="../../../.gitbook/assets/image (336).png" alt=""><figcaption></figcaption></figure>

## Jadval sarlavhalari

Jadval sarlavhalari \<th> elementi bilan bilan yaratiladi. Har bir th elementi jadval katakchasini ifodalaydi.

```
<table>
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
</table> 
```

## Vertikal jadval sarlavhalari

Birinchi ustunni jadval sarlavhasi sifatida ishlatish uchun har bir qatordagi birinchi katakchani \<th> elementi sifatida ifodalang:

```
<table>
  <tr>
    <th>Firstname</th>
    <td>Jill</td>
    <td>Eve</td>
  </tr>
  <tr>
    <th>Lastname</th>
    <td>Smith</td>
    <td>Jackson</td>
  </tr>
  <tr>
    <th>Age</th>
    <td>94</td>
    <td>50</td>
  </tr>
</table>
```

## Jadval sarlavhalarini joylashuvi

Standart tarzda jadval sarlavhalari qalin bo'ladi va markazda joylashadi.

| Ism  | Familya | Yosh |
| ---- | ------- | ---- |
| Jill | Smith   | 50   |
| Eve  | Jackson | 94   |

Jadval sarlavhalarini chapga surish uchun CSSning text-align xususiyatidan foydalaning:

```
th {
  text-align: left;
}
```

## Bir nechta ustunlar uchun sarlavha

Ikki yoki undan ortiq ustundan iborat sarlavhaga ega bo'lishingiz mumkin.

![](<../../../.gitbook/assets/image (204).png>)

Buni amalga oshirish uchun \<th> elementining colspan attributidan foydalaning:

```
<table>
  <tr>
    <th colspan="2">Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
</table>
```

## Jadval bosh sarlavhasi

Siz jadvalga butun jadval uchun sarlavha sifatida xizmat qiluvchi bosh sarlavha ham qo'shishingiz mumkin.

![](<../../../.gitbook/assets/image (59).png>)

Jadvalga bosh sarlavha qo'shish uchun \<caption> elementidan foydalaning.

```
<table style="width:100%">
  <caption>Monthly savings</caption>
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
  <tr>
    <td>February</td>
    <td>$50</td>
  </tr>
</table> 
```

{% hint style="warning" %}
**Eslatma**: \<caption> tegi \<table> tegidan keyin darhol kiritilishi kerak.
{% endhint %}

