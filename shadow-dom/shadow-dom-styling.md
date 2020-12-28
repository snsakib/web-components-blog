# Shadow DOM Styling

Just because you’re using a web component doesn’t mean the styles of it are entirely isolated. You might have content within a web component that is styled normally along with the rest of your website.

* **Styling the "Shadow Host" with `:host` selector:**

![Styling the Shadow Host with :host selector](../.gitbook/assets/image%20%2845%29.png)

* **Theming the "Shadow Host":**

![Theming the Shadow Host](../.gitbook/assets/image%20%289%29.png)

* **`:host` has low specificity. More specific selectors in the "Light DOM" may override `:host` selector:**

![&quot;:host&quot; has low specificity](../.gitbook/assets/image%20%2814%29.png)

* **Styling "Shadow Host" states**:
  * :host\(:hover\)
  * :host\(:active\)
  * :host\(:visited\)
  * :host\(:link\)
* **Style `:host` based on matching ancestor using `:host-context`:**
* **Style "Distributed Nodes" with `::content` pseudo-selector:**
* **Avoid "Flash of Unstyled Content" \(FOUC\) using `:unresolved`:**
  * Only elements with a dash \(-\) in their name are affected by `:unresolved`
* **Style "Shadow DOM" from "Light DOM" \(Features in works\):**
  * **Constructible Stylesheets: `CSSStyleSheet()`**
  * **CSS Modules: `import styles from './styles.css'`**
  * `::part()` **:** Modify shadow DOM element styles from light DOM. Can't access the nested elements
  * `::theme()` **:** Modify shadow DOM element styles from light DOM. CanModify shadow DOM element styles from light DOM. Can't access the nested elements access the nested elements

