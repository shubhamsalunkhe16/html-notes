## What is HTML ?

- stands for `Hyper Text Markup Language`
- describes the `structure of Web pages` using markup
- `building blocks` of web pages
- `represented by tags`
- `use them to render the content` on the web page (audio, text, images, etc.)

---

## HTML Page Structure

![html_structure](./images/html_structure.png)

---

## `<head>` Tag

- container for `metadata` and `links` that define the document's properties.

### Common Elements in `<head>`:

- `<title>`: Defines the title of the document, displayed on the browser tab.
- `<meta>`: Provides metadata such as character encoding, description, keywords, etc.
- `<link>`: Links to external resources like stylesheets.
- `<style>`: Contains internal CSS.
- `<script>`: Includes or links to JavaScript files.
- `<base>`: Specifies the base URL for relative links.

### `Meta Tags`

- provide `additional information` about the webpage.
- `not visible to users` but are `critical for SEO`, `accessibility`, and `browser behavior.`

### Commonly Used Meta Tags:

| **Meta Tag**                | **Description**                                                                | **Example**                                                                  |
| --------------------------- | ------------------------------------------------------------------------------ | ---------------------------------------------------------------------------- |
| **Charset**                 | Defines the character encoding for the webpage. Ensures proper text rendering. | `<meta charset="UTF-8">`                                                     |
| **Viewport**                | Controls page scaling on mobile devices. Makes websites responsive.            | `<meta name="viewport" content="width=device-width, initial-scale=1.0">`     |
| **Description**             | Provides a short description of the page for search engines (SEO).             | `<meta name="description" content="Best soy candles with soothing scents.">` |
| **Keywords** _(deprecated)_ | Used to specify keywords for search engines (mostly ignored now).              | `<meta name="keywords" content="candles, soy wax, handmade">`                |
| **Author**                  | Defines the author of the webpage.                                             | `<meta name="author" content="Shubham Salunkhe">`                            |
| **Robots**                  | Instructs search engine crawlers on indexing/following links.                  | `<meta name="robots" content="index, follow">`                               |
| **Refresh/Redirect**        | Automatically refreshes or redirects a page after a given time.                | `<meta http-equiv="refresh" content="5;url=https://example.com">`            |
| **HTTP-Equiv**              | Provides HTTP headers (e.g., content type, cache control).                     | `<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">`        |
| **Theme Color**             | Sets the browser’s theme color (for mobile address bar customization).         | `<meta name="theme-color" content="#ffffff">`                                |
| **Open Graph (OG)**         | Used for social media sharing (Facebook, LinkedIn).                            | `<meta property="og:title" content="Buy Premium Soy Candles">`               |
| **Twitter Cards**           | Controls how links appear when shared on Twitter.                              | `<meta name="twitter:card" content="summary_large_image">`                   |

### Link Tags

- Used to link external resources like CSS, icons, and prefetching resources.

####

```html
<!-- Linking Stylesheets -->
<link rel="stylesheet" href="styles.css" />

<!-- Adding Favicons -->
<link rel="icon" href="favicon.ico" type="image/x-icon" />

<!-- Preloading Resources -->
<link rel="preload" href="image.jpg" as="image" />
```

### Script Tags

- Used to include JavaScript.

```html
<script src="script.js"></script>
```

### Base Tag

- Specifies the base URL for relative links.

```html
<base href="https://example.com/" />
```

---

## Comments

```html
<!-- Write your comments here -->
```

- `not displayed` by the browser.
- `can help to document` source code.

---

## How HTML elements should be displayed/styled by CSS?

- CSS can be added to HTML elements in `3 ways`：

| **Aspect**          | **Inline**                          | **Internal**                       | **External**             |
| ------------------- | ----------------------------------- | ---------------------------------- | ------------------------ |
| **Written in**      | `style` attribute.                  | `<style>` in `<head>`.             | Separate `.css` file.    |
| **Syntax Example**  | `<h1 style="color:red;">Hello</h1>` | `<style>h1 {color: blue;}</style>` | `h1 { color: green; }`   |
| **Scope**           | Single element.                     | One page.                          | Multiple pages.          |
| **Reusability**     | ❌ None.                            | ❌ Page-specific.                  | ✅ Fully reusable.       |
| **Maintainability** | ❌ Poor.                            | ⚠️ Medium.                         | ✅ Best (centralized).   |
| **Performance**     | ⚠️ Slightly faster.                 | ⚠️ Loads with HTML.                | ✅ Cached, faster.       |
| **Best for**        | Quick fixes/testing.                | Single-page styles.                | Full sites/pro projects. |
| **Readability**     | ❌ Messy.                           | ⚠️ Better.                         | ✅ Clean separation.     |

---

## Makes HTML pages more dynamic and interactive by JavaScript

- JS can be added to HTML elements in `3 ways`：

| **Aspect**          | **Inline**                                            | **Internal**                              | **External**                                                 |
| ------------------- | ----------------------------------------------------- | ----------------------------------------- | ------------------------------------------------------------ |
| **Written in**      | `onclick`, `onchange`.                                | `<script>` in HTML.                       | Separate `.js` file.                                         |
| **Syntax Example**  | `<button onclick="alert('Hello!')">Click Me</button>` | `<script>console.log("Hello!");</script>` | `<script src="app.js"></script>`<br>`console.log("Hello!");` |
| **Scope**           | Single element/action.                                | One page.                                 | Multiple pages.                                              |
| **Reusability**     | ❌ None.                                              | ❌ Page-specific.                         | ✅ Fully reusable.                                           |
| **Maintainability** | ❌ Poor.                                              | ⚠️ Medium.                                | ✅ Best (centralized).                                       |
| **Performance**     | ⚠️ Slightly faster.                                   | ⚠️ Blocks if in `<head>`.                 | ✅ Cached, can use `defer`.                                  |
| **Best for**        | Quick event handlers.                                 | Small page-specific JS.                   | Full websites/web apps.                                      |
| **Readability**     | ❌ Messy.                                             | ⚠️ Better.                                | ✅ Clean separation.                                         |

---

## HTML Elements

- usually consists of a `start tag` and `end tag`, with the `content` inserted in between.

![html_tag_breakdown](./images/html_tag_breakdown.png)

### Do Not Forget the End Tag

- Some HTML elements `will display correctly, even if you forget the end tag`：

  ```html
  <html>
    <body>
      <p>This is a paragraph</p>
      <p>This is a paragraph</p>
    </body>
  </html>
  ```

> Never rely on this. It might produce unexpected results and/or errors if you forget the end tag.

### Empty HTML Elements

