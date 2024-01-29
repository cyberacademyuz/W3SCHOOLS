# JS Plotly

{% hint style="success" %}
Plotly.js - bu 40 dan ortiq diagramma turlari, 3D diagrammalar, statistik grafiklar va SVG xaritalaridan tashkil topgan diagramma kutubxonasi.
{% endhint %}

### Scatter Plotlari

<figure><img src="../../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi:" %}
```
var xArray = [50,60,70,80,90,100,110,120,130,140,150];
var yArray = [7,8,8,9,9,9,10,11,14,14,15];

// Define Data
var data = [{
  x: xArray,
  y: yArray,
  mode:"markers",
  type:"scatter"
}];

// Define Layout
var layout = {
  xaxis: {range: [40, 160], title: "Square Meters"},
  yaxis: {range: [5, 16], title: "Price in Millions"},
  title: "House Prices vs. Size"
};

Plotly.newPlot("myPlot", data, layout);
```
{% endcode %}

### Chiziqli grafikalar

<figure><img src="../../.gitbook/assets/image (538).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi:" %}
```
var xArray = [50,60,70,80,90,100,110,120,130,140,150];
var yArray = [7,8,8,9,9,9,10,11,14,14,15];

// Define Data
var data = [{
  x: xArray,
  y: yArray,
  mode: "lines",
  type: "scatter"
}];

// Define Layout
var layout = {
  xaxis: {range: [40, 160], title: "Square Meters"},
  yaxis: {range: [5, 16], title: "Price in Millions"},
  title: "House Prices vs Size"
};

// Display using Plotly
Plotly.newPlot("myPlot", data, layout);
```
{% endcode %}

### Chiziqli grafikalar

<figure><img src="../../.gitbook/assets/image (208).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi:" %}
```
var exp = "x + 17";

// Generate values
var xValues = [];
var yValues = [];
for (var x = 0; x <= 10; x += 1) {
  yValues.push(eval(exp));
  xValues.push(x);
}

// Define Data
var data = [{
  x: xValues,
  y: yValues,
  mode: "lines"
}];

// Define Layout
var layout = {title: "y = " + exp};

// Display using Plotly
Plotly.newPlot("myPlot", data, layout);
```
{% endcode %}

### Bir necha qatorli

<figure><img src="../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi:" %}
```
var exp1 = "x";
var exp2 = "1.5*x";
var exp3 = "1.5*x + 7";

// Generate values

var x1Values = [];
var x2Values = [];
var x3Values = [];
var y1Values = [];
var y2Values = [];
var y3Values = [];

for (var x = 0; x <= 10; x += 1) {
  x1Values.push(x);
  x2Values.push(x);
  x3Values.push(x);
  y1Values.push(eval(exp1));
  y2Values.push(eval(exp2));
  y3Values.push(eval(exp3));
}

// Define Data
var data = [
  {x: x1Values, y: y1Values, mode:"lines"},
  {x: x2Values, y: y2Values, mode:"lines"},
  {x: x3Values, y: y3Values, mode:"lines"}
];

// Define Layout
var layout = {title: "[y=" + exp1 + "] [y=" + exp2 + "] [y=" + exp3 + "]"};

// Display using Plotly
Plotly.newPlot("myPlot", data, layout);
```
{% endcode %}

### Chiziqli diagrammalar

<figure><img src="../../.gitbook/assets/image (206).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi:" %}
```
var xArray = ["Italy","France","Spain","USA","Argentina"];
var yArray = [55, 49, 44, 24, 15];

var data = [{
  x: xArray,
  y: yArray,
  type: "bar"  }];
var layout = {title:"World Wide Wine Production"};

Plotly.newPlot("myPlot", data, layout);
```
{% endcode %}

### Gorizontal chiziqli diagrammalar

<figure><img src="../../.gitbook/assets/image (536).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi:" %}
```
var xArray = [55, 49, 44, 24, 15];
var yArray = ["Italy","France","Spain","USA","Argentina"];

var data = [{
  x: xArray,
  y: yArray,
  type: "bar",
  orientation: "h"
}];

var layout = {title:"World Wide Wine Production"};

Plotly.newPlot("myPlot", data, layout);
```
{% endcode %}

### Pirog diagrammalari

<figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

Chiziqlar oʻrniga pirogni koʻrsatish uchun x va y ni teglar va qiymatlarga oʻzgartiring va turini “pirog” ga oʻzgartiring:

```
var data = [{
  labels: xArray,
  values: yArray,
  type: "pie"
}];
```

### Donut diagrammalari

<figure><img src="../../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

Pirog diagrammasining o'rniga donutni diaframmasini ko'rsatish uchun teshik qo'shing:

```
var data = [{
  labels: xArray,
  values: yArray,
  hole: .4,
  type: "pie"
}];
```

### Tenglamalar tuzish

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi:" %}
```
var exp = "Math.sin(x)";

// Generate values
var xValues = [];
var yValues = [];
for (var x = 0; x <= 10; x += 0.1) {
  yValues.push(eval(exp));
  xValues.push(x);
}

// Display using Plotly
var data = [{x:xValues, y:yValues, mode:"lines"}];
var layout = {title: "y = " + exp};
Plotly.newPlot("myPlot", data, layout);
```
{% endcode %}

<figure><img src="../../.gitbook/assets/image (451).png" alt=""><figcaption></figcaption></figure>
