# BS5 Range

### Maxsus diapazon

Diapazon menyusini tuzish uchun input elementiga `.form-range` classini va `type="range"` atribut qiymatini qo'shing:

Maxsus diapazon

<figure><img src="../../.gitbook/assets/image (662).png" alt=""><figcaption></figcaption></figure>

standart diapazon: ![](<../../.gitbook/assets/image (669).png>)

```
<label for="customRange" class="form-label">Custom range</label>
<input type="range" class="form-range" id="customRange">
```

### Qadamlar

Standart tarzda, diapazon raqamlari orasidagi interval 1 ga teng. Siz uni `step` atributi yordamida o'zgartirishingiz mumkin:

<figure><img src="../../.gitbook/assets/image (735).png" alt=""><figcaption></figcaption></figure>

```
<input type="range" class="form-range" step="10">
```

### Min va max

Standart tarzda, minimal qiymat 0, maksimal qiymat esa 100. Siz bu `min` yoki `max`atributi yordamida o'zgartirishingiz mumkin:

<figure><img src="../../.gitbook/assets/image (696).png" alt=""><figcaption></figcaption></figure>

```
<input type="range" class="form-range" min="0" max="4">
```