- `elements with no content, so no closing tag`
- Empty elements `can be closed in the opening tag` like this：`<br />`.

### Use Lowercase Tags

- `not case sensitive`：`<P>` means the same as `<p>`.
- `recommends lowercase.`

### Nesting elements

- `elements can contain other elements`

```html
<p>My cat is <strong>very</strong> grumpy.</p>
```

#### wrong way

```html
<p>My cat is <strong>very grumpy.</p></strong>
```

---

## HTML Attributes

- provide `additional information` about an element.
- `always specified in the start tag`.
- `name/value pairs` like：name="value".
- `not case sensitive`
- `recommends lowercase`

### Core/Global Attributes

- 5 core attributes are `id`,`class`,`title`,`style`,`data-*`

| **Attribute** | **Purpose**                                                                                | **Example**                                            | **Notes / Use Cases**                                                                                                              |
| ------------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| **`id`**      | Assigns a **unique identifier** to an element. Used for CSS, JS, and navigation (anchors). | `<div id="header"></div>`                              | Must be **unique per page**. Often used for **JS targeting** (`document.getElementById`) and **CSS styling** (`#header`).          |
| **`class`**   | Assigns one or more **class names** to an element for styling or scripting.                | `<p class="intro highlight"></p>`                      | Can be reused across multiple elements. Useful for **group styling** and **JS selectors** (`document.querySelectorAll('.class')`). |
| **`title`**   | Provides **extra information** about an element (tooltip on hover).                        | `<button title="Click to submit form">Submit</button>` | Improves **accessibility** and **UX**. Screen readers also read this.                                                              |
| **`style`**   | Adds **inline CSS** styles directly to the element.                                        | `<h1 style="color:red; font-size:20px;">Hello</h1>`    | **Avoid for large projects** — hard to maintain. Use **external CSS** instead.                                                     |
| **`data-*`**  | Stores **custom data** on elements without affecting rendering.                            | `<div data-user-id="123" data-role="admin"></div>`     | Used to store **dynamic values** for **JavaScript** (e.g., `element.dataset.userId`). Very helpful in **dynamic UIs**.             |

---

## HTML Text Markup Elements

| **Tag**        | **Purpose**                                             | **Example (Code)**                                     | **How It Displays**                                | **Notes / Usage**                                                       |
| -------------- | ------------------------------------------------------- | ------------------------------------------------------ | -------------------------------------------------- | ----------------------------------------------------------------------- |
| `<h1>`–`<h6>`  | Defines **headings** (h1 = most important, h6 = least). | `<h1>Main Title</h1>`<br>`<h3>Subheading</h3>`         | **Main Title** (large)<br>**Subheading** (smaller) | **Use for content hierarchy & SEO.** Only one `<h1>` per page ideally.  |
| `<p>`          | Defines a **paragraph**.                                | `<p>This is a paragraph.</p>`                          | Adds space above & below text                      | Basic content container. **Block-level element.**                       |
| `<span>`       | Generic **inline container** for text.                  | `<span class="highlight">Text</span>`                  | No visual change by default                        | Use for **styling specific text** or **wrapping small inline content**. |
| `<b>`          | Makes text **bold** (no semantic meaning).              | `<b>Important</b>`                                     | **Important**                                      | Purely visual. Prefer `<strong>` when meaning matters.                  |
| `<strong>`     | Marks text as **important** (bold + semantic).          | `<strong>Warning!</strong>`                            | **Warning!**                                       | Semantic emphasis. Screen readers highlight it.                         |
| `<i>`          | Makes text **italic** (visual only).                    | `<i>Italic text</i>`                                   | _Italic text_                                      | Prefer `<em>` for meaningful emphasis.                                  |
| `<em>`         | Adds **emphasis** (italic + semantic).                  | `<em>Very important</em>`                              | _Very important_                                   | Better for accessibility than `<i>`.                                    |
| `<mark>`       | Highlights text.                                        | `This is <mark>highlighted</mark>.`                    | This is <mark>highlighted</mark>.                  | Useful for search results or key terms.                                 |
| `<small>`      | Renders text **smaller** than normal.                   | `<small>Fine print</small>`                            | <small>Fine print</small>                          | Often used for disclaimers or captions.                                 |
| `<del>`        | Shows **deleted** (strikethrough) text.                 | `<del>Old price: $50</del>`                            | <del>Old price: \$50</del>                         | Used for content removal (often with `<ins>`).                          |
| `<ins>`        | Shows **inserted** (underlined) text.                   | `<ins>New price: $40</ins>`                            | <ins>New price: \$40</ins>                         | Indicates added content.                                                |
| `<sub>`        | Displays **subscript** text.                            | `H<sub>2</sub>O`                                       | H<sub>2</sub>O                                     | Used in chemical formulas or math.                                      |
| `<sup>`        | Displays **superscript** text.                          | `E = mc<sup>2</sup>`                                   | E = mc<sup>2</sup>                                 | Used for powers, ordinals, footnotes.                                   |
| `<q>`          | Inline **short quotation**.                             | `<q>This is a quote</q>`                               | “This is a quote”                                  | Adds quotation marks automatically.                                     |
| `<blockquote>` | **Block-level quotation**.                              | `<blockquote>Quoted paragraph</blockquote>`            | Indented block of text                             | Used for large quotes, often with `<cite>`.                             |
| `<code>`       | Displays **inline code**.                               | `<code>console.log('Hello')</code>`                    | `console.log('Hello')`                             | Use inside `<pre>` for multi-line code blocks.                          |
| `<pre>`        | **Preformatted** text (preserves spacing).              | `<pre>  Indented text</pre>`                           | Preserves spaces & line breaks                     | Used for code, ASCII art, or preformatted text.                         |
| `<abbr>`       | Defines an **abbreviation**.                            | `<abbr title="Hypertext Markup Language">HTML</abbr>`  | HTML _(tooltip on hover)_                          | Improves accessibility with tooltips.                                   |
| `<cite>`       | Marks a **citation/reference**.                         | `<cite>— Shakespeare</cite>`                           | — Shakespeare                                      | Used for sources, books, authors.                                       |
| `<dfn>`        | Defines a **term**.                                     | `<dfn>API</dfn> is Application Programming Interface.` | **API** is Application Programming Interface.      | Indicates a term being defined.                                         |

---

## HTML Links

- HTML links are `hyperlinks`
- can click on a link and `jump to another document`
- `Note:` A link does not have to be text. A `link can be an image or any other HTML element!`

