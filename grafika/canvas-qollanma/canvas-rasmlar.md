# Canvas Rasmlar

### Kanvas - Rasmlar

Tuvalga rasm chizish uchun quyidagi usuldan foydalaning:

* drawImage ( _rasm, x, y_ )

#### Misol

![Qichqiriq](https://www.w3schools.com/graphics/pic\_the\_scream.jpg)

JavaScript:

window.onload = function() {\
&#x20; var canvas = document.getElementById("myCanvas");\
&#x20; var ctx = canvas.getContext("2d");\
&#x20; var img = document.getElementById("scream");\
&#x20; ctx.drawImage(img, 10, 10);\
};
