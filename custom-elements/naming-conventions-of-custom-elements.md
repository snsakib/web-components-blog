# Naming conventions of "Custom Elements"

* **Custom Element's name must have a dash:**

| Valid | Invalid |
| :--- | :--- |
| &lt;my-component&gt; | &lt;mycomponent&gt; |
| &lt;pluralsight-tab&gt; | &lt;pluralsight\_tab&gt; |
| &lt;billing-form&gt; | &lt;billingForm&gt; |

* **Prefix tag names with a unique namespace to avoid naming conflicts. Common namespacing approaches are the following:**
  * Company Name: `<ms-select>`
  * Brand Name: `<ng-select>`
  * Application Name: `<todo-select>`
  * GitHub Username: `<snsakib-select>`