| **Attribute / Type**            | **Purpose**                                                   | **Example**                                                                             | **Notes / Usage**                                                                      |
| ------------------------------- | ------------------------------------------------------------- | --------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| **`href`**                      | Defines the destination of the link.                          | `<a href="https://example.com">Visit</a>`                                               | Can be **absolute** (`https://...`), **relative** (`/about`), **anchor** (`#section`). |
| **Relative link**               | Links to a page **within the same site/project**.             | `<a href="/about.html">About Us</a>`                                                    | Good for internal navigation.                                                          |
| **Absolute link**               | Links to a **complete URL** (external site).                  | `<a href="https://google.com">Google</a>`                                               | Used for external resources.                                                           |
| **Anchor link**                 | Jumps to a **specific section** on the same page.             | `<a href="#contact">Contact</a>` → `<div id="contact">...</div>`                        | Great for **page navigation** (Table of contents, jump links).                         |
| **`target="_self"`**            | Opens in the **same tab** (default).                          | `<a href="page.html" target="_self">Same Tab</a>`                                       | Default behavior.                                                                      |
| **`target="_blank"`**           | Opens link in a **new tab/window**.                           | `<a href="https://example.com" target="_blank">New Tab</a>`                             | Use with `rel="noopener noreferrer"` for **security**.                                 |
| **`rel="noopener noreferrer"`** | **Prevents tabnabbing** & hides referrer info.                | `<a href="https://example.com" target="_blank" rel="noopener noreferrer">Safe Link</a>` | Must use with `target="_blank"` for security.                                          |
| **`download`**                  | Forces the link to **download** a file instead of opening it. | `<a href="file.pdf" download>Download PDF</a>`                                          | Works for same-origin or properly configured cross-origin files.                       |
| **`mailto:`**                   | Opens the user’s **email client**.                            | `<a href="mailto:hello@example.com">Email Us</a>`                                       | Can include subject: `mailto:hello@example.com?subject=Hi`.                            |
| **`tel:`**                      | Opens the **phone dialer** on supported devices.              | `<a href="tel:+1234567890">Call Us</a>`                                                 | Commonly used in **mobile-friendly sites**.                                            |
| **`title`**                     | Adds a **tooltip** on hover.                                  | `<a href="about.html" title="Learn more about us">About</a>`                            | Improves accessibility & UX.                                                           |
| **`accesskey`**                 | Defines a **keyboard shortcut** for the link.                 | `<a href="/home" accesskey="h">Home</a>`                                                | Rarely used; use carefully for accessibility.                                          |
| **`tabindex`**                  | Sets **tab order** for keyboard navigation.                   | `<a href="/contact" tabindex="2">Contact</a>`                                           | Helps with **keyboard navigation**.                                                    |

---

## HTML Images `<img>`

| **Attribute**        | **Purpose**                                                 | **Example**                                                                              | **Notes / Usage**                                                              |
| -------------------- | ----------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **`src`**            | Specifies the **image source** (URL or path).               | `<img src="images/photo.jpg" alt="Profile Photo">`                                       | Can be **relative** (`/img/pic.png`) or **absolute** (`https://...`).          |
| **`alt`**            | Provides **alternative text** for the image.                | `<img src="logo.png" alt="Company Logo">`                                                | **Crucial for accessibility** & shown when image fails to load. Helps **SEO**. |
| **`title`**          | Adds a **tooltip** when hovering over the image.            | `<img src="cat.jpg" alt="Cat" title="Cute Cat">`                                         | Optional, improves UX but not a replacement for `alt`.                         |
| **`width`**          | Sets the **image width** (in px or %).                      | `<img src="img.jpg" width="200">`                                                        | Better to use **CSS** for responsiveness instead of inline width.              |
| **`height`**         | Sets the **image height**.                                  | `<img src="img.jpg" height="150">`                                                       | Keep **aspect ratio** consistent to avoid distortion.                          |
| **`loading`**        | Enables **lazy loading** of images.                         | `<img src="big.jpg" alt="Big Image" loading="lazy">`                                     | `lazy` delays loading off-screen images → **faster page speed**.               |
| **`srcset`**         | Provides **multiple image versions** for different devices. | `<img src="small.jpg" srcset="medium.jpg 768w, large.jpg 1200w" alt="Responsive Image">` | **Responsive images**: browser picks the best size.                            |
| **`sizes`**          | Works with `srcset` to define image display size.           | `<img src="small.jpg" srcset="medium.jpg 768w" sizes="(max-width: 768px) 100vw, 50vw">`  | Helps the browser **choose optimal image** for the screen size.                |
| **`crossorigin`**    | Handles **cross-origin image requests**.                    | `<img src="https://cdn.com/img.jpg" crossorigin="anonymous">`                            | Needed for **CORS-enabled images** (like for canvas editing).                  |
| **`usemap`**         | Links image to a **map** for clickable regions.             | `<img src="map.jpg" usemap="#worldmap">`                                                 | Used with `<map>` + `<area>` for interactive images.                           |
| **`decoding`**       | Hints how the browser should **decode the image**.          | `<img src="photo.jpg" decoding="async">`                                                 | `async` improves perceived performance by not blocking rendering.              |
| **`referrerpolicy`** | Controls **referrer info** sent with image requests.        | `<img src="image.jpg" referrerpolicy="no-referrer">`                                     | Enhances **privacy/security**.                                                 |

### Image Maps

- An image map is an `image with clickable areas`
- The areas are defined with one or more `<area>` tags.

```html
<img src="workplace.jpg" alt="Workplace" usemap="#workmap" />

<map name="workmap">
  <area
    shape="rect"
    coords="290,172,333,250"
    alt="Phone"
    href="phone.htm"
    onclick="myFunction()"
  />
  <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm" />
  <area
    shape="poly"
    coords="140,121,181,116,204,160,204,222,191,270,140,329,85,355,58,352,37,322,40,259,103,161,128,147"
    href="croissant.htm"
  />
</map>
<script>
  function myFunction() {
    alert("You clicked the Phone!");
  }
</script>
```

### HTML `<picture>` Element

- allows to display `different pictures for different devices or screen sizes`.

```html
<picture>
  <source media="(min-width: 650px)" srcset="img_food.jpg" />
  <source media="(min-width: 465px)" srcset="img_car.jpg" />
  <img src="img_girl.jpg" />
</picture>
```

`Note:`

- Always specify an `<img>` element as the `last child` element of the `<picture>` element for `fallback`.

### HTML Favicon

```html
<head>
  <title>My Page Title</title>
  <link rel="icon" type="image/x-icon" href="/images/favicon.ico" />
</head>
```

- `Tip`: A favicon is a small image, so it should be a simple image with high contrast.

