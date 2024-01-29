# React Render HTML

Reactning maqsadi HTMLni turli xil yo'llar bilan sahifada ko'rsatishdir.

React HTML-ni veb-sahifaga `createRoot()` nomli funksiya va uning `render()` metodi yordamida ko'rsatadi.

### CreateRoot funksiyasi

`createRoot()` funksiyasi bitta argument sifatida HTML elementini qabul qiladi oladi.

Bu funksiyaning maqsadi React komponenti ko'rsatilishi kerak bo'lgan HTML elementni ifodalashdir.

### Render metodi

Keyin `render()` metodi ko'rsatilishi kerak bo'lgan React komponentini yaratish uchun chaqiriladi.

Lekin qayerda ko'rsatiladi ?

React loyihangizning asosiy katalogida “**public**” nomli boshqa bir papka mavjud. Ushbu papkada `index.html` fayli bor.

Ushbu faylning body qismida bitta \<div> ni ko'rasiz. Bu yerda bizning React ilovamiz ko'rsatiladi.

{% code title=""root" identifikatori bilan element ichidagi paragrafni ko'rsatish:" %}
```jsx
const container = document.getElementById('root');
const root = ReactDOM.createRoot(container);
root.render(<p>Hello</p>);
```
{% endcode %}

Natija `<div id="root">` elementida ko'rsatiladi:

```html
<body>
  <div id="root"></div>
</body>
```

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_render1" %}

{% hint style="warning" %}
E'tibor bering, element identifikatori "root" deb nomlanishi shart emas, lekin bu standart konventsiya.
{% endhint %}

### HTML kodi

Ushbu qo'llanmadagi HTML kod JSX-dan foydalanadi, bu JavaScript kodiga HTML teglarini yozish imkonini beradi:

Bunday sintaksis siz uchun notanish bo'lsa, tashvishlanmang, keyingi bo'limda JSX haqida ko'proq bilib olasiz.

{% code title="HTML kodni o'z ichiga olgan o'zgaruvchi yaratish va uni "root" node-ida ko'rsatish:" %}
```jsx
const myelement = (
  <table>
    <tr>
      <th>Name</th>
    </tr>
    <tr>
      <td>John</td>
    </tr>
    <tr>
      <td>Elsa</td>
    </tr>
  </table>
);

const container = document.getElementById('root');
const root = ReactDOM.createRoot(container);
root.render(myelement);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_render2" %}

### Root node

Root node - natija ko'rsatiladigan HTML elementi hisoblanadi.

_Bu React tomonidan boshqariladigan kontent uchun konteynerga_ o'xshaydi.

U element bo'lishi shart emas va unda `<div>` hamda `id='root'`ham bo'lishi shart emas:&#x20;

Root node-ini xohlagancha chaqirish mumkin:

```html
<body>

  <header id="sandy"></header>

</body>
```

{% code title="Natijani <header id="sandy"> elementida ko'rsatish:" %}
```jsx
const container = document.getElementById('sandy');
const root = ReactDOM.createRoot(container);
root.render(<p>Hallo</p>);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_render3" %}
