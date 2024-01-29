# Funksiya Apply

### Metodni qayta ishlatish

`apply()` metodi yordamida turli obyektlarda foydalanish mumkin bo'lgan metod yozishingiz mumkin.

### apply() metodi

`apply()` metodi `call()` metodiga o'xshaydi.

Ushbu misolda personning **fullName** metodi **person1** da qo'llaniladi:

```
const person = {
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}

const person1 = {
  firstName: "Mary",
  lastName: "Doe"
}

// This will return "Mary Doe":
person.fullName.apply(person1);
```

### Call() va apply() o'rtasidagi farq

Farqi shundaki:

`call()` metodi argumentlarni **alohida** oladi.

`apply()` metodi argumentlarni **massiv** sifatida oladi.

{% hint style="warning" %}
Agar argumentlar roʻyxati oʻrniga massivdan foydalanmoqchi boʻlsangiz, apply() metodi juda qulay.
{% endhint %}

### apply() metodi bilan argumentlar

`apply()` metodi massivdagi argumentlarni qabul qiladi:

```
const person = {
  fullName: function(city, country) {
    return this.firstName + " " + this.lastName + "," + city + "," + country;
  }
}

const person1 = {
  firstName:"John",
  lastName: "Doe"
}

person.fullName.apply(person1, ["Oslo", "Norway"]);
```

`call()` metodi bilan taqqoslaganda:

```
const person = {
  fullName: function(city, country) {
    return this.firstName + " " + this.lastName + "," + city + "," + country;
  }
}

const person1 = {
  firstName:"John",
  lastName: "Doe"
}

person.fullName.call(person1, "Oslo", "Norway");
```

### Massivlarda Max metodini simulyatsiya qilish

Eng katta sonni `Math.max()` metodi yordamida topishingiz mumkin:

```
Math.max(1,2,3);  // Will return 3
```

**Massivlarda** max() metodi yo'qligi sababli, buning o'rniga `Math.max()`  metodini qo'llashingiz mumkin.

```
Math.max.apply(null, [1,2,3]); // Will also return 3
```

Birinchi argument (null) muhim emas. Bu misolda ishlatilmaydi.

Quyidagi misollar bir xil natija beradi:

```
Math.max.apply(Math, [1,2,3]); // Will also return 3
```

```
Math.max.apply(" ", [1,2,3]); // Will also return 3
```

```
Math.max.apply(0, [1,2,3]); // Will also return 3
```

### Qatiy rejim

Qat'iy rejimda, agar `apply()` metodining birinchi argumenti obyekt bo'lmasa, u chaqirilgan funksiyaning egasi (obyekti) bo'ladi. "Qat'iy bo'lmagan" rejimda u global obyektga aylanadi.