---

## Lists `<ol>/<ul>/<dl>`

### Ordered lists `<ol>`

- An ordered list can be numerical or alphabetical
- `type attribute` defines the type of the list item marker
- `type="A"/"a"/"I"/"i"`
- By default, an ordered list will `start counting from 1`
- to start from a specified number, you can use the `start attribute`

```html
<ol type="1" start="5">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

### _output :_

<ol type="1" start="5">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>

### Unordered lists `<ul>`

- List items will be `marked with bullets`
- `type attribute` defines the type of the list item marker
- `type="disc/circle/square/none"`

```html
<ul type="square">
  <li>technologists</li>
  <li>thinkers</li>
  <li>builders</li>
</ul>
```

### _output :_

<ul type="square">
  <li>technologists</li>
  <li>thinkers</li>
  <li>builders</li>
</ul>

### Description list `<dl>`

- list of terms`<dt>`, with a description`<dd>` of each term.

```html
<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>
```

### _output :_

<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>

---

## HTML Tables

- consists of table cells inside `rows and columns`

| **Tag / Attribute**    | **Purpose**                                 | **Example**                              | **Notes / Usage**                                                              |
| ---------------------- | ------------------------------------------- | ---------------------------------------- | ------------------------------------------------------------------------------ |
| **`<table>`**          | Wraps the entire table.                     | `<table>...</table>`                     | Always the outermost container for a table.                                    |
| **`<tr>`**             | Defines a **table row**.                    | `<tr><td>Cell</td></tr>`                 | Must be inside `<table>`.                                                      |
| **`<td>`**             | Defines a **table data cell**.              | `<td>Data</td>`                          | Default cell element for table content.                                        |
| **`<th>`**             | Defines a **table header cell**.            | `<th>Heading</th>`                       | By default **bold + centered**. Use `scope` for accessibility.                 |
| **`<thead>`**          | Groups **header rows**.                     | `<thead><tr><th>Col1</th></tr></thead>`  | Useful for separating table headings (especially for accessibility & styling). |
| **`<tbody>`**          | Groups **body rows**.                       | `<tbody><tr><td>Data</td></tr></tbody>`  | Helps organize table structure.                                                |
| **`<tfoot>`**          | Groups **footer rows**.                     | `<tfoot><tr><td>Total</td></tr></tfoot>` | Useful for summaries (e.g., totals in reports).                                |
| **`colspan`**          | **Merges columns** within a cell.           | `<td colspan="2">Merged Cell</td>`       | Used when one cell spans multiple columns.                                     |
| **`rowspan`**          | **Merges rows** within a cell.              | `<td rowspan="2">Merged Cell</td>`       | Used when one cell spans multiple rows.                                        |
| **`caption`**          | Adds a **title/caption** to a table.        | `<caption>Monthly Report</caption>`      | Should be the first child of `<table>`. Improves accessibility.                |
| **`scope`** (th)       | Defines **cell scope** for accessibility.   | `<th scope="col">Name</th>`              | Values: `col`, `row`, `colgroup`, `rowgroup`. Helps screen readers.            |
| **`border`**           | Sets a **border** around the table (HTML4). | `<table border="1">`                     | Deprecated → use CSS `border`.                                                 |
| **`width` / `height`** | Sets table/cell size (HTML4).               | `<table width="100%">`                   | Deprecated → use CSS instead.                                                  |
| **`align`**            | Aligns table or cell content.               | `<td align="center">Text</td>`           | Deprecated → use CSS `text-align`.                                             |

```html
<table>
  <caption>
    Student Scores
  </caption>
  <thead>
    <tr>
      <th scope="col">Name</th>
      <th scope="col">Score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John</td>
      <td>85</td>
    </tr>
    <tr>
      <td>Mary</td>
      <td>92</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="2">Average: 88.5</td>
    </tr>
  </tfoot>
