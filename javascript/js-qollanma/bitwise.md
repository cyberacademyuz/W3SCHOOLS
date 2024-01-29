# Bitwise

### Bitwise operatorlar

| Operator | Nomi                  | Ta'rif                                                                                                   |
| -------- | --------------------- | -------------------------------------------------------------------------------------------------------- |
| &        | AND                   | Ikkala bit ham 1 bo'lsa, har bir bitni 1 ga o'rnatadi                                                    |
| \|       | OR                    | Sets each bit to 1 if one of two bits is 1                                                               |
| ^        | XOR                   | Sets each bit to 1 if only one of two bits is 1                                                          |
| \~       | NOT                   | Inverts all the bits                                                                                     |
| <<       | Zero fill left shift  | Shifts left by pushing zeros in from the right and let the leftmost bits fall off                        |
| >>       | Signed right shift    | Shifts right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off |
| >>>      | Zero fill right shift | Shifts right by pushing zeros in from the left, and let the rightmost bits fall off                      |

### Misollar

| Amal    | Natija | ... bilan bir xil | Natija |
| ------- | ------ | ----------------- | ------ |
| 5 & 1   | 1      | 0101 & 0001       |  0001  |
| 5 \| 1  | 5      | 0101 \| 0001      |  0101  |
| \~ 5    | 10     |  \~0101           |  1010  |
| 5 << 1  | 10     | 0101 << 1         |  1010  |
| 5 ^ 1   | 4      | 0101 ^ 0001       |  0100  |
| 5 >> 1  | 2      | 0101 >> 1         |  0010  |
| 5 >>> 1 | 2      | 0101 >>> 1        |  0010  |

### JavaScript 32 bitli bitwise operandlardan foydalanadi

JavaScript raqamlarni 64 bitli float raqam sifatida saqlaydi, lekin barcha bit bo'yicha operatsiyalar 32 bitli ikkilik sanoq tizimidagi raqamlarda amalga oshiriladi.

Bitwise amalini bajarishdan oldin, JavaScript raqamlarni 32 bitli signed integer sonlarga aylantiradi.

Bitwise amali bajarilgandan keyin, natija 64 bitli raqam aylantiriladi.

{% hint style="warning" %}
Yuqoridagi misollar 4 bitli unsigned binar raqamlardan foydalanadi. Shu sababli \~ 5 10 ni qaytaradi.

JavaScript 32 bitli signed integerlardan foydalanganligi sababli, u 10 qaytarmaydi. U -6 ni qaytaradi.

000000000000000000000000000000101 (5)

11111111111111111111111111111010 (\~5 = -6)

Berilgan integer eng chapdagi bitni minus belgi sifatida ishlatadi.
{% endhint %}

### Bitwise AND

Bitwise juftligida AND bajarilsa, ikkala bit ham 1 bo'lsa, u 1 ni qaytaradi.

Bitta misol:

| Amal   | Natija |
| ------ | ------ |
| 0 va 0 | 0      |
| 0 va 1 | 0      |
| 1 va 0 | 0      |
| 1 va 1 | 1      |

4 bitliga misol:

| Operatsiya   | Natija |
| ------------ | ------ |
| 1111 va 0000 | 0000   |
| 1111 va 0001 | 0001   |
| 1111 va 0010 | 0010   |
| 1111 va 0100 | 0100   |

### Bitwise OR

Bitwise OR bir juft bitda bajarilganda, bitlardan biri 1 bo'lsa, u 1 ni qaytaradi:

Misol:

| Operatsiya | Natija |
| ---------- | ------ |
| 0 \| 0     | 0      |
| 0 \| 1     | 1      |
| 1 \| 0     | 1      |
| 1 \| 1     | 1      |

4 bitliga misol:

|              | Natija |
| ------------ | ------ |
| 1111 \| 0000 | 1111   |
| 1111 \| 0001 | 1111   |
| 1111 \| 0010 | 1111   |
| 1111 \| 0100 | 1111   |

### JavaScript Bitwise XOR

Bitli XOR bir juft bitda bajarilganda, agar bitlar boshqacha bo'lsa, u 1 ni qaytaradi:

Bitta misol:

| Operatsiya | Natija |
| ---------- | ------ |
| 0 ^ 0      | 0      |
| 0 ^ 1      | 1      |
| 1 ^ 0      | 1      |
| 1 ^ 1      | 0      |

4 bitliga misol:

| Operatsiya  | Natija |
| ----------- | ------ |
| 1111 ^ 0000 | 1111   |
| 1111 ^ 0001 | 1110   |
| 1111 ^ 0010 | 1101   |
| 1111 ^ 0100 | 1011   |

### Bitwise AND (&)

Bitwise AND ikkala bit 1 bo'lsagina 1 qaytaradi:

