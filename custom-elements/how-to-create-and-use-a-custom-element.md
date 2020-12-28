# How to create & use an "Autonomous Custom Element"

There are 2 steps to create & use a "Custom Element":

* **Registering "Custom Element":**

{% tabs %}
{% tab title="index.js" %}
```javascript
// 1. Create a class which extends generic 'HTMLElement'
class UserName extends HTMLElement {
  // 2. Write all the functionality of the custom element 
  // inside the 'constructor' function
  constructor() {
    // 2.1 Always call 'super()' first to
    // establish the correct prototype chain
    super();
    
    // 2.2 Define the attributes
    const name = "Syed Nazmus Sakib";
    
    // 2.3 Create the HTML structure of the custom element
    const p = document.createElement("p");
    p.textContent = this.hasAttribute("name")
      ? this.getAttribute("name")
      : name;
    
    // 2.4 Create a 'ShadowRoot' which
    // sets & returns 'this.shadowRoot'
    // Read the hint below for more details
    this.attachShadow({ mode: "open" });
    
    // 2.5 Attatch the created HTML structure
    // to the 'Shadow DOM'
    this.shadowRoot.append(p);
  }
}

// 3. Register the custom element in
// the 'CustomElementRegistry'
customElements.define("user-name", UserName);
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
`attachShadow()` method takes as its parameter an options object that contains one option — `mode` — with a value of `open` or `closed` 

`open` means that you can access the shadow DOM using JavaScript written in the main page context

If you attach a shadow root to a custom element with `mode: closed` set, you won't be able to access the shadow DOM from the outside
{% endhint %}

* **Instantiating "Custom Element":** 
  * There are 4 ways to instantiate a 'Custom Element'

{% tabs %}
{% tab title="index.html" %}
```markup
<!-- Method 1: HTML Markup -->
<user-name name="Nazmus Sakib"></user-name>
```
{% endtab %}

{% tab title="index.js" %}
```javascript
// Method 2: 'new' operator
let userName = new UserName();
document.body.appendChild(userName);

// Method 3: createElement
let userName = document.createElement("user-name");
document.body.appendChild(userName);

// Method 4: innerHTML
document.body.innerHTML += "<user-name name='Nazmus Sakib'/>";
```
{% endtab %}
{% endtabs %}

* **Demo:** [**https://stackblitz.com/edit/creating-and-using-autonomous-custom-elements?file=index.html**](https://stackblitz.com/edit/creating-and-using-autonomous-custom-elements?file=index.html)\*\*\*\*