</table>
```

<table>
  <caption>Student Scores</caption>
  <thead>
    <tr>
      <th scope="col">Name</th>
      <th scope="col">Score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John</td>
      <td>85</td>
    </tr>
    <tr>
      <td>Mary</td>
      <td>92</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="2">Average: 88.5</td>
    </tr>
  </tfoot>
</table>

---

## HTML Form Tags

| **Tag**          | **Purpose**                              | **How It Displays**                                                                                                                  | **Example**                                                                         | **Notes / Usage**                                          |
| ---------------- | ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| **`<form>`**     | Wraps all form controls.                 | _(No visible UI — just a container)_                                                                                                 | `<form action="/submit" method="POST">...</form>`                                   | Must include `action` (URL) & `method` (`GET`/`POST`).     |
| **`<input>`**    | Single-line input field (various types). | <input type="text" placeholder="Sample input">                                                                                       | `<input type="text" name="username">`                                               | The most versatile tag. `type` defines its behavior.       |
| **`<textarea>`** | Multi-line text input.                   | <textarea rows="3" cols="25">Sample text</textarea>                                                                                  | `<textarea rows="4" cols="30"></textarea>`                                          | For longer text inputs (e.g., comments).                   |
| **`<select>`**   | Dropdown menu (single or multiple).      | <select><option>India</option><option>USA</option></select>                                                                          | `<select><option>India</option></select>`                                           | Use `multiple` for multi-select.                           |
| **`<option>`**   | An option inside `<select>`.             | <select><option selected>India</option><option>USA</option></select>                                                                 | `<option value="IN">India</option>`                                                 | Use `selected` to pre-select.                              |
| **`<optgroup>`** | Groups options in a dropdown.            | <select><optgroup label="Asia"><option>India</option></optgroup><optgroup label="Europe"><option>France</option></optgroup></select> | `<optgroup label="Asia"><option>India</option></optgroup>`                          | Helps categorize dropdown values.                          |
| **`<button>`**   | Clickable button.                        | <button type="submit">Submit</button>                                                                                                | `<button type="submit">Submit</button>`                                             | Types: `submit`, `reset`, `button`.                        |
| **`<label>`**    | Labels form controls.                    | <label for="email">Email:</label> <input id="email" type="email">                                                                    | `<label for="email">Email:</label>`                                                 | Clicking it focuses the input with matching `id`.          |
| **`<fieldset>`** | Groups related fields.                   | <fieldset><legend>Login</legend><input type="text" placeholder="Username"></fieldset>                                                | `<fieldset><legend>Login</legend>...</fieldset>`                                    | Improves structure & accessibility.                        |
| **`<legend>`**   | Title for a `<fieldset>`.                | <fieldset><legend>Personal Info</legend><input type="text" placeholder="Name"></fieldset>                                            | `<legend>Personal Info</legend>`                                                    | Gives context to grouped inputs.                           |
| **`<datalist>`** | Provides auto-suggestions.               | <input list="browsers"><datalist id="browsers"><option>Chrome</option><option>Firefox</option></datalist>                            | `<input list="browsers"><datalist id="browsers"><option>Chrome</option></datalist>` | Works with `<input list="">`.                              |
| **`<output>`**   | Displays calculated results.             | <output name="result">0</output>                                                                                                     | `<output name="result">0</output>`                                                  | Can dynamically show results (e.g., JS-calculated values). |
| **`<progress>`** | Shows task progress.                     | <progress value="70" max="100"></progress>                                                                                           | `<progress value="70" max="100"></progress>`                                        | For indicating progress in tasks.                          |
| **`<meter>`**    | Displays a measurement within a range.   | <meter value="0.6" min="0" max="1"></meter>                                                                                          | `<meter value="0.6" min="0" max="1"></meter>`                                       | For displaying scores or capacity levels.                  |

## HTML Form Attributes

| **Attribute**      | **Purpose**                                  | **How It Displays**                                                                                       | **Example**                                                                         | **Notes / Usage**                                                               |
| ------------------ | -------------------------------------------- | --------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **`action`**       | URL where form data is sent.                 | _(No visual effect)_                                                                                      | `<form action="/submit">`                                                           | Can be **relative** (`/submit`) or **absolute** (`https://...`).                |
| **`method`**       | HTTP method for form submission.             | _(No visual effect)_                                                                                      | `<form method="POST">`                                                              | `GET` → appends data in URL (**visible**). `POST` → sends in body (**secure**). |
| **`enctype`**      | Encoding type for submitted data.            | _(No visual effect)_                                                                                      | `<form enctype="multipart/form-data">`                                              | Required for **file uploads**. Default: `application/x-www-form-urlencoded`.    |
| **`target`**       | Where to open the response.                  | _(No visual effect)_                                                                                      | `<form target="_blank">`                                                            | `_self` (default), `_blank` (new tab), `_parent`, `_top`.                       |
| **`name`**         | Key name for form data (used in submission). | <input type="text" name="email" placeholder="Email">                                                      | `<input type="text" name="email">`                                                  | **Mandatory** for input to be included in submission.                           |
| **`id`**           | Unique identifier for elements.              | <input id="username" placeholder="Username">                                                              | `<input id="username">`                                                             | Used with `<label for="id">` & JS access.                                       |
| **`value`**        | Default/pre-filled value.                    | <input type="text" value="John">                                                                          | `<input type="text" value="John">`                                                  | Sets initial input value.                                                       |
| **`placeholder`**  | Hint text inside the input field.            | <input type="text" placeholder="Enter name">                                                              | `<input type="text" placeholder="Enter name">`                                      | **Not a replacement for labels**.                                               |
| **`required`**     | Makes a field mandatory.                     | <input type="email" placeholder="Email" required>                                                         | `<input type="email" required>`                                                     | Prevents form submission if empty.                                              |
| **`readonly`**     | Makes input non-editable (still submits).    | <input type="text" value="123" readonly>                                                                  | `<input type="text" value="123" readonly>`                                          | Unlike `disabled`, value **is submitted**.                                      |
| **`disabled`**     | Disables input (cannot edit/submit).         | <input type="text" value="Disabled" disabled>                                                             | `<input type="text" disabled>`                                                      | Value **is not sent** to server.                                                |
| **`multiple`**     | Allows multiple selections.                  | <input type="file" multiple>                                                                              | `<input type="file" multiple>`                                                      | Works for file inputs & multi-select dropdowns.                                 |
| **`checked`**      | Pre-checks a checkbox/radio button.          | <input type="checkbox" checked>                                                                           | `<input type="checkbox" checked>`                                                   | Used for `checkbox` & `radio`.                                                  |
| **`selected`**     | Pre-selects an option in dropdown.           | <select><option selected>India</option><option>USA</option></select>                                      | `<option value="IN" selected>India</option>`                                        | Used inside `<select>`.                                                         |
| **`autocomplete`** | Enables/disables browser auto-fill.          | _(No visual effect)_                                                                                      | `<form autocomplete="off">`                                                         | Can be `on` or `off`.                                                           |
| **`min` / `max`**  | Sets numeric or date limits.                 | <input type="number" min="1" max="10" value="5">                                                          | `<input type="number" min="1" max="10">`                                            | Works with `number`, `date`, `range`.                                           |
| **`step`**         | Defines input step intervals.                | <input type="number" step="0.5" value="2.5">                                                              | `<input type="number" step="0.5">`                                                  | Useful for precise numeric/range inputs.                                        |
| **`pattern`**      | Adds **regex validation**.                   | <input type="text" pattern="[A-Za-z]{3,}" placeholder="Only letters">                                     | `<input type="text" pattern="[A-Za-z]{3,}">`                                        | Ensures input matches the regex pattern.                                        |
| **`maxlength`**    | Limits max characters in input.              | <input type="text" maxlength="10" placeholder="Max 10">                                                   | `<input type="text" maxlength="10">`                                                | Prevents extra characters.                                                      |
| **`size`**         | Visible width of input in characters.        | <input type="text" size="30" value="Wide Field">                                                          | `<input type="text" size="30">`                                                     | **Only visual**; doesn’t restrict length.                                       |
| **`list`**         | Binds `<input>` to `<datalist>`.             | <input list="browsers"><datalist id="browsers"><option>Chrome</option><option>Firefox</option></datalist> | `<input list="browsers"><datalist id="browsers"><option>Chrome</option></datalist>` | Provides auto-suggestions.                                                      |
| **`novalidate`**   | Disables built-in HTML5 validation.          | _(No visual effect)_                                                                                      | `<form novalidate>`                                                                 | Lets JS handle validation manually.                                             |

---

## HTML Iframe

- used to `embed another document` within the `current HTML document`

```html
<iframe src="url" title="description"></iframe>
```

- `title` attribute used by `screen readers` to read out what the content of the iframe is

---

## HTML Computer Code Elements