| O'nlik | Ikkilik                               |
| ------ | ------------------------------------- |
| 5      | 000000000000000000000000000000101     |
| 1      | 000000000000000000000000000000001     |
| 5 va 1 | 000000000000000000000000000000001 (1) |

```
let x = 5 & 1;
```

### JavaScript Bitwise YOKI (|)

Bitwise OR, agar bitlardan biri 1 bo'lsa, 1 qaytaradi:

| O'nlik | Ikkilik                               |
| ------ | ------------------------------------- |
| 5      | 000000000000000000000000000000101     |
| 1      | 000000000000000000000000000000001     |
| 5 \| 1 | 000000000000000000000000000000101 (5) |

```
let x = 5 | 1;
```

### JavaScript Bitwise XOR (^)

Bitwise XOR, agar bitlar boshqacha bo'lsa, 1 ni qaytaradi:

| O'nlik | Ikkilik                               |
| ------ | ------------------------------------- |
| 5      | 000000000000000000000000000000101     |
| 1      | 000000000000000000000000000000001     |
| 5 ^ 1  | 000000000000000000000000000000100 (4) |

```
let x = 5 ^ 1;
```

### Bitwise NOT (\~)

| O'nlik | Ikkilik                               |
| ------ | ------------------------------------- |
| 5      | 000000000000000000000000000000101     |
| \~5    | 11111111111111111111111111111010 (-6) |

```
let x = ~5;
```

### Bitwise Left Shift (<<)

Bu nol to'ldirish chap siljish. Bir yoki bir nechta nol bitlar o'ngdan itariladi va eng chap bitlar tushadi:

| O'nlik | Ikkilik                                |
| ------ | -------------------------------------- |
| 5      | 000000000000000000000000000000101      |
| 5 << 1 | 000000000000000000000000000001010 (10) |

```
let x = 5 << 1;
```

### Bitwise Right Shift(>>)

Bu to'g'ri siljishni saqlaydigan belgi. Eng chap bitning nusxalari chapdan ichkariga suriladi va eng o'ngdagi bitlar tushadi:

| O'nlik  | Ikkilik                               |
| ------- | ------------------------------------- |
| -5      | 11111111111111111111111111111011      |
| -5 >> 1 | 11111111111111111111111111111101 (-3) |

```
let x = -5 >> 1;
```

### JavaScript (nol to'ldirish) o'ngga siljitish (>>>)

Bu nol to'ldirish o'ngga siljish. Bir yoki bir nechta nol bitlar chapdan itariladi va eng o'ngdagi bitlar tushadi:

| O'nlik  | Ikkilik                               |
| ------- | ------------------------------------- |
| 5       | 000000000000000000000000000000101     |
| 5 >>> 1 | 000000000000000000000000000000010 (2) |

```
let x = 5 >>> 1;
```

### Ikkilik raqamlar

Bir birli ikkilik raqamlarni tushunish oson:

| Ikkilik vakillik                  | O'nlik qiymat |
| --------------------------------- | ------------- |
| 000000000000000000000000000000001 | 1             |
| 000000000000000000000000000000010 | 2             |
| 000000000000000000000000000000100 | 4             |
| 000000000000000000000000000001000 | 8             |
| 000000000000000000000000000010000 | 16            |
| 00000000000000000000000000100000  | 32            |
| 00000000000000000000000001000000  | 64            |

Yana bir nechta bitni o'rnatish ikkilik patternlarini ko'rsatadi:

| Ikkilik vakillik                  | O'nlik qiymat       |
| --------------------------------- | ------------------- |
| 000000000000000000000000000000101 | 5 (4 + 1)           |
| 000000000000000000000000000001101 | 13 (8 + 4 + 1)      |
| 000000000000000000000000000101101 | 45 (32 + 8 + 4 + 1) |

JavaScript ikkilik sanoq tizimidagi raqamlari ikkita to'ldiruvchi formatda saqlanadi.

Bu shuni anglatadiki manfiy raqam, raqam + 1 ning Bitwise NOT-i ekanligini anglatadi.

| Ikkilik vakillik                  | O'nlik qiymat |
| --------------------------------- | ------------- |
| 000000000000000000000000000000101 | 5             |
| 11111111111111111111111111111011  | -5            |
| 000000000000000000000000000000110 | 6             |
| 11111111111111111111111111111010  | -6            |
| 00000000000000000000000000101000  | 40            |
| 11111111111111111111111111011000  | -40           |

### O'nlik sanoqni ikkilik sanoqqa aylantirish

```
function dec2bin(dec){
  return (dec >>> 0).toString(2);
}
```

### Ikkilik sanoqli tizimga aylantirish

```
function bin2dec(bin){
  return parseInt(bin, 2).toString(10);
}
```
