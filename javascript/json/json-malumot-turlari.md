# JSON Ma'lumot turlari

### To'g'ri ma'lumotlar turlari

JSON-da qiymatlar quyidagi ma'lumot turlaridan biri bo'lishi kerak:

* string
* raqam
* obyekt (JSON obyekti)
* massiv
* boolean
* _null_

{% hint style="danger" %}
JSON qiymatlari quyidagi ma'lumot turlaridan biri bo'la olmaydi**:**

* funktsiya
* sana
* _undefined_
{% endhint %}

### JSON Stringlar

JSON-dagi stringlar qo'shtirnoq ichida yozilishi kerak.

```
{"name":"John"}
```

### JSON Raqamlar

JSON-dagi raqamlar butun son yoki float bo'lishi kerak.

```
{"age":30}
```

### JSON Obyektlar

JSON-dagi qiymatlar obyekt bo'ladi.

```
{
"employee":{"name":"John", "age":30, "city":"New York"}
}
```

{% hint style="warning" %}
Obyektlar JSON qiymatlari sifatida JSON sintaksisiga rioya qilishlari kerak.
{% endhint %}

### JSON Massivlar

JSON-dagi qiymatlar massiv bo'lishi mumkin.

```
{
"employees":["John", "Anna", "Peter"]
}
```

### JSON Boolean

JSONdagi qiymatlar true/false bo‘lishi mumkin.

```
{"sale":true}
```

### JSON null

JSONdagi qiymatlar null bo'lishi mumkin.

```
{"middlename":null}
```