| **Tag**      | **Purpose**                                             | **How It Displays**                                 | **Example**                                        | **Notes / Usage**                                                 |
| ------------ | ------------------------------------------------------- | --------------------------------------------------- | -------------------------------------------------- | ----------------------------------------------------------------- |
| **`<code>`** | Represents **inline computer code**.                    | <p>Use <code>console.log()</code> in JS.</p>        | `<p>Use <code>console.log()</code> in JS.</p>`     | For **short inline code snippets**. Doesn’t preserve line breaks. |
| **`<pre>`**  | Preformatted text (**preserves spaces & line breaks**). | <br><pre>function test() {<br> return 1;<br>}</pre> | `<pre>function test() {<br>  return 1;<br>}</pre>` | Best for **multiline code**. Often used with `<code>`.            |
| **`<samp>`** | Represents **sample program output**.                   | <p>Output: <samp>Hello, World!</samp></p>           | `<p>Output: <samp>Hello, World!</samp></p>`        | Good for **program outputs** or results.                          |
| **`<kbd>`**  | Represents **keyboard input**.                          | <p>Press <kbd>Ctrl</kbd> + <kbd>C</kbd></p>         | `<p>Press <kbd>Ctrl</kbd> + <kbd>C</kbd></p>`      | Used for **keyboard shortcuts** or user input.                    |
| **`<var>`**  | Represents **variables in programming**.                | <p>The variable <var>x</var> stores value.</p>      | `<p>The variable <var>x</var> stores value.</p>`   | Good for **variables** in math/code expressions.                  |

---

## HTML `<details>` and `<summary>` Elements

- specifies `additional details` that the user `can open and close on demand`

```html
<details>
  <summary>Epcot Center</summary>
  <p>
    Epcot is a theme park at Walt Disney World Resort featuring exciting
    attractions.
  </p>
</details>
```

### _output:_

<details>
  <summary>Epcot Center</summary>
  <p>Epcot is a theme park at Walt Disney World Resort featuring exciting attractions.</p>
</details>

---

## HTML `<figure>` and `<figcaption>` Elements

```html
<figure>
  <img src="pic_trulli.jpg" alt="Trulli" />
  <figcaption>Fig1. - Trulli, Puglia, Italy.</figcaption>
</figure>
```

---

## HTML `<time>` Elements

```html
<p>I have a date on <time datetime="2008-02-14 20:00">Valentines day</time>.</p>
```

### _output:_

<p>I have a date on <time datetime="2008-02-14 20:00">Valentines day</time>.</p>

---

## HTML Multimedia

| **Tag**        | **Purpose**                          | **Example (Code)**                                                                               | **How It Displays**                                                                                                                                                        | **Notes / Usage**                                                                 |
| -------------- | ------------------------------------ | ------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `<img>`        | Embeds an **image**.                 | `<img src="image.jpg" alt="Sample" width="200">`                                                 | <img src="https://fastly.picsum.photos/id/553/200/200.jpg?hmac=HSLKzqqoxnajv4KjLxYSjZokWcuCCiZLGdRPUoryhXk" alt="Sample" width="150">                                      | Always include **`alt`** for accessibility & SEO. Use `width`/`height` to resize. |
| `<audio>`      | Embeds an **audio player**.          | `<audio controls><source src="sound.mp3" type="audio/mpeg"></audio>`                             | <audio controls><source src="https://www.w3schools.com/html/horse.mp3" type="audio/mpeg"></audio>                                                                          | Use `controls` for play/pause UI. Multiple `<source>` tags for fallback formats.  |
| `<video>`      | Embeds a **video player**.           | `<video width="320" controls><source src="movie.mp4" type="video/mp4"></video>`                  | <video width="200" controls><source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4"></video>                                                             | Add `controls` for play/pause. Use `poster` for thumbnail before play.            |
| `<source>`     | Provides **media sources**.          | `<video controls><source src="movie.mp4" type="video/mp4"></video>`                              | _(No direct display — works inside `<video>`/`<audio>`)_                                                                                                                   | Add multiple formats (`mp4`, `ogg`, `webm`) for cross-browser compatibility.      |
| `<track>`      | Adds **subtitles or captions**.      | `<video controls><track src="subs.vtt" kind="subtitles" srclang="en" label="English"></video>`   | _(No direct display — enables captions/subtitles)_                                                                                                                         | Works inside `<video>`. Use `.vtt` (WebVTT) files for subtitles.                  |
| `<iframe>`     | Embeds another **webpage** or media. | `<iframe src="https://www.example.com" width="300" height="200"></iframe>`                       | <iframe src="https://www.example.com" width="200" height="100"></iframe>                                                                                                   | Used for embedding external content (maps, YouTube, etc.).                        |
| `<embed>`      | Embeds **external content**.         | `<embed src="file.pdf" width="500" height="300">`                                                | _(Displays embedded file content)_                                                                                                                                         | Mostly for PDFs or plugins. Limited styling.                                      |
| `<object>`     | Embeds external objects/files.       | `<object data="file.pdf" type="application/pdf" width="500" height="300"></object>`              | _(Displays embedded object)_                                                                                                                                               | Similar to `<embed>`. Can provide fallback content between tags.                  |
| `<canvas>`     | Creates a **drawable area** (JS).    | `<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000;"></canvas>`        | <canvas id="myCanvas" width="200" height="100" style="border:1px solid #000;"></canvas>                                                                                    | Used with **JavaScript** for graphics, games, charts, etc.                        |
| `<svg>`        | Displays **vector graphics**.        | `<svg width="100" height="100"><circle cx="50" cy="50" r="40" stroke="black" fill="red"/></svg>` | <svg width="100" height="100"><circle cx="50" cy="50" r="40" stroke="black" fill="red"/></svg>                                                                             | Scalable graphics. Better than images for icons, shapes, animations.              |
| `<figure>`     | Wraps media (image/video).           | `<figure><img src="image.jpg" alt="Sample"><figcaption>Caption</figcaption></figure>`            | <figure><img src="https://fastly.picsum.photos/id/553/200/200.jpg?hmac=HSLKzqqoxnajv4KjLxYSjZokWcuCCiZLGdRPUoryhXk" alt="Sample"><figcaption>Caption</figcaption></figure> | Groups media + caption for semantic meaning.                                      |
| `<figcaption>` | Adds a **caption** to `<figure>`.    | `<figcaption>This is a caption</figcaption>`                                                     | <figcaption>This is a caption</figcaption>                                                                                                                                 | Should be placed **inside** `<figure>`.                                           |

---

## HTML YouTube Videos

- YouTube will display an `id` (like tgbNymZ7vqY)

```html
<iframe
  width="420"
  height="315"
  src="https://www.youtube.com/embed/tgbNymZ7vqY"
>
</iframe>
```

- `mute=1` after `autoplay=1` to let your video start playing automatically (but muted)

- `controls=0` to not display controls in the video player

- `loop=1` to let your video loop forever

```html
<iframe
  width="420"
  height="315"
  src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1&controls=0&loop=1"
>
</iframe>
```

