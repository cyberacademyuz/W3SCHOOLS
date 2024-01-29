# JS Google Chart

{% hint style="success" %}
Oddiy chiziqli diagrammalardan murakkab shajara xaritalarigacha, Google Chart galereyasi foydalanishga tayyor juda ko'p diagramma turlarini taqdim qiladi:

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

### Google Chart-dan qanday foydalanish kerak ?

Veb-sahifangizda Google Chart-dan foydalanish uchun diagrammalar yuklovchining savolasini qo'shing:

```
<script
src="https://www.gstatic.com/charts/loader.js">
</script>
```

Google Chart-dan foydalanish oson.

Grafikni ko'rsatish uchun faqat \<div> elementini qo'shing:

```
<div id="myChart" style="max-width:700px; height:400px"></div>
```

\<div> elementi unikal id-iga ega bo'lishi kerak.

Keyin Google Graph API-ni ulang:

1. Visualization API va asosiy diagramma paketini ulang
2. API yuklanganda chaqirish uchun callback funksiyasini o'rnating

```
1 google.charts.load('current',{packages:['corechart']});

2 google.charts.setOnLoadCallback(drawChart);
```

Ana bo'ldi!

### Chiziqli grafik

<figure><img src="../../.gitbook/assets/image (186).png" alt=""><figcaption></figcaption></figure>

{% code title="" %}
```
function drawChart() {
// Set Data
var data = google.visualization.arrayToDataTable([
  ['Price', 'Size'],
  [50,7],[60,8],[70,8],[80,9],[90,9],[100,9],
  [110,10],[120,11],[130,14],[140,14],[150,15]
  ]);
// Set Options
var options = {
  title: 'House Prices vs Size',
  hAxis: {title: 'Square Meters'},
  vAxis: {title: 'Price in Millions'},
  legend: 'none'
};
// Draw Chart
var chart = new google.visualization.LineChart(document.getElementById('myChart'));
chart.draw(data, options);
}
```
{% endcode %}

### Scatter plot

Xuddi shu ma'lumotlarni scatter plot diagrammasi uchun google.visualization ni ScatterChart ga o'zgartiring:

```
var chart = new google.visualization.ScatterChart(document.getElementById('myChart'));
```

<figure><img src="../../.gitbook/assets/image (598).png" alt=""><figcaption></figcaption></figure>

### Chiziqli diagrammalar

<figure><img src="../../.gitbook/assets/image (620).png" alt=""><figcaption></figcaption></figure>

{% code title="Manba kodi" %}
```
function drawChart() {

var data = google.visualization.arrayToDataTable([
  ['Contry', 'Mhl'],
  ['Italy', 55],
  ['France', 49],
  ['Spain', 44],
  ['USA', 24],
  ['Argentina', 15]
]);

var options = {
  title: 'World Wide Wine Production'
};

var chart = new google.visualization.BarChart(document.getElementById('myChart'));
chart.draw(data, options);
}
```
{% endcode %}

### Pirog diagrammalari

Chiziqli diagrammani dumaloq diagrammaga aylantirish uchun quyidagini:

```
google.visualization. BarChart
```

kodni

```
google.visualization. PieChart
```

bilan alashtiring.

```
var chart = new google.visualization.PieChart(document.getElementById('myChart'));
```

<figure><img src="../../.gitbook/assets/image (602).png" alt=""><figcaption></figcaption></figure>

### 3D pirog

Pirogni 3D formatida ko'rsatish uchun faqat `is3D:true`ni qo'shing:

```
var options = {
  title: 'World Wide Wine Production',
  is3D: true
};
```

<figure><img src="../../.gitbook/assets/image (578).png" alt=""><figcaption></figcaption></figure>
