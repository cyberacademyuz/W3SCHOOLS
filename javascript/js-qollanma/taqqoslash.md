# Taqqoslash

Taqqoslash va Boolean operatorlari `true` yoki `false`ni tekshirish uchun ishlatiladi.

### Taqqoslash operatorlari

Taqqoslash operatorlari mantiqiy steytmentlarda o'zgaruvchilar yoki qiymatlar orasidagi tenglik yoki farqni aniqlash uchun ishlatiladi.

Quyidagi jadvalda berilgan `x = 5` misolida taqqoslash operatorlari tushuntiriladi:

| Operator | Ta'rif                                | Taqqoslash                             | Qaytuvchi javob              |
| -------- | ------------------------------------- | -------------------------------------- | ---------------------------- |
| ==       | ga teng                               | <p>x == 8<br>x == 5<br>x == "5"</p>    | <p>false<br>true<br>true</p> |
| ===      | qiymati ham qiymat turi ham teng      | <p>x === 5<br>x === "5"</p>            | <p>true<br>false</p>         |
| !=       | teng emas                             | x != 8                                 | true                         |
| !==      | qiymati ham qiymat turi ham teng emas | <p>x !== 5<br>x !== "5"<br>x !== 8</p> | <p>false<br>true<br>true</p> |
| >        | dan katta                             | x > 8                                  | false                        |
| <        | dan kichik                            | x < 8                                  | true                         |
| >=       | dan katta yoki ..ga teng              | x >= 8                                 | false                        |
| <=       | dan kichik yoki ..ga teng             | x <= 8                                 | true                         |

### Qanday foydalanish mumkin

Taqqoslash operatorlari qiymatlarni solishtirish va natijaga qarab harakat qilish uchun shartli ifodalarda ishlatilishi mumkin:

```
if (age < 18) text = "Too young to buy alcohol";
```

Siz ushbu qo'llanmaning keyingi bo'limida shartli ifodlardan foydalanish haqida ko'proq bilib olasiz.

### Mantiqiy operatorlar

Mantiqiy operatorlar o'zgaruvchilar yoki qiymatlar orasidagi mantiqni aniqlash uchun ishlatiladi.

Quyidagi jadvalda berilgan  `x = 6` va `y = 3` misolida mantiqiy operatorlar tushuntirilgan:

| Operator | Ta'rif | Misol                         |
| -------- | ------ | ----------------------------- |
| &&       | va     | (x < 10 && y > 1) is true     |
| \|\|     | yoki   | (x == 5 \|\| y == 5) is false |
| !        | emas   | !(x == y) is true             |

### Shartli (ternary) operator

JavaScript b a'zi bir shartlar asosida o'zgaruvchiga qiymat beradigan shartli operatorni o'z ichiga oladi.

#### Sintaksis

```
variablename = (condition) ? value1:value2 
```

```
let voteable = (age < 18) ? "Too young":"Old enough";
```

Agar **age** o'zgaruvchisi 18 yoshdan kichik bo'lsa, **voteable** o'zgaruvchining qiymati "Too young" ga teng bo'ladi, aks holda **voteable** o'zgatuvchisining qiymati "Old enough" bo'ladi.

### Har xil turlarni solishtirish

Har xil turdagi ma'lumotlarni solishtirish kutilmagan natijalar berishi mumkin.

Stringni raqam bilan solishtirganda, JavaScript taqqoslash paytida stringni raqamga aylantiradi. Bo'sh string 0 ga aylanadi. Raqamli bo'lmagan string har doim false bo'lgan `NaN` ga aylanadi.

| Taqqoslash  | Qiymat |
| ----------- | ------ |
| 2 < 12      | true   |
| 2 < "12"    | true   |
| 2 < "John"  | false  |
| 2 > "John"  | false  |
| 2 == "John" | false  |
| "2" < "12"  | false  |
| "2" > "12"  | true   |
| "2" == "12" | false  |

Ikki stringni taqqoslaganda, "2" "12" dan katta bo'ladi, chunki (alifbo tartibida) 1 2 dan kichik.

Natija biz kutgandek to'gri chiqishi uchun o'zgaruvchilarni taqqoslashdan oldin ularni tegishli turga aylantirilishi kerak:

```
age = Number(age);
if (isNaN(age)) {
  voteable = "Input is not a number";
} else {
  voteable = (age < 18) ? "Too young" : "Old enough";
}
```

### Nullish Coalescing operatori (??)

Agar birinchi argument nol (`null`yoki `undefined`) bo'lmasa `??` operatori birinchi argumentni qaytaradi.

Aks holda ikkinchi argumentni qaytaradi.

```
let name = null;
let text = "missing";
let result = name ?? text;
```

Nullish operatori 2020 yil mart oyidan boshlab barcha brauzerlarda qo'llab-quvvatlanadi:

| Chrome    | Edge     | Firefox    | Safari      |          |
| --------- | -------- | ---------- | ----------- | -------- |
| Chrome 80 | Edge 80  | Firefox 72 | Safari 13.1 | Opera 67 |
| Feb 2020  | Feb 2020 | Jan 2020   | Mar 2020    | Mar 2020 |

### Ixtiyoriy zanjir operatori (?.)

Agar obyekt `undefined` yoki `null` bo'lsa `?.` operatori `undefined` qaytaradi.

```
// Create an object:
const car = {type:"Fiat", model:"500", color:"white"};
// Ask for car name:
document.getElementById("demo").innerHTML = car?.name;
```

2020-yil mart oyidan boshlab barcha brauzerlarda ixtiyoriy zanjir operatori qo‘llab-quvvatlanadi:

| Chrome    | Edge     | Firefox    | Safari      |          |
| --------- | -------- | ---------- | ----------- | -------- |
| Chrome 80 | Edge 80  | Firefox 72 | Safari 13.1 | Opera 67 |
| Feb 2020  | Feb 2020 | Jan 2020   | Mar 2020    | Mar 2020 |
