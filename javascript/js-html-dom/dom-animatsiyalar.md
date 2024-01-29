# DOM Animatsiyalar

JavaScript yordamida HTML animatsiyalarini yaratishni o'rganing.

### Boshlang'ich veb-sahifa

JavaScript yordamida HTML animatsiyalarini qanday yaratishni ko'rsatib berish uchun oddiy veb-sahifadan foydalanamiz:

```
<!DOCTYPE html>
<html>
<body>

<h1>My First JavaScript Animation</h1>

<div id="animation">My animation will go here</div>

</body>
</html>
```

### Animatsiya konteynerini yaratish

Barcha animatsiyalar konteyner element ichida bo'lishi kerak.

```
<div id ="container">
  <div id ="animate">My animation will go here</div>
</div>
```

### Elementlarga stil berish

Konteyner elementining cssiga `"position: relative"`  berilishi kerak.

Animatsiya elementining cssiga esa = `"position: absolute"` berish kerak.

```
#container {
  width: 400px;
  height: 400px;
  position: relative;
  background: yellow;
}
#animate {
  width: 50px;
  height: 50px;
  position: absolute;
  background: red;
}
```

### animatsiya kodi

JavaScript animatsiyalari element cssidagi o'zgarishlarni bosqichma-bosqich berish orqali amalga oshiriladi.

O'zgarishlar taymer tomonidan chaqiriladi. Taymer oralig'i kichik bo'lsa, animatsiya chiroyli ko'rinadi.

Asosiy kod:

```
id = setInterval(frame, 5);

function frame() {
  if (/* test for finished */) {
    clearInterval(id);
  } else {
    /* code to change the element style */ 
  }
}
```

### JavaScript yordamida to'liq animatsiya yaratish

```
function myMove() {
  let id = null;
  const elem = document.getElementById("animate");
  let pos = 0;
  clearInterval(id);
  id = setInterval(frame, 5);
  function frame() {
    if (pos == 350) {
      clearInterval(id);
    } else {
      pos++;
      elem.style.top = pos + 'px';
      elem.style.left = pos + 'px';
    }
  }
}
```
