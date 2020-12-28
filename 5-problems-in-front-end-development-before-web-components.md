# 5 Problems in Front-end Development before "Web Components"

1. **Undescriptive HTML markup:**
   * The "Div" hell
2. **Style conflicts:**
   * Avoiding style conflicts requires highly specific CSS selectors
   * Overuse of "!important" to force styles
   * No guarantee another style won't conflict
3. **No native support of HTML templates/Modular HTML/Reusable HTML:**
   * We can't add HTML code like "&lt;script&gt;" /  "&lt;link&gt;" tags
   * Sometimes we use "&lt;script type='text/html'&gt;". But this cause XSS issues
   * We sometimes use "iframe" to get separate scope and styling. But this creates a complex problem to interact between "iframe" & "host" page
4. **No bundling support:**
   * There is no native way to bundle various HTML, CSS & JS together in a single call.
     * Example: Bootstrap
5. **No Standard:**
   * We can't use one library's component into another library