---

## Block and Inline Elements

### Block-level Elements

- A block-level element `always starts on a new line`
- and `takes up the full width available` (stretches out to the left and right as far as it can).

- Some examples of block-level elements：

  - `<div>`
  - `<h1> - <h6>`
  - `<p>`
  - `<form>`

### Inline Elements

- `does not start on a new line`
- and `only takes up as much width as necessary`

- Some Examples of inline elements：

  - `<span>`
  - `<a>`
  - `<img>`

![block_vs_inline_diagram](./images/block_vs_inline_diagram.png)

---

## HTML Semantic Elements

- Semantic elements `describes the purpose of content inside element` to both the `browser` and the `developer`.

| **Tag**        | **Purpose**                                  | **Example (Code)**                                                     | **How It Displays**                | **Notes / Usage**                                                 |                                                          |
| -------------- | -------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------- | ----------------------------------------------------------------- | -------------------------------------------------------- |
| `<header>`     | Represents the **header** of a page/section. | `<header><h1>Site Title</h1></header>`                                 | Block element (top section).       | Usually contains **logo, nav, or intro content**.                 |                                                          |
| `<nav>`        | Defines **navigation links**.                | \`<nav><a href="/">Home</a>                                            | <a href="/about">About</a></nav>\` | Horizontal/vertical group of links.                               | For **menus & navigation bars**. Improves accessibility. |
| `<section>`    | Groups **related content**.                  | `<section><h2>Features</h2><p>Details...</p></section>`                | Block section.                     | Ideal for **page sections** (e.g., Features, About).              |                                                          |
| `<article>`    | Represents **self-contained content**.       | `<article><h2>Blog Post</h2><p>Content...</p></article>`               | Independent block of content.      | Can be **syndicated** (e.g., blog posts, news).                   |                                                          |
| `<aside>`      | Represents **side content**.                 | `<aside>Related Links</aside>`                                         | Small side block.                  | Used for **ads, sidebars, related content**.                      |                                                          |
| `<footer>`     | Represents the **footer** of page/section.   | `<footer>&copy; 2025 MySite</footer>`                                  | Block element (bottom section).    | Usually contains **copyright, links, contact info**.              |                                                          |
| `<main>`       | Represents the **main content** of a page.   | `<main><h1>Welcome</h1><p>Main content here</p></main>`                | Block element.                     | Only **one `<main>`** per page.                                   |                                                          |
| `<figure>`     | Groups **media + caption**.                  | `<figure><img src="img.jpg"><figcaption>Caption</figcaption></figure>` | Media block with caption.          | For **images, charts, code snippets** with a caption.             |                                                          |
| `<figcaption>` | Adds a **caption** to `<figure>`.            | `<figcaption>Image Caption</figcaption>`                               | Text below or above figure.        | Must be inside `<figure>`.                                        |                                                          |
| `<time>`       | Represents **dates/times**.                  | `<time datetime="2025-07-27">July 27, 2025</time>`                     | Formatted date/time.               | Use `datetime` for machine-readable format (SEO & accessibility). |                                                          |
| `<mark>`       | Highlights **important text**.               | `This is <mark>highlighted</mark>.`                                    | Text with a yellow background.     | Useful for **search highlights** or key points.                   |                                                          |
| `<address>`    | Represents **contact info**.                 | `<address>123 Main St, City</address>`                                 | Block of italicized text.          | For **physical or email contact information**.                    |                                                          |

- `Non-semantic elements` `tells nothing about its content`
- eg. `<div>` and `<span>`

---

## HTML Entities

- `Reserved characters` in HTML must be `replaced with character entities`,as the browser `might mix them with tags`.
- To display a less than sign (`<`) we must write：`&lt;` or `&#60;`
- `Characters that are not present on your keyboard` can also be replaced by entities.

  ```
  &entity_name;

  OR

  &#entity_number;
  ```

![html_entities](./images/html_entities.png)

> `Advantage of using an entity name`：An entity name is `easy to remember`.

> `Disadvantage of using an entity name`： `Browsers may not support all entity names`, but the support for `numbers is good`.

---

## Non-breaking Space

- Another common use of the `non-breaking space` is to prevent that `browsers truncate spaces` in HTML pages.

- If you write `10 spaces` in your text, the browser will `remove 9 of them`. To add real spaces to your text, you can use the `&nbsp;` character entity.

---

## **✅ What is ARIA?**

**ARIA (Accessible Rich Internet Applications)** is a set of **HTML attributes** that improve **accessibility** for users with disabilities (e.g., screen reader users).
It helps **describe roles, states, and properties** of UI elements — especially when building **custom components** (modals, sliders, menus) that don’t have native semantics.

---

### **ARIA Components in Depth**

| **Type**       | **Purpose**                                     | **Example**                                | **Notes / Usage**                                                   |
| -------------- | ----------------------------------------------- | ------------------------------------------ | ------------------------------------------------------------------- |
| **Roles**      | Define **what an element is** (its purpose).    | `<div role="button">Click</div>`           | Adds semantic meaning to non-semantic tags (`div`, `span`).         |
| **States**     | Describe the **current state** of an element.   | `<button aria-pressed="true">On</button>`  | Used for toggles, expanded/collapsed states, active items.          |
| **Properties** | Provide **extra information** about an element. | `<div aria-label="Main Navigation"></div>` | Adds labels, descriptions, relationships for better screen reading. |

---

### **Common ARIA Attributes**

| **Attribute**      | **Purpose**                           | **Example**                                      |
| ------------------ | ------------------------------------- | ------------------------------------------------ |
| `role`             | Defines the element’s role.           | `<div role="dialog">`                            |
| `aria-label`       | Adds a text label for assistive tech. | `<button aria-label="Close Menu">X</button>`     |
| `aria-labelledby`  | Links to another element’s label.     | `<div aria-labelledby="title-id">`               |
| `aria-describedby` | Links to additional descriptive text. | `<div aria-describedby="desc-id">`               |
| `aria-hidden`      | Hides elements from screen readers.   | `<div aria-hidden="true">Hidden</div>`           |
| `aria-checked`     | State for checkboxes/toggles.         | `<input type="checkbox" aria-checked="true">`    |
| `aria-expanded`    | Indicates open/closed state.          | `<button aria-expanded="false">Menu</button>`    |
| `aria-disabled`    | Marks an element as disabled.         | `<button aria-disabled="true">Disabled</button>` |

### 🔎 Tools to Test ARIA

