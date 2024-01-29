# React Classlar

React 16.8 dan oldin Class komponentlari React komponentidagi holat va ishlash jarayonini kuzatishning yagona usuli edi. Funktsiya komponentlari "state-less" deb hisoblangan.

Hooks qo'shilishi bilan funktsiya komponentlari endi Class komponentlari bilan deyarli bir xil. Ularning farqi shunchalik ozki, Reactda hech qachon Class komponentidan foydalanishga hojat qolmaydi.

Funksiya komponentlaridan foydalanish afzal bo'lsada, Class komponentlarini React-dan olib tashlash bo'yicha hozircha rejalar mavjud emas.

Ushbu bo'lim Reactda Class komponentlaridan qanday foydalanish kerakligi haqida umumiy ma'lumot beradi.

{% hint style="danger" %}
Ushbu bo'limni o'tkazib yuboring va uning o'rniga funktsiya komponentlaridan foydalaning.
{% endhint %}

### React komponentlari

Komponentlar mustaqil va qayta ishlatiladigan kod bitlaridir. Ular JavaScript funksiyalari bilan bir xil maqsadda ishlaydi, lekin izolyatsiyada ishlaydi va HTML elementlarini render() funksiyasi orqali qaytaradi.

Komponentlar ikki xil bo'ladi, Class komponentlari va Funksiya komponentlari, bu bo'limda Class komponentlari haqida bilib olasiz.

### Class komponentini yaratish

React komponentini yaratishda komponent nomi katta harf bilan boshlanishi kerak.

Class komponenti `extends React.Component` steytmentini o'z ichiga olishi kerak. Ushbu steytment **React.Component** uchun meros yaratadi va sizning komponentingizga **React.Component**ning funksiyalariga murojaat qilish huquqini beradi.

Komponent ham `render()` metodini talab qiladi, bu metod HTML elementini qaytaradi.

`Car` deb nomlangan Class komponentini yarating:

```jsx
class Car extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  }
}
```

Endi sizning React ilovangizda `<h2>` elementini qaytaradigan Car nomli komponent mavjud.

Ushbu komponentni ilovangizda ishlatish uchun oddiy HTML kabi sintaksisdan foydalaning:`<Car />`

`Car` komponentini "root" elementida ko'rsating:

```jsx
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car />);
```

### Komponent konstruktori

Agar komponentingizda `constructor()` funksiyasi mavjud bo'lsa, komponent ishga tushganda bu funksiya chaqiriladi.

Konstruktor funksiyasi komponentning xususiyatlarini ishga tushiradigan joydir.

React-da komponent xususiyatlari `state` deb nomlangan obyektda saqlanishi kerak.

`state` haqida keyinroq batafsil bilib olasiz.

Konstruktor funktsiyasi,shuningdek ota komponentning konstruktor funktsiyasini bajaradigan `super()` steytmentini qo'shish orqali ota komponentning merosini hurmat qilasiz va komponentingiz asosiy komponentning (React.Component) barcha funksiyalariga murojaat qilish huquqiga ega bo'ladi.

Car komponentida konstruktor funksiyasini yarating va color xususiyatini qo'shing:

```jsx
class Car extends React.Component {
  constructor() {
    super();
    this.state = {color: "red"};
  }
  render() {
    return <h2>I am a Car!</h2>;
  }
}
```

`render()` funksiyasida color xususiyatidan foydalaning:

```jsx
class Car extends React.Component {
  constructor() {
    super();
    this.state = {color: "red"};
  }
  render() {
    return <h2>I am a {this.state.color} Car!</h2>;
  }
}
```

### Taqdimotlar

Komponentlar xususiyatlarni bildiruvchi `props` sifatida uzatilishi mumkin.

Propslar funksiya argumentlariga o'xshaydi va ularni komponentga atribut sifatida yuborasiz.

Keyingi bo'limda `props` haqida ko'proq bilib olasiz .

`Color`ni `Car` komponentiga o'tkazish uchun atributdan foydalaning va uni `render()` funksiyasida ishlating:

```jsx
class Car extends React.Component {
  render() {
    return <h2>I am a {this.props.color} Car!</h2>;
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car color="red"/>);
```

### Konstruktorda props

Agar komponentingiz konstruktor funksiyasiga ega bo'lsa, props har doim konstruktorga, shuningdek, `super()` metodi orqali React.Componentga uzatilishi kerak.

```jsx
class Car extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return <h2>I am a {this.props.model}!</h2>;
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car model="Mustang"/>);
```

### Komponentlardagi komponentlar

Komponentlar ichidagi boshqa komponentlarga murojaat qilishimiz mumkin:

Garage komponenti ichidagi Car komponentidan foydalaning:

```jsx
class Car extends React.Component {
  render() {
    return <h2>I am a Car!</h2>;
  }
}

class Garage extends React.Component {
  render() {
    return (
      <div>
      <h1>Who lives in my Garage?</h1>
      <Car />
      </div>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage />);
```

### Fayllardagi komponentlar

React - bu kodni qayta ishlatish bilan bog'liq va ba'zi komponentlaringizni alohida fayllarga kiritish oqilona bo'lishi mumkin.

Buning uchun `.js` kengaytmali yangi fayl yarating va uning ichiga kodni qo'ying:

E'tibor bering, fayl React ni import qilish bilan boshlanishi kerak (avvalgidek) va u `export default Car;` steytmenti bilan tugashi kerak.

{% code title="Bu yangi fayl, uni Car.js deb nomladik:" %}
```jsx
import React from 'react';

class Car extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  }
}

export default Car;
```
{% endcode %}

`Car` komponentidan foydalanish uchun faylni ilovangizga import qilishingiz kerak.

{% code title="Endi Car.js faylini ilovaga import qilamiz va Car komponentini xuddi shu yerda yaratilgandek ishlatishimiz mumkin." %}
```jsx
import React from 'react';
import ReactDOM from 'react-dom/client';
import Car from './Car.js';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car />);
```
{% endcode %}

### React class komponentining steyti

React Class komponentlari built-in `state` obyektiga ega.

Oldinroq komponentlar konstruktori bo‘limida `state`dan foydalanganimizni sezgan bo‘lishingiz mumkin.

`state` obyekti komponentga tegishli xususiyat qiymatlarini saqlaydigan joy hisoblanadi.

`state` obekti o'zgarganda, komponent qayta render bo'ladi.

### State obyektini yaratish

State obyekti konstruktorda ishga tushiriladi:

{% code title="Konstruktor metodia state obyektini yaratish:" %}
```jsx
class Car extends React.Component {
  constructor(props) {
    super(props);
  this.state = {brand: "Ford"};
  }
  render() {
    return (
      <div>
        <h1>My Car</h1>
      </div>
    );
  }
}
```
{% endcode %}

State obyekti qancha hohlasangiz shuncha xususiyatlarni o'z ichiga olishi mumkin:

{% code title="Komponentingizga kerak bo'lgan barcha xususiyatlarni belgilang:" %}
```jsx
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      brand: "Ford",
      model: "Mustang",
      color: "red",
      year: 1964
    };
  }
  render() {
    return (
      <div>
        <h1>My Car</h1>
      </div>
    );
  }
}
```
{% endcode %}

### `state` obyektidan foydalanish

`this.state.`_`propertyname`_ sintaksisidan foydalanib, komponentning istalgan joyidagi `state` obyektiga murojaat qiling:

`render()` metodidagi `state` obyektiga murojaat qilish:

```jsx
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      brand: "Ford",
      model: "Mustang",
      color: "red",
      year: 1964
    };
  }
  render() {
    return (
      <div>
        <h1>My {this.state.brand}</h1>
        <p>
          It is a {this.state.color}
          {this.state.model}
          from {this.state.year}.
        </p>
      </div>
    );
  }
}
```

### `state` obyektini o'zgartirish

state obyektidagi qiymatni o'zgartirish uchun `this.setState()` metodidan foydalaning.

