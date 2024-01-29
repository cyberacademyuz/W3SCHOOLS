# JS Chart.js

{% hint style="success" %}
Chart.js HTML-ga asoslangan grafikalarni yaratish uchun bepul kutubxona. Bu JavaScript uchun eng oddiy vizualizatsiya kutubxonalaridan biri hisoblanib, quyidagi built-in diagramma turlarini o'z ichiga oladi:

* Scatter Plot
* Chiziqli diagramma
* Bar diagramma
* Pirog diagrammasi
* Donut diagrammasi
* Bubble diagrammasi
* Maydon diagrammasi
* Radar diagrammasi
* Aralash diagramma
{% endhint %}

### Chart.js dan qanday foydalanish kerak ?

Chart.js-dan foydalanish oson.

Birinchi, Chart.jsni taqdim qiluvchi CDN (Content Delivery Network) havolasini kiriting:

```
<script
src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.9.4/Chart.js">
</script>
```

Keyin, diagramma chizmoqchi bo'lgan joyingizga \<canvas> elementini qo'shing:

```
<canvas id="myChart" style="width:100%;max-width:700px"></canvas>
```

Canvas elementi unikal id-ga ega bo'lishi kerak.

Ana bo'ldi!

**Oddiy Scatter diagrammasining sintaksisi:**

```
const myChart = new Chart("myChart", {
  type: "scatter",
  data: {},
  options: {}
});
```

**Oddiy chiziqli diagramma sintaksisi:**

```
const myChart = new Chart("myChart", {
  type: "line",
  data: {},
  options: {}
});
```

**Oddiy chiziqli diagramma sintaksisi:**

```
const myChart = new Chart("myChart", {
  type: "bar",
  data: {},
  options: {}
});
```

### **Scatter** chizmalari

Uy narxlari vs. size

<figure><img src="../../.gitbook/assets/image (202).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi:" %}
```
const xyValues = [
  {x:50, y:7},
  {x:60, y:8},
  {x:70, y:8},
  {x:80, y:9},
  {x:90, y:9},
  {x:100, y:9},
  {x:110, y:10},
  {x:120, y:11},
  {x:130, y:14},
  {x:140, y:14},
  {x:150, y:15}
];

new Chart("myChart", {
  type: "scatter",
  data: {
    datasets: [{
      pointRadius: 4,
      pointBackgroundColor: "rgba(0,0,255,1)",
      data: xyValues
    }]
  },
  options:{...}
});
```
{% endcode %}

### Chiziqli grafiklar

Uy narxlari vs. size

<figure><img src="../../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi:" %}
```
const xValues = [50,60,70,80,90,100,110,120,130,140,150];
const yValues = [7,8,8,9,9,9,10,11,14,14,15];

new Chart("myChart", {
  type: "line",
  data: {
    labels: xValues,
    datasets: [{
      backgroundColor:"rgba(0,0,255,1.0)",
      borderColor: "rgba(0,0,255,0.1)",
      data: yValues
    }]
  }
  options:{...}
});
```
{% endcode %}

Agar `borderColor` qiymatini 0 qilsangiz, scatter plot grafikasini chizishingiz mumkin:

```
borderColor: "rgba(0,0,0,0)",
```

### Bir necha qatorli grafik

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi:" %}
```
const xValues = [100,200,300,400,500,600,700,800,900,1000];

new Chart("myChart", {
  type: "line",
  data: {
    labels: xValues,
    datasets: [{
      data: [860,1140,1060,1060,1070,1110,1330,2210,7830,2478],
      borderColor: "red",
      fill: false
    },{
      data: [1600,1700,1700,1900,2000,2700,4000,5000,6000,7000],
      borderColor: "green",
      fill: false
    },{
      data: [300,700,2000,5000,6000,4000,2000,1000,200,100],
      borderColor: "blue",
      fill: false
    }]
  },
  options: {
    legend: {display: false}
  }
});
```
{% endcode %}

### Chiziqli grafiklar

<figure><img src="../../.gitbook/assets/image (207).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi:" %}
```
const xValues = [];
const yValues = [];
generateData("x * 2 + 7", 0, 10, 0.5);

new Chart("myChart", {
  type: "line",
  data: {
    labels: xValues,
    datasets: [{
      fill: false,
      pointRadius: 1,
      borderColor: "rgba(255,0,0,0.5)",
      data: yValues
    }]
  },
  options: {...}
});

function generateData(value, i1, i2, step = 1) {
  for (let x = i1; x <= i2; x += step) {
    yValues.push(eval(value));
    xValues.push(x);
  }
}
```
{% endcode %}

### Funksional grafiklar

<figure><img src="../../.gitbook/assets/image (203).png" alt=""><figcaption></figcaption></figure>

{% code title="Chiziqli grafik bilan bir xil. Faqat GenereData parametrlarini o'zgartiring:" %}
```
generateData("Math.sin(x)", 0, 10, 0.5);
```
{% endcode %}

### Chiziqli diagrammalar

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi" %}
```
var xValues = ["Italy", "France", "Spain", "USA", "Argentina"];
var yValues = [55, 49, 44, 24, 15];
var barColors = ["red", "green","blue","orange","brown"];

new Chart("myChart", {
  type: "bar",
  data: {
    labels: xValues,
    datasets: [{
      backgroundColor: barColors,
      data: yValues
    }]
  },
  options: {...}
});
```
{% endcode %}

{% code title="Faqat bitta chiziqga rang bering:" %}
```
var barColors = ["blue"];
```
{% endcode %}

{% code title="Barcha chiziqlar bir xil rangda:" %}
```
var barColors ="red";
```
{% endcode %}

{% code title="Rang soyalari:" %}
```
var barColors = [
  "rgba(0,0,255,1.0)",
  "rgba(0,0,255,0.8)",
  "rgba(0,0,255,0.6)",
  "rgba(0,0,255,0.4)",
  "rgba(0,0,255,0.2)",
];
```
{% endcode %}

#### Gorizontal chiziqlar

{% code title="Faqat turini "bar" dan "gorizontalBar" ga o'zgartiring:" %}
```
type: "horizontalBar",
```
{% endcode %}

### Pirog diagrammalari

<figure><img src="../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

```
new Chart("myChart", {
  type: "pie",
  data: {
    labels: xValues,
    datasets: [{
      backgroundColor: barColors,
      data: yValues
    }]
  },
  options: {
    title: {
      display: true,
      text: "World Wide Wine Production"
    }
  }
});
```

### Donut diagrammalri

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

{% code title="Faqat turini "pirog" dan "donut" ga o'zgartiring:" %}
```
type: "doughnut";
```
{% endcode %}
