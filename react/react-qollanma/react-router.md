# React Router

Create React App sahifalarni yo'naltirishni o'z ichiga olmaydi.

React Router buni hal qilish uchun eng mashhur yechim hisoblanadi.

### React Routerni qo'shish

Ilovangizga React Routerni qo'shish uchun ushbu buyruqni terminalda ilovaning root katalogida ishga tushiring:

```bash
npm i -D react-router-dom
```

{% hint style="warning" %}
**Eslatma:** Ushbu qo'llanmada React Router v6 dan foydalaniladi.

Agar v5dan v6ga yangilayotgan bo'lsangiz, `@latest` flagidan foydalanishingiz kerak bo'ladi:
{% endhint %}

```bash
npm i -D react-router-dom@latest
```

### Papka strukturasi

Bir nechta sahifali routerlar bilan dastur yaratish uchun avval fayl strukturasidan boshlaylik.

`src` papkasi ichida  bir nechta fayllardan iborat `pages` papkasini yaratamiz:

`src\pages\`:

* `Layout.js`
* `Home.js`
* `Blogs.js`
* `Contact.js`
* `NoPage.js`

Har bir fayl juda oddiy React komponentini o'z ichiga oladi.

### Boshlang'ich foydalanish

Endi `index.js` faylimizda Routerimizdan foydalanamiz.

URL-ga asoslangan sahifalarga yo'naltirish uchun React Router-dan foydalanish:

{% code title=" index.js:" %}
```jsx
import ReactDOM from "react-dom/client";
import { BrowserRouter, Routes, Route } from "react-router-dom";
import Layout from "./pages/Layout";
import Home from "./pages/Home";
import Blogs from "./pages/Blogs";
import Contact from "./pages/Contact";
import NoPage from "./pages/NoPage";

export default function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Layout />}>
          <Route index element={<Home />} />
          <Route path="blogs" element={<Blogs />} />
          <Route path="contact" element={<Contact />} />
          <Route path="*" element={<NoPage />} />
        </Route>
      </Routes>
    </BrowserRouter>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```
{% endcode %}

#### Misolni tushuntirish

Kontentni avval `<BrowserRouter>` bilan o'rab olamiz.

Keyin `<Routes>`mizni tuzamiz. Ilovada bir nechta `<Routes>` bo'lishi mumkin. Bizning sodda misolimizda faqat bitta foydalaniladi.

`<Route>`lar ichma ich bo'lishi mumkin. Birinchisi `<Route>` `/` pathi-ga ega va `Layout` komponentini render qiladi.

Uning ichiga joylashtirilgan `<Route>lar` meros oladi va parent route-ga qo'shiladi. Shu sababli `blogs` joylashuvi parent bilan birlashtiriladi va `/blogs` bo'ladi.

`Home` komponent routeri pathga ega emas, lekin `index` atributiga ega. Bu ushbu routerni ota router uchun standart router sifatida belgilaydi, ya'ni `/`.

`path`ni `*`  qilish har qanday topilmagan URL manzillar uchun hamma narsani qamrab oladi. Bu 404 xato sahifasiga yo'naltirish uchun qo'l keladi.

### Sahifalar / komponentlar

`Layout` komponentida `<Outlet>` va `<Link>` elementlari mavjud.

`<Outlet>` tanlangan joriy route-ni render qiladi.

`<Link>` URL manzilni belgilash va sahifalarga o'tish tarixini kuzatish uchun ishlatiladi.

Har doim ichki joylashuvlarni ulaganimizda, `<a href="">`  o'rniga `<Link>`dan foydalanamiz.

"Layout route" umumiy kontentni barcha sahifalarga, masalan, navigatsiya menyusiga kiritadigan umumiy komponentdir.

{% code title="Layout.js:" %}
```jsx
import { Outlet, Link } from "react-router-dom";

const Layout = () => {
  return (
    <>
      <nav>
        <ul>
          <li>
            <Link to="/">Home</Link>
          </li>
          <li>
            <Link to="/blogs">Blogs</Link>
          </li>
          <li>
            <Link to="/contact">Contact</Link>
          </li>
        </ul>
      </nav>

      <Outlet />
    </>
  )
};

export default Layout;
```
{% endcode %}

{% code title=" Home.js:" %}
```jsx
const Home = () => {
  return <h1>Home</h1>;
};

export default Home;
```
{% endcode %}

{% code title="Blogs.js:" %}
```jsx
const Blogs = () => {
  return <h1>Blog Articles</h1>;
};

export default Blogs;
```
{% endcode %}

{% code title="Contact.js:" %}
```jsx
const Contact = () => {
  return <h1>Contact Me</h1>;
};

export default Contact;
```
{% endcode %}

{% code title="NoPage.js:" %}
```jsx
const NoPage = () => {
  return <h1>404</h1>;
};

export default NoPage;
```
{% endcode %}
