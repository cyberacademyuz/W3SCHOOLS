# JS Canvas

{% hint style="success" %}
HTMLning Canvass **Scatter Plotlar**i uchun juda mos keladi

HTMLning Canvasi chiziqli grafikalar uchun ham juda mos keladi

HTML Canvasi **Scatter** va Chiziqlarni birlashtirish uchun ham juda mos keladi
{% endhint %}

### Scatter Plotlari

{% code title="Manba kodi" %}
```
const xArray = [50,60,70,80,90,100,110,120,130,140,150];
const yArray = [7,8,8,9,9,9,10,11,14,14,15];

// Plot Scatter
ctx.fillStyle = "red";
for (let i = 0; i < xArray.length-1; i++) {
  let x = xArray[i]*400/150;
  let y = yArray[i]*400/15;
  ctx.beginPath();
  ctx.ellipse(x, y, 2, 3, 0, 0, Math.PI * 2);
  ctx.fill();
}
```
{% endcode %}

### Chiziqli grafikalar

{% code title="Manba kodi" %}
```
let xMax = canvas.height;
let slope = 1.2;
let intercept = 70;

// Plot Scatter
ctx.moveTo(0, intercept);
ctx.lineTo(xMax, f(xMax));
ctx.strokeStyle = "black";
ctx.stroke();

// Line Function
function f(x) {
  return x * slope + intercept;
}

```
{% endcode %}

### Birlashtirilgan

{% code title="Manba kodi:" %}
```
let xMax = canvas.height;
let yMax = canvas.width;
let slope = 1.2;
let intercept = 70;

const xArray = [50,60,70,80,90,100,110,120,130,140,150];
const yArray = [7,8,8,9,9,9,10,11,14,14,15];

// Plot Scatter
ctx.fillStyle = "red";
for (let i = 0; i < xArray.length-1; i++) {
  let x = xArray[i]*400/150;
  let y = yArray[i]*400/15;
  ctx.beginPath();
  ctx.ellipse(x, y, 2, 3, 0, 0, Math.PI * 2);
  ctx.fill();
}

// Plot Line
ctx.moveTo(0, intercept);
ctx.lineTo(xMax, f(xMax));
ctx.strokeStyle = "black";
ctx.stroke();

// Line Function
function f(x) {
  return x * slope + intercept;
}
```
{% endcode %}