`state` obyektidagi qiymat o'zgarganda, komponent qayta renderlanadi, ya'ni output yangi qiymat(lar)ga muvofiq o'zgaradi.

{% code title="Color xususiyatini o'zgartiradigan onClick hodisasi bilan tugma qo'shing:" %}
```jsx
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      brand: "Ford",
      model: "Mustang",
      color: "red",
      year: 1964
    };
  }
  changeColor = () => {
    this.setState({color: "blue"});
  }
  render() {
    return (
      <div>
        <h1>My {this.state.brand}</h1>
        <p>
          It is a {this.state.color}
          {this.state.model}
          from {this.state.year}.
        </p>
        <button
          type="button"
          onClick={this.changeColor}
        >Change color</button>
      </div>
    );
  }
}
```
{% endcode %}

{% hint style="warning" %}
State obyektini o'zgartirish uchun har doim `setState()` metodidan foydalaning, u komponent yangilanganligini bilishini ta'minlaydi va `render()` metodini (va barcha boshqa lifecycle metodlarini) chaqiradi.
{% endhint %}

### Komponentlarning lifecycle-i

React-ning har bir komponentida uning uchta asosiy bosqichida kuzatishingiz va boshqarishingiz mumkin bo'lgan lifecycle-i mavjud.

Uch bosqich: **o'rnatish** , **yangilash** va **o'chirish**.

### O'rnatish

O'rnatish DOMga elementlarni joylashtirishni anglatadi.

React-da to'rtta built-in metod mavjud, ular komponentni o'rnatishda shu tartibda chaqiriladi:

1. `constructor()`
2. `getDerivedStateFromProps()`
3. `render()`
4. `componentDidMount()`

`render()` metodi talab qilinadi va har doim chaqiriladi, qolganlari ixtiyoriy va agar ulardan foydalansangiz chaqiriladi.

#### constructor

`constructor()` metodi hamma narsadan oldin, komponent ishga tushirilganida chaqiriladi va bu boshlang'ich `state` va boshqa boshlang'ich qiymatlarni o'rnatish uchun tabiiy joydir.

`constructor()` metodii argument sifatida, `props` bilan chaqiriladi va har doim hamma narsadan oldin `super(props)`ni chaqirishdan boshlashingiz kerak, bu parentni konstruktor metodini ishga tushiradi va komponentga o'zining parentidan ( `React.Component`) metodlarni meros qilib olish imkonini beradi.

`constructor` metod har safar komponent yaratganingizda React tomonidan chaqiriladi:

```jsx
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  render() {
    return (
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Header />);
```

#### getDerivedStateFromProps

`getDerivedStateFromProps()` metodi DOMdagi element(lar)ni renderlashdan avval darhol chaqiriladi.

Bu boshlang'ich `props`ga asoslangan `state` obektini o'rnatish uchun tabiiy joy.

U `state` argumenti sifatida qabul qilinadi va `state`ga o'zgartirishlar kiritilgan obyektni qaytaradi.

Quyidagi misol favoritecolorning "qizil" bo'lishi bilan boshlanadi, ammo `getDerivedStateFromProps()`lmetodi `favcol` atributi asosida `favoritecolor`ni yangilaydi:

{% code title="getDerivedStateFromProps metodi render metodidan oldin chaqiriladi:" %}
```jsx
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  static getDerivedStateFromProps(props, state) {
    return {favoritecolor: props.favcol };
  }
  render() {
    return (
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Header favcol="yellow"/>);
```
{% endcode %}

#### Render

`render()` metodi talab qilinadi va aslida HTMLni DOMga chiqaradigan metod hisoblanadi.

{% code title="render() metodi yordamida oddiy komponent:" %}
```jsx
class Header extends React.Component {
  render() {
    return (
      <h1>This is the content of the Header component</h1>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Header />);
```
{% endcode %}

#### komponentDidMount

Usul `componentDidMount()`komponent ko'rsatilgandan keyin chaqiriladi.

Bu erda komponent allaqachon DOM-ga joylashtirilgan bo'lishini talab qiluvchi bayonotlarni ishga tushirasiz.

