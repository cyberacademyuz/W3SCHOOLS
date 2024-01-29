# ES6 Ternary operatorlar

### Renary operatorlar

Ternary operatori `if`/`else` ning soddaroq ko'rinishdagi shartli operatordir.

Sintaksis: `condition ? <expression if true> : <expression if false>`

Mana bu `if`/`else` orqali tuzilgan misol:

{% code title="Oldin:" %}
```jsx
if (authenticated) {
  renderApp();
} else {
  renderLogin();
}
```
{% endcode %}

Bu esa, ternary operatori yordamida tuzilgan misol:

{% code title="Ternary yordamida:" %}
```jsx
authenticated ? renderApp() : renderLogin();
```
{% endcode %}