- ✅ **Chrome DevTools > Accessibility tab**
- ✅ **[axe DevTools](https://www.deque.com/axe/devtools/)**
- ✅ **NVDA (Windows)**, **VoiceOver (Mac/iOS)**
- ✅ **WAVE tool** – [https://wave.webaim.org](https://wave.webaim.org)

### 🧠 Summary: ARIA In Depth

| Feature        | Example                       | Use Case                        |
| -------------- | ----------------------------- | ------------------------------- |
| **Roles**      | `role="dialog"`               | What element is                 |
| **Properties** | `aria-label="Close"`          | What label/description it has   |
| **States**     | `aria-expanded="false"`       | What it’s doing now             |
| **Live**       | `aria-live="polite"`          | Auto-updates for screen readers |
| **Pairing**    | With `tabindex`, JS, & events | Required for usable UIs         |

---

## **in-depth checklist of major points** to consider

### ✅ 1. **Semantic HTML First**

Use tags according to their **meaning**, not appearance.

| Bad (non-semantic)      | Good (semantic)         |
| ----------------------- | ----------------------- |
| `<div id="nav">`        | `<nav>`                 |
| `<div class="header">`  | `<header>`              |
| `<div class="content">` | `<main>` or `<section>` |
| `<b>`                   | `<strong>`              |
| `<i>`                   | `<em>`                  |

### ➕ Benefits:

- Better SEO
- Better screen reader support
- Easier for developers to understand

---

### ✅ 2. **Accessibility (a11y) Is Non-Negotiable**

| Best Practice                        | Why It Matters                            |
| ------------------------------------ | ----------------------------------------- |
| Use proper heading order (`h1`–`h6`) | Helps screen readers understand structure |
| Add `alt` to all `<img>` tags        | Describes images for non-visual users     |
| Use `aria-*` attributes when needed  | For custom components                     |
| Label all form fields with `<label>` | Ensures users know what to input          |
| Use semantic roles (`role="button"`) | Required for custom UI elements           |

🔍 Example:

```html
<button aria-label="Close Modal">✖</button>
```

---

### ✅ 3. **Scalable Component Structure**

Follow **BEM** or **utility-first** (e.g., Tailwind) or component-based methodology (e.g., React, Vue):

```html
<div class="card card--highlight">
  <h2 class="card__title">Title</h2>
  <p class="card__description">Text</p>
</div>
```

Use:

- Atomic Design principles
- Reusable UI patterns
- Consistent class naming
- Minimal depth nesting (avoid div hell)

---

### ✅ 4. **SEO Best Practices**

| Element                     | Purpose                                |
| --------------------------- | -------------------------------------- |
| `<title>`                   | Primary title in search results        |
| `<meta name="description">` | Controls search snippet                |
| `<h1>`                      | Main content heading (only one!)       |
| `<a href="...">`            | Must include descriptive anchor text   |
| `<img alt="...">`           | Used in image search and accessibility |

📌 Example:

```html
<meta name="description" content="Best AI Quiz App for Students" />
```

---

### ✅ 5. **Performance-Aware HTML**

- Lazy-load images: `<img loading="lazy" />`
- Use `<picture>` for responsive images
- Avoid large inline SVGs or base64 images
- Minimize DOM nodes
- Use critical CSS/JS inline only above the fold

---

### ✅ 6. **Form Best Practices**

| Feature                         | Why Important                   |
| ------------------------------- | ------------------------------- |
| Use `<label for="">`            | Accessibility and UX            |
| Group fields using `<fieldset>` | Semantic grouping               |
| Use proper input types          | e.g., `email`, `number`, `date` |
| Validation attributes           | `required`, `minlength`, etc.   |
| Don’t disable submit buttons    | Use client-side logic instead   |

```html
<label for="email">Email</label> <input type="email" id="email" required />
```

---

### ✅ 7. **Mobile-First & Responsive Design**

HTML must support responsive CSS:

- Always include viewport meta tag:

```html
<meta name="viewport" content="width=device-width, initial-scale=1" />
```

- Use responsive-friendly layouts:

  - Flexbox, Grid
  - Avoid fixed `px` widths in HTML (prefer `%`, `em`, `rem`)

---

### ✅ 8. **Progressive Enhancement**

Build for the **baseline first**, then add enhancements:

- Your page must work without JavaScript (fallbacks)
- Use `<noscript>` tags where required
- Gracefully degrade animations, interactions, modals

```html
<noscript>Please enable JavaScript to use this feature</noscript>
```

---

### ✅ 9. **HTML5 APIs Awareness**

Use:

- `<dialog>` for modals
- `<details>` + `<summary>` for collapsible sections
- `<output>` for live form results
- `<progress>` and `<meter>` for dynamic indicators

---

### ✅ 10. **Security Best Practices**

| Practice                                 | Why It Matters                      |
| ---------------------------------------- | ----------------------------------- |
| Sanitize user input                      | Prevent XSS                         |
| Avoid inline scripts                     | Hard to manage & insecure           |
| Use `rel="noopener noreferrer"` in links | Prevent tab-nabbing                 |
| Don’t expose sensitive HTML comments     | Protect server logic or credentials |

```html
<a href="..." target="_blank" rel="noopener noreferrer">Link</a>
```

---

### ✅ 11. **Versioned & Maintainable Code**

- Include comments only where it adds value
- Version control via Git
- Group reusable sections with includes (SSG or template engines)
- Use partials or components if using frameworks

---

### ✅ 12. **Integrate with CI/CD and Linters**

- Use [HTMLHint](https://htmlhint.com/)
- Add CI step to check broken links, accessibility (e.g., Lighthouse CLI, pa11y)
- Avoid unclosed tags, nesting errors

---

### ✅ Bonus: Professional Developer Mindset

- **Think long term**: Will this HTML break in 2 years?
- **Minimize assumptions**: Don’t assume everyone has JavaScript or fast internet
- **Prioritize clarity over cleverness**: Readability > 2-line hacks
- **Comment purpose, not obvious HTML**
- **Collaborate with designers** on structure and semantics

---

### 📁 Folder & File Organization (HTML-centric)

```
/project
  ├── index.html
  ├── about.html
  ├── /partials
  │    ├── header.html
  │    ├── footer.html
  ├── /assets
  │    ├── /images
  │    ├── /css
  │    ├── /js
```

---

### 🧠 Summary Checklist

- ✅ Use semantic tags
- ✅ Optimize for accessibility (a11y)
- ✅ Make SEO-friendly structure
- ✅ Write performance-aware markup
- ✅ Design mobile-first
- ✅ Build with maintainability in mind
- ✅ Include fallback for JS-required features
- ✅ Secure and future-proof your HTML