Avvaliga mening eng yaxshi ko'rgan rangim qizil, lekin menga bir soniya bering va uning o'rniga u sariq:

```jsx
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  componentDidMount() {
    setTimeout(() => {
      this.setState({favoritecolor: "yellow"})
    }, 1000)
  }
  render() {
    return (
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Header />);
```

### Yangilanmoqda

Hayotiy tsiklning keyingi bosqichi komponent yangilanganda _bo'ladi_ .

`state`Komponent yoki komponent o'zgarganda komponent yangilanadi `props`.

React-da tarkibiy qism yangilanganda ushbu tartibda chaqiriladigan beshta o'rnatilgan usullar mavjud:

1. `getDerivedStateFromProps()`
2. `shouldComponentUpdate()`
3. `render()`
4. `getSnapshotBeforeUpdate()`
5. `componentDidUpdate()`

Usul `render()`talab qilinadi va har doim chaqiriladi, qolganlari ixtiyoriy va agar siz ularni aniqlasangiz chaqiriladi.

#### getDerivedStateFromProps

Shuningdek, yangilanishlarda _usul_ chaqiriladi `getDerivedStateFromProps`. Bu komponent yangilanganda chaqiriladigan birinchi usul.

`state`Bu ob'ektni dastlabki rekvizitlar asosida o'rnatish uchun hali ham tabiiy joy .

Quyidagi misolda sevimli rangni ko‘k rangga o‘zgartiruvchi tugma mavjud, biroq `getDerivedStateFromProps()`favcol atributidagi rang bilan holatni yangilaydigan usul chaqirilgani uchun sevimli rang hali ham sariq rangda ko‘rsatiladi:

Agar komponent yangilansa, `getDerivedStateFromProps()`usul chaqiriladi:

```jsx
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  static getDerivedStateFromProps(props, state) {
    return {favoritecolor: props.favcol };
  }
  changeColor = () => {
    this.setState({favoritecolor: "blue"});
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <button type="button" onClick={this.changeColor}>Change color</button>
      </div>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Header favcol="yellow" />);
```

#### shouldComponentUpdate

Usulda `shouldComponentUpdate()`siz React renderlashda davom etishini yoki davom etmasligini ko'rsatadigan mantiqiy qiymatni qaytarishingiz mumkin.

Standart qiymat `true`.

Quyidagi misol `shouldComponentUpdate()`usul qaytib kelganida nima sodir bo'lishini ko'rsatadi `false`:

Har qanday yangilanishda komponentni ko'rsatishni to'xtating:

```jsx
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  shouldComponentUpdate() {
    return false;
  }
  changeColor = () => {
    this.setState({favoritecolor: "blue"});
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <button type="button" onClick={this.changeColor}>Change color</button>
      </div>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Header />);
```

Yuqoridagi kabi bir xil misol, lekin bu safar `shouldComponentUpdate()`usul o'rniga qaytadi `true`:

```jsx
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  shouldComponentUpdate() {
    return true;
  }
  changeColor = () => {
    this.setState({favoritecolor: "blue"});
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <button type="button" onClick={this.changeColor}>Change color</button>
      </div>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Header />);
```

#### ko'rsatish

Usul `render()`, albatta, komponent yangilanganda chaqiriladi _,_ u HTMLni yangi o'zgarishlar bilan DOMga qayta ko'rsatishi kerak.

Quyidagi misolda sevimli rangni ko'k rangga o'zgartiradigan tugma mavjud:

Komponent holatini o'zgartirish uchun tugmani bosing:

```jsx
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  changeColor = () => {
    this.setState({favoritecolor: "blue"});
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <button type="button" onClick={this.changeColor}>Change color</button>
      </div>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Header />);
```

#### getSnapshotBeforeUpdate

Usulda siz yangilanishdan oldin va undan _oldin_`getSnapshotBeforeUpdate()` kirishingiz mumkin , ya'ni yangilanishdan keyin ham yangilanishdan _oldingi_ qiymatlarni tekshirishingiz mumkin .`propsstate`

