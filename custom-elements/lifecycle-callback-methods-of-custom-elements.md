# Lifecycle callback methods of "Custom Elements"

<table>
  <thead>
    <tr>
      <th style="text-align:left">Lifecycle Callback Methods</th>
      <th style="text-align:left">Descriptions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">connectedCallback</td>
      <td style="text-align:left">
        <p>Invoked each time the custom element is appended into a document-connected
          element. This will happen each time the node is moved and may happen before
          the element&apos;s contents have been fully parsed.</p>
        <p><code>connectedCallback</code> may be called once your element is no longer
          connected, use <a href="https://developer.mozilla.org/en-US/docs/Web/API/Node/isConnected"><code>Node.isConnected</code></a> to
          make sure.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">disconnectedCallback</td>
      <td style="text-align:left">Invoked each time the custom element is disconnected from the document&apos;s
        DOM.</td>
    </tr>
    <tr>
      <td style="text-align:left">adoptedCallback</td>
      <td style="text-align:left">Invoked each time the custom element is moved to a new document.</td>
    </tr>
    <tr>
      <td style="text-align:left">attributeChangedCallback</td>
      <td style="text-align:left">Invoked each time one of the custom element&apos;s attributes is added,
        removed, or changed. Which attributes to notice the change for is specified
        in a static get <code>observedAttributes</code> method</td>
    </tr>
  </tbody>
</table>

