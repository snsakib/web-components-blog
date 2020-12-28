# How to create & use an "Customized built-in Custom Element"

Everythins is same as the following document:

{% page-ref page="how-to-create-and-use-a-custom-element.md" %}

The key differences are the following:

* **Don't extend from `HTMLElement` :**

{% tabs %}
{% tab title="index.js" %}
```javascript
class ExpandingList extends HTMLUListElement {

}
```
{% endtab %}
{% endtabs %}

* **Add another parameter while registering the custom element:**

{% tabs %}
{% tab title="index.js" %}
```javascript
customElements.define('expanding-list', ExpandingList, { extends: "ul" });
```
{% endtab %}
{% endtabs %}

* **There are 3 ways to instantiate the custom element:**

{% tabs %}
{% tab title="index.html" %}
```markup
<!-- Method 1: using 'is' -->
<ul is="expanding-list"></ul>
```
{% endtab %}

{% tab title="index.js" %}
```javascript
// Method 2: createElement
let ulList = document.createElement('ul', 'expanding-list');
document.body.appendChild(ulList);

// Method 3: 'new' operator
let ulList = new ExpandingList();
document.body.appendChild(ulList);
```
{% endtab %}
{% endtabs %}

