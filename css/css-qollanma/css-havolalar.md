# CSS Havolalar

CSS yordamida linklarga turli yo'llar orqali still berish mumkin.

![](<../../.gitbook/assets/image (524).png>)

### Linklarga stil berish <a href="#linklarga-stil-berish" id="linklarga-stil-berish"></a>

Linklar har qanday CSS xususiyatlari orqali (`color`, `font-family`, `background` va hokazolar) o'zgartirilishi mumkin

```
a {
  color: hotpink;
}
```

Bundan tashqari, linklarning holatiga qarab ham ulrni o'zgartirish mumkin.

Linklarning 4 holati:

* `a:link` - oddiy holat, hali kirilmagan link holatini bildiradi
* `a:visited` - foydalanuvchi tomonidan kirilgan link holatini bildiradi
* `a:hover` - foydalanuvchi sichqocha kursorini link elementining ustiga olib borgandagi hover holati
* `a:active` - link ustiga bosilgandagi holatni bildiradi

```
/* unvisited link */
a:link {
  color: red;
}

/* visited link */
a:visited {
  color: green;
}

/* mouse over link */
a:hover {
  color: hotpink;
}

/* selected link */
a:active {
  color: blue;
}
```

Link holatlariga stil berayotganda quyidagi ba'zi qoidalarga amal qilish kerak:

* `a:hover` - `a:link` va `a:visited` dan keyin kelishi SHART
* `a:active` - `a:hover` dan keyin kelishi SHART

### Text decoration <a href="#matn-dekoratsiyasi" id="matn-dekoratsiyasi"></a>

`text-decoration` xususiyati asosan havola elementining pastki chiziqlarini olib tashlash uchun ishlatiladi.

```
a:link {
  text-decoration: none;
}

a:visited {
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

a:active {
  text-decoration: underline;
}
```

### Fon rangi <a href="#fon-rangi" id="fon-rangi"></a>

`background-color` xususiyati linklarning orqafoniga rang berish uchun ishlatiladi.

```
a:link {
  background-color: yellow;
}

a:visited {
  background-color: cyan;
}

a:hover {
  background-color: lightgreen;
}

a:active {
  background-color: hotpink;
}
```

### Havolali tugmalar <a href="#link-tugmalar" id="link-tugmalar"></a>

Ushbu misolda CSSning bir qancha xususiyatlaridan foydalanib tugma yasash ko'rsatib berilgan:

```
a:link, a:visited {
  background-color: #f44336;
  color: white;
  padding: 14px 25px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
}

a:hover, a:active {
  background-color: red;
}
```

### Ko'proq misollar <a href="#koproq-misollar" id="koproq-misollar"></a>

{% code title="Ushbu misolda giperhavolalarga boshqacha stillarni ham berishshish ko'rsatilgan:" %}
```
a.one:link {color: #ff0000;}
a.one:visited {color: #0000ff;}
a.one:hover {color: #ffcc00;}

a.two:link {color: #ff0000;}
a.two:visited {color: #0000ff;}
a.two:hover {font-size: 150%;}

a.three:link {color: #ff0000;}
a.three:visited {color: #0000ff;}
a.three:hover {background: #66ff66;}

a.four:link {color: #ff0000;}
a.four:visited {color: #0000ff;}
a.four:hover {font-family: monospace;}

a.five:link {color: #ff0000; text-decoration: none;}
a.five:visited {color: #0000ff; text-decoration: none;}
a.five:hover {text-decoration: underline;}
```
{% endcode %}

{% code title="Tugma yaratish bo'yicha yana bir boshqa misol:" %}
```
a:link, a:visited {
  background-color: white;
  color: black;
  border: 2px solid green;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
}

a:hover, a:active {
  background-color: green;
  color: white;
}
```
{% endcode %}

{% code title="Ushbu misolda har xil turdagi kursorlar ko'rsatilgan" %}
```
<span style="cursor: auto">auto</span><br>
<span style="cursor: crosshair">crosshair</span><br>
<span style="cursor: default">default</span><br>
<span style="cursor: e-resize">e-resize</span><br>
<span style="cursor: help">help</span><br>
<span style="cursor: move">move</span><br>
<span style="cursor: n-resize">n-resize</span><br>
<span style="cursor: ne-resize">ne-resize</span><br>
<span style="cursor: nw-resize">nw-resize</span><br>
<span style="cursor: pointer">pointer</span><br>
<span style="cursor: progress">progress</span><br>
<span style="cursor: s-resize">s-resize</span><br>
<span style="cursor: se-resize">se-resize</span><br>
<span style="cursor: sw-resize">sw-resize</span><br>
<span style="cursor: text">text</span><br>
<span style="cursor: w-resize">w-resize</span><br>
<span style="cursor: wait">wait</span>
```
{% endcode %}
