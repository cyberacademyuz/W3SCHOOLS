---
description: >-
  HTML jadvallari bir nechta qator yoki ustunlar o'rnini egallab oluvchi
  kataklarga ega bo'lishi mumkin.
---

# Colspan va Rowspan

<figure><img src="../../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

## HTML jadvali - Colspan

Bir nechta ustunlar o'rnini egallab turuvchi kataklar yaratish uchun `colspan` atributidan foydalaning:

```
<table>
  <tr>
    <th colspan="2">Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>43</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>57</td>
  </tr>
</table> 
```

{% hint style="warning" %}
**Eslatma**: `colspan` atributining qiymati egallanadigan ustunlar sonini bildiradi.
{% endhint %}

## HTML jadval - Rowspan&#x20;

Bir nechta qatorlar o'rnini egallab turuvchi kataklar yaratish uchun `rowspan` atributidan foydalaning:

```
<table>
  <tr>
    <th>Name</th>
    <td>Jill</td>
  </tr>
  <tr>
    <th rowspan="2">Phone</th>
    <td>555-1234</td>
  </tr>
  <tr>
    <td>555-8745</td>
</tr>
</table> 
```

{% hint style="warning" %}
**Eslatma**: `rowspan` atributining qiymati egallanadigan qatorlar sonini bildiradi.
{% endhint %}
