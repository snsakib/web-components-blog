# How to create & use "Template" & "Slot"

{% tabs %}
{% tab title="index.html" %}
```markup
// 1. Create a template
<template id="my-name">
  <p>Syed Nazmus Sakib</p>
  
  // 9. Create a slot with a unique
  // 'name' attribute
  <slot name="city">Sylhet</slot>
</template>
    
// 8. Instantiate the custom element
<my-name>
  // 10. Use the slot
  <ul slot="city">
    <li>Sylhet</li>
    <li>Dhaka</li>
  </ul>
</my-name>
```
{% endtab %}

{% tab title="index.js" %}
```javascript
class MyName extends HTMLElement {
  constructor() {
    super();
    // 2. Get a reference of the template
    const template = document.getElementById("my-name");
    // 3. Get a reference of the template content
    const templateContent = template.content;
    
    // 4. Create a shadow root
    const shadowRoot = this.attachShadow({ mode: "open" });
    // 5. Clone the template content
    // 6. Append it to the shadow root
    shadowRoot.appendChild(templateContent.cloneNode(true));
  }
}

// 7. Register the custom element
customElements.define("my-name", MyName);

```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
An unnamed [`<slot>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/slot) will be filled with all of the custom element's top-level child nodes that do not have the [`slot`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes#attr-slot) attribute. This includes text nodes.
{% endhint %}

* **Demo:** [**https://stackblitz.com/edit/how-to-use-template-and-slot?file=index.html**](https://stackblitz.com/edit/how-to-use-template-and-slot?file=index.html)\*\*\*\*