Agar `getSnapshotBeforeUpdate()`usul mavjud bo'lsa, siz `componentDidUpdate()`usulni ham kiritishingiz kerak, aks holda siz xatoga yo'l qo'yasiz.

Quyidagi misol murakkab bo'lib tuyulishi mumkin, ammo u faqat shunday qiladi:

Komponent o'rnatilganda _u_ sevimli rang "qizil" bilan ko'rsatiladi.

Komponent _o'rnatilgandan so'ng,_ taymer holatni o'zgartiradi va bir soniyadan so'ng sevimli rang "sariq" bo'ladi.

Ushbu harakat _yangilanish_ bosqichini ishga tushiradi va bu komponentning `getSnapshotBeforeUpdate()`usuli borligi sababli, bu usul bajariladi va bo'sh DIV1 elementiga xabar yozadi.

Keyin `componentDidUpdate()`usul bajariladi va bo'sh DIV2 elementiga xabar yozadi:

Yangilanishdan oldin ob'ekt `getSnapshotBeforeUpdate()`qanday ko'rinishini bilish uchun usuldan foydalaning :`state`

```jsx
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  componentDidMount() {
    setTimeout(() => {
      this.setState({favoritecolor: "yellow"})
    }, 1000)
  }
  getSnapshotBeforeUpdate(prevProps, prevState) {
    document.getElementById("div1").innerHTML =
    "Before the update, the favorite was " + prevState.favoritecolor;
  }
  componentDidUpdate() {
    document.getElementById("div2").innerHTML =
    "The updated favorite is " + this.state.favoritecolor;
  }
  render() {
    return (
      <div>
        <h1>My Favorite Color is {this.state.favoritecolor}</h1>
        <div id="div1"></div>
        <div id="div2"></div>
      </div>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Header />);
```

#### komponentDidUpdate

Usul `componentDidUpdate`komponent DOMda yangilangandan keyin chaqiriladi.

Quyidagi misol murakkab bo'lib tuyulishi mumkin, ammo u faqat shunday qiladi:

Komponent o'rnatilganda _u_ sevimli rang "qizil" bilan ko'rsatiladi.

Komponent _o'rnatilgandan so'ng,_ taymer holatni o'zgartiradi va rang "sariq" bo'ladi.

Ushbu harakat _yangilanish_ bosqichini ishga tushiradi va ushbu komponentda `componentDidUpdate`usul mavjud bo'lganligi sababli, bu usul bajariladi va bo'sh DIV elementiga xabar yozadi:

Usul `componentDidUpdate`DOMda yangilanish ko'rsatilgandan keyin chaqiriladi:

```jsx
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  componentDidMount() {
    setTimeout(() => {
      this.setState({favoritecolor: "yellow"})
    }, 1000)
  }
  componentDidUpdate() {
    document.getElementById("mydiv").innerHTML =
    "The updated favorite is " + this.state.favoritecolor;
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <div id="mydiv"></div>
      </div>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Header />);
```

### Oʻchirish

Hayotiy tsiklning keyingi bosqichi komponent DOM dan o'chirilishi yoki React uni chaqirishni yoqtirganidek _uzilishidir ._

React faqat bitta o'rnatilgan usulga ega bo'lib, komponent o'chirilganda chaqiriladi:

* `componentWillUnmount()`

#### komponentWillUnmount

Usul `componentWillUnmount`komponent DOMdan olib tashlanishi arafasida bo'lganda chaqiriladi.

Sarlavhani o'chirish uchun tugmani bosing:

```jsx
class Container extends React.Component {
  constructor(props) {
    super(props);
    this.state = {show: true};
  }
  delHeader = () => {
    this.setState({show: false});
  }
  render() {
    let myheader;
    if (this.state.show) {
      myheader = <Child />;
    };
    return (
      <div>
      {myheader}
      <button type="button" onClick={this.delHeader}>Delete Header</button>
      </div>
    );
  }
}

class Child extends React.Component {
  componentWillUnmount() {
    alert("The component named Header is about to be unmounted.");
  }
  render() {
    return (
      <h1>Hello World!</h1>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Container />);
```
