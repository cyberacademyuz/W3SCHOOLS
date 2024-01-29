# Radial gradient

### CSS Radial Gradientlar <a href="#css-radial-gradientlar" id="css-radial-gradientlar"></a>

Radial gradient o'rtadan boshlab yaratiladi.

Radial gradient yaratish uchun kamida ikkita rang to'xtash nuqtasini belgilashingiz kerak.

#### Sintaksis <a href="#sintaksisi" id="sintaksisi"></a>

```
background-image: radial-gradient(shape size at position, start-color, ..., last-color);
```

Standart holatda shakl ellips shaklda bo'lib, uning o'lchami o'rtadan boshlanib ohirgi burchakgacha tarqaladi.

#### Radial gradient - Bir xil joylashgan rang to'xtash nuqtalari (standart holatda)

Quyidagi misolda bir xil intervaldagi rang to'xtash joylariga ega radial gradient ko'rsatilgan:

<figure><img src="../../../.gitbook/assets/image (847).png" alt=""><figcaption></figcaption></figure>

```
#grad {
  background-image: radial-gradient(red, yellow, green);
}
```

#### Radial gradient - turl oraliqdagi ranglar&#x20;

Quyidagi misolda turli xil rangdagi to'xtash joylari orqali radial gradient ko'rsatilgan:

<figure><img src="../../../.gitbook/assets/image (273).png" alt=""><figcaption></figcaption></figure>

```
#grad {
  background-image: radial-gradient(red 5%, yellow 15%, green 60%);
}
```

### Shakl berish <a href="#shakl-berish" id="shakl-berish"></a>

Shakl parametri shaklni yaratadi. U circle yoki ellips qiymatlarini qabul qiladi. Standart qiymat ellips hisoblanadi.

Quyidagi misolda aylana shaklidagi radial gradient ko'rsatilgan:

![](<../../../.gitbook/assets/image (842).png>)

```
#grad {
  background-image: radial-gradient(circle, red, yellow, green);
}
```

### Turli o'lcham kalit so'zlaridan foydalanish <a href="#har-xil-razmer-kalit-sozlaridan-foydalanish" id="har-xil-razmer-kalit-sozlaridan-foydalanish"></a>

O'lcham parametri gradientnng o'lchamini belgilaydi. U to'rtta qiymat qabul qiladi:

* closest-side (eng yaqin tomoni)
* farthest-side (eng uzoq tomoni)
* closest-corner (eng yaqin burchak)
* farthest-corner (eng uzoq burchak)

{% code title="Turli oʻlcham kalit soʻzlarga ega radial gradient:" %}
```
#grad1 {
  background-image: radial-gradient(closest-side at 60% 55%, red, yellow, black);
}

#grad2 {
  background-image: radial-gradient(farthest-side at 60% 55%, red, yellow, black);
}
```
{% endcode %}

### Takrorlanuvchi radial gradient <a href="#takrorlanuvchi-radial-gradient" id="takrorlanuvchi-radial-gradient"></a>

repeating-radial-gradient()  radial gradientni takrorlash uchun ishlatiladi:

<figure><img src="../../../.gitbook/assets/image (795).png" alt=""><figcaption></figcaption></figure>

```
#grad {
  background-image: repeating-radial-gradient(red, yellow 10%, green 15%);
}
```
