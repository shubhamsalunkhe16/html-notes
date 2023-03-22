# HTML Tutorial

- stands for `Hyper Text Markup Language`
- used `.htm` or `.html` extention
- `not a programming language`, it is a `markup language`
- uses markup tags to `describe web pages`
- `skeleton` of web content
- `HTML5` is the current version of HTML which is used.
- `case insensitive`. For example, a `<title>` tag could be written as `<title>`, `<TITLE>`, `<Title>`, etc. but `recommends lowercase` in HTML

## HTML Elements

### The three main parts:

- `Opening Tag`: `start` of the element
- `Content`: contents that are `visible` on the browser
- `Closing Tag`: `end` of the element. starts with a backward slash `'/'`

![html element](./images/htmlElement.png)

## Attributes

- provide `additional information` about elements
- always `specified in the start tag`
- usually come in `name/value pairs` like: `name="value"`

### Core Attributes

- 4 core attributes are `id`,`class`,`title`,`style`

### `The Id Attribute`

- used to specify a `unique id` for an HTML element
- used by `CSS` and `JavaScript` to `select and access` specific elements
- case sensitive
- used to create `HTML bookmarks`

```html
<p id="html">This para explains what is HTML</p>
```

### `The class Attribute`

- specifies `one or more` class names for an element
- used by `CSS` and `JavaScript` to `select and access` specific elements
- `case sensitive`
- `Different HTML elements` can point to the `same class name`

```html
<p class="sub-heading bold italic">This para explains what is HTML</p>
...
<p class="sub-heading">This para explains what is HTML</p>
...
<p class="sub-heading">This para explains what is HTML</p>
```

### `The title Attribute`

- displayed as a `tooltip` when cursor comes over the element or while the element is loading

```html
<h3 title="Hello HTML!">Titled Heading Tag Example</h3>
```

### `The Style Attribute`

- used to `add styles` to an element

```html
<tagname style="property:value;">...</tagname>

<body style="background-color:red;font-size:12px">
  ...
</body>
```

![Attribute](./images/htmlAttribute.png)

## Nesting elements

- `elements can contain other elements`

```html
<p>My cat is <strong>very</strong> grumpy.</p>
```

### _wrong way_

```html
<p>My cat is <strong>very grumpy.</p></strong>
```

## Void elements

- elements with `no content`

```html
<img src="images/firefox-icon.png" alt="My test image" />
```

## Block versus inline elements

### Block-level elements

- always takes up the `full width available`
- always `starts on a new line`
- browsers `automatically add some space` (a margin) before and after the element
- eg: `<p>` and `<div>`

### Inline elements

- only takes up as much `width as necessary`
- `does not start on a new line`
- `<span>` element inside a paragraph

`Note:` An inline element cannot contain a block-level element!

## HTML Page Structure

`<!DOCTYPE html>`

- defines doc is an `HTML5` doc

`<html>`

- `wraps all the content` on the entire page
- known as the `root element`

`<head>`

- contains `additional(meta) information about the HTML page`, like the page title
- includes things like `keywords` and a `page description` that you want to appear in search results and for `SEO`

```html
<meta name="keywords" content="HTML, CSS, JavaScript" />
<meta name="description" content="Free Web tutorials" />
<meta name="author" content="John Doe" />
```

- to ensures the page renders at the `width of viewport`, `preventing mobile browsers` from rendering pages wider than the viewport and then `shrinking` them down

```html
<meta name="viewport" content="width=device-width" />
```

- to `refresh document every 30 seconds`

```html
<meta http-equiv="refresh" content="30" />
```

- `CSS` to style our content, character set declarations, and more
- should use to UTF-8 which `includes most characters` from the vast majority of written languages

```html
<meta charset="utf-8" />
```

`<title>`

- specifies a `title for the webpage`,
- which is shown in the `browser's window`

`<body>`

- contains all the `contents of the webpage`

#### `thepizzabox.html` file looks like this.

```html
<html>
  <head>
    <title>The Pizza Box</title>
  </head>
  <body>
    <h1>The Pizza Box</h1>
    <p>Margherita Pizza, 449/-</p>
    <p>Cheeze Burst Pizza, 459/-</p>
    <p>Farm House Pizza, 399/-</p>
  </body>
</html>
```

## Comment `<!-- comment -->`

```html
<!-- this is html comment -->
```

- `browser ignores` comments as it renders the code
- way `to write helpful notes` about your code

## Marking up text

### Headings `<h1> - <h6>`

- `defines` the most important `headings and subheadings`
- contains `6` heading levels, `<h1> - <h6>`

```html
<h1>My main title</h1>
<h2>My top level heading</h2>
<h3>My subheading</h3>
<h4>My sub-subheading</h4>
```

### _output :_

<h1>My main title</h1>
<h2>My top level heading</h2>
<h3>My subheading</h3>
<h4>My sub-subheading</h4>

`Note:`

- `search engines` use the headings to `index` the structure and content of your web pages
- `Don't use` headings `to make text BIG or bold`

## Paragraphs `<p>`

- `regular text content`
- cannot change the display by adding extra spaces or extra lines as `browser will automatically remove extra spaces`

```html
<p>This is a single paragraph</p>
```

- ### _output :_ <p>This is a single paragraph</p>

## HTML Horizontal Rules `<hr>`

- defines a `thematic break`
- `used to separate content`
- ### _output :_ <hr/>

## HTML Line Breaks `<br>`

- used for `line break` (a new line)
- without starting a new paragraph
- ### _output :_
  <br/>
  <br/>

## `<pre>`

- defines `preformatted text`
- displayed in a fixed-width font (usually Courier), and it `preserves both spaces and line breaks`

```html
<pre>
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
</pre>
```

- ### _output :_

<pre style="color:yellow">
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
</pre>

## HTML Formatting Elements

| Element    | Description      |
| ---------- | ---------------- |
| `<b>`      | Bold text        |
| `<strong>` | Important text   |
| `<i>`      | Italic text      |
| `<em>`     | Emphasized text  |
| `<mark>`   | Marked text      |
| `<small>`  | Smaller text     |
| `<del>`    | Deleted text     |
| `<s>`      | Strike text      |
| `<ins>`    | Inserted text    |
| `<u>`      | Underlined text  |
| `<sub>`    | Subscript text   |
| `<sup>`    | Superscript text |

## `<b>`

- defines `bold text`
- `without any extra importance`

```html
<b>This text is bold</b>
```

- ### _output :_
  <b>This text is bold</b>

## `<strong>`

- defines text with `strong importance`
- displayed in bold text

```html
<strong>This text is important!</strong>
```

- ### _output :_
  <strong>This text is important!</strong>

## `<i>`

- used to indicate a `technical term, a phrase from another language, a thought, a ship name`, etc

```html
<i>This text is italic</i>
```

- ### _output :_
  <i>This text is italic</i>

## `<em>`

- defines `emphasized text`
- `screen reader` will pronounce the words in `<em>` with an emphasis, using `verbal stress`

```html
<em>This text is emphasized</em>
```

- ### _output :_
  <em>This text is italic</em>

## `<small>`

- defines `smaller text`

```html
<small>This text is small</small>
```

- ### _output :_
  <small>This text is italic</small>

## `<mark>`

- defines text that should be `marked or highlighted`

```html
<span>Do not forget to buy <mark>milk</mark> today.</span>
```

- ### _output :_
  <span>Do not forget to buy <mark>milk</mark> today.</span>

## `<del>`

- defines `text deleted` from a document
- usually renders in `strike a line` through deleted text

```html
<span>My favorite color is <del>blue</del> red.</span>
```

- ### _output :_
  <span>My favorite color is <del>blue</del> red.</span>

## `<s>`

- renders in `strike a line` through text

```html
<span>My favorite color is <s>blue</s> red.</span>
```

- ### _output :_
  <span>My favorite color is <s>blue</s> red.</span>

## `<ins>`

- defines a `text inserted` into a document
- usually renders in `underline` inserted text

```html
<span>My favorite color is <ins>red</ins>.</span>
```

- ### _output :_
  <span>My favorite color is <ins>red</ins>.</span>

## `<u>`

- renders `underlined` text

```html
<span>My favorite color is <u>red</u>.</span>
```

- ### _output :_
  <span>My favorite color is <u>red</u>.</span>

## `<sub>`

- defines `subscript text`
- subscript text appears `half a character below` the normal line
- used for `chemical formulas`,etc

```html
<span>H<sub>2</sub>0</span>
```

- ### _output :_
  <span>H<sub>2</sub>0</span>

## `<sup>`

- defines `superscript text`
- superscript text appears `half a character above` the normal line
- used for `footnotes`, `math square`,etc

```html
<span>WWW<sup>[1]</sup></span>
```

- ### _output :_
  <span>WWW<sup>[1]</sup></span>

## HTML Quotation and Citation Elements

## `<blockquote>`

- defines a section that is `quoted from another source`
- `cite attribute` defines the `source`
- browsers usually `indent` it

```html
<p>Here is a quote from WWF's website:</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
  For 60 years, WWF has worked to help people and nature thrive. As the world's
  leading conservation organization, WWF works in nearly 100 countries.
</blockquote>
```

- ### _output :_
<p>Here is a quote from WWF's website:</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
For 60 years, WWF has worked to help people and nature thrive. As the world's leading conservation organization, WWF works in nearly 100 countries.
</blockquote>

## `<q>`

- defines a `short quotation`
- browsers normally insert `quotation marks` around the quotation

```html
<span>
  WWF's goal is to:
  <q>Build a future where people live in harmony with nature.</q>
</span>
```

- ### _output :_ <span>WWF's goal is to: <q>Build a future where people live in harmony with nature.</q></span>

## `<abbr>`

- defines an `abbreviation`, like `HTML`, `CSS`, `Mr.`, `Dr.`, `ASAP`, `ATM`,etc
- can give useful information to `browsers`, `translation systems` and `search-engines`

- `Tip`: use `title attribute` to show the description for the abbreviation/acronym when you mouse over the element

```html
<span>
  The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.
</span>
```

- ### _output :_
  <span>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</span>

## `<address>`

- defines the `contact information`
- contact information can be an `email address`, `URL`, `physical address`, `phone number`, `social media handle`, etc
- usually renders in `italic`
- browsers will always `add a line break before and after` the it

```html
<address>
  Written by John Doe.<br />
  Visit us at:<br />
  Example.com<br />
  Box 564, Disneyland<br />
  USA
</address>
```

- ### _output :_
  <address>
  Written by John Doe.<br>
  Visit us at:<br>
  Example.com<br>
  Box 564, Disneyland<br>
  USA
  </address>

## `<cite>`

- defines the `title of a creative work` (e.g. `a book`, `a song`, `a movie`,etc.)
- usually renders in `italic`

`Note`: A person's name is not the title of a work.

```html
<span><cite>The Scream</cite> by Edvard Munch. Painted in 1893.</span>
```

- ### _output :_
  <span><cite>The Scream</cite> by Edvard Munch. Painted in 1893.</span>

## `<bdo>`

- BDO stands for `Bi-Directional Override`.
- used to `override the current text direction`

```html
<bdo dir="rtl">This text will be written from right to left</bdo>
```

- ### _output :_
  <bdo dir="rtl">This text will be written from right to left</bdo>

## HTML Links

- HTML links are `hyperlinks`
- can click on a link and `jump to another document`
- `cursor` will be `pointer`

- `Note:` A link does not have to be text. A link can be an image or any other HTML element!

- Use the `mailto:` scheme inside the `href attribute` to create a `link that opens the user's email` program

```html
<a href="default.asp">
  <img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;" />
</a>

<a href="mailto:someone@example.com">Send email</a>

<a href="https://www.w3schools.com/">Visit W3Schools.com!</a>
```

- ### _output :_
  <a href="https://www.w3schools.com/">Visit W3Schools.com!</a>

### target attribute

- specifies `where to open the linked document`
- can have one of the following values:

  - `_self` - Default. Opens the document in the `same window/tab`
  - `_blank` - Opens the document in a `new window or tab`
  - `_parent` - Opens the document in the `parent frame`
  - `_top` - Opens the document in the `full body of the window`

### By default, links will appear as follows in all browsers

- `unvisited link` => underlined and blue
- `visited link` => underlined and purple
- `active link` => underlined and red

- You can `change the link state colors`, by using CSS:

```html
<style>
  /* unvisited link will be green with no underline. */
  a:link {
    color: green;
    background-color: transparent;
    text-decoration: none;
  }
  /* visited link will be pink with no underline. */
  a:visited {
    color: pink;
    background-color: transparent;
    text-decoration: none;
  }
  /* hover link will become red and underlined */
  a:hover {
    color: red;
    background-color: transparent;
    text-decoration: underline;
  }
  /* active link will be yellow and underlined. */
  a:active {
    color: yellow;
    background-color: transparent;
    text-decoration: underline;
  }
</style>
```

### Create a Bookmark in HTML

- can `jump to specific parts` of a web page
- use the `id` attribute (id="value") to define bookmarks in a page
- use the `href` attribute (href="#value") to link to the bookmark

```html
<h2 id="C4">Chapter 4</h2>
. . .
<a href="#C4">Jump to Chapter 4</a>
```

- You can also add a link to a `bookmark` on another page:

```html
<a href="html_demo.html#C4">Jump to Chapter 4</a>s
```

## HTML Images `<img>`

- used to `embed an image`
- `src` attribute, contains the `path of image file`
- `alt` specify `descriptive text`
  - `screen readers read out` the alt text
  - `on image loading error`, alt text displays

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

## HTML Tables

- consists of table cells inside `rows and columns`

| Element      | Description                                                               |
| ------------ | ------------------------------------------------------------------------- |
| `<table>`    | Defines a table                                                           |
| `<th>`       | Defines a header cell in a table                                          |
| `<tr>`       | Defines a row in a table                                                  |
| `<td>`       | Defines a cell in a table                                                 |
| `<caption>`  | Defines a table caption                                                   |
| `<colgroup>` | Specifies a group of one or more columns in a table for formatting        |
| `<col>`      | Specifies column properties for each column within a `<colgroup>` element |
| `<thead>`    | Groups the header content in a table                                      |
| `<tbody>`    | Groups the body content in a table                                        |
| `<tfoot>`    | Groups the footer content in a table                                      |

- To make a `cell span over multiple columns`, use the `colspan` attribute
- To make a `cell span over multiple rows`, use the `rowspan` attribute
- value of the `rowspan` attribute represents the number of `rows` to span same for `colspan`, number of column
- used to `style specific columns` of a table

```html
<table style="width:100%;">
  <caption>
    Monthly savings
  </caption>
  <colgroup>
    <col span="2" style="background-color: blue" />
    <!-- to style columns in the middle of a table, insert a "empty" <col> element -->
    <!-- <col span="2"> -->
    <col span="1" style="background-color: green" />
    <!-- hide last column -->
    <!-- <col span="1" style="visibility: collapse"> -->
  </colgroup>
  <thead>
    <tr>
      <th colspan="2">Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Jill</td>
      <td>Smith</td>
      <td>50</td>
    </tr>
    <tr>
      <td>Eve</td>
      <td>Jackson</td>
      <td rowspan="2">94</td>
    </tr>
    <tr>
      <td>Eve</td>
      <td>Jackson</td>
    </tr>
  </tbody>
</table>
```

<table style="width:100%;">
  <caption>Monthly savings</caption>
  <colgroup>
    <col span="2" style="background-color: blue">
    <!-- <col span="2"> -->
    <col span="1" style="background-color: green">
    <!-- <col span="1" style="visibility: collapse"> -->
  </colgroup>
  <thead>
   <tr>
    <th colspan="2">Name</th>
    <th>Age</th>
   </tr>
  </thead>
  <tbody>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
      <td>Eve</td>
    <td>Jackson</td>
    <td rowspan="2">94</td>
  </tr>
  <tr>
      <td>Eve</td>
    <td>Jackson</td>
  </tr>
  </tbody>
</table>

## HTML Forms

- used to `collect user input`

### `type="text"`

- defines a `single-line text input` field

### `type="email"`

- used for input fields that should contain an e-mail address

### `type="password"`

- defines a `password field`

### `type="hidden"`

- defines a `hidden input field` (not visible to a user)

- lets web developers `include data that cannot be seen or modified by users` when a form is submitted

### `type="number"`

- defines a `numeric input field`

### `type="submit"`

- defines a button for `submitting form data to a form-handler`
- `form-handler` is typically a `server page with a script for processing input data`
- `form-handler` is specified in the `form's action` attribute

### `type="reset"`

- will `reset all form values` to their default values

```html
<fieldset>
  <legend>Personalia:</legend>
  <form action="/action_page.php">
    <label for="fname">First name:</label><br />
    <input type="text" id="fname" name="fname" /><br />
    <label for="email">Email:</label><br />
    <input type="email" id="email" name="email" /><br />
    <label for="password">Password:</label><br />
    <input type="password" id="password" name="password" /><br />
    <label for="quantity">Quantity (between 1 and 5):</label><br />
    <input
      type="number"
      id="quantity"
      name="quantity"
      min="1"
      max="5"
    /><br /><br />
    <input type="hidden" id="custId" name="custId" value="3487" />
    <input type="submit" value="Submit" />
    <input type="reset" />
  </form>
</fieldset>
```

<fieldset>
<legend>Personalia:</legend>
<form action="/action_page.php">
  <label for="fname">First name:</label><br />
  <input type="text" id="fname" name="fname" /><br />
  <label for="email">Email:</label><br />
  <input type="email" id="email" name="email" /><br />
  <label for="password">Password:</label><br />
  <input type="password" id="password" name="password" /><br />
  <label for="level">Level (between 1 and 5):</label><br/>
  <input type="number" id="level" name="level" min="1" max="5"><br/><br/>
  <input type="hidden" id="custId" name="custId" value="3487" />
  <input type="submit" value="Submit" />
  <input type="reset" />
</form>
</fieldset>

- `<fieldset>` tag is used to group related elements in a form.
- `<fieldset>` tag draws a box around the related elements
- `<legend>` tag is used to define a caption for the `<fieldset>` element.

### `type="radio"`

- defines a `radio button`
- user will select `ONLY ONE` of a limited number of choices
- `name` for all radio input must be `same`

```html
<p>Choose your favorite Web language:</p>

<form>
  <input type="radio" id="html" name="fav_language" value="HTML" />
  <label for="html">HTML</label><br />
  <input type="radio" id="css" name="fav_language" value="CSS" />
  <label for="css">CSS</label><br />
  <input type="radio" id="javascript" name="fav_language" value="JavaScript" />
  <label for="javascript">JavaScript</label>
</form>
```

<p>Choose your favorite Web language:</p>

<form>
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <input type="radio" id="javascript" name="fav_language" value="JavaScript">
  <label for="javascript">JavaScript</label>
</form>

### `type="checkbox"`

- user select `ZERO or MORE options` of a limited number of choices

```html
<form>
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike" />
  <label for="vehicle1"> I have a bike</label><br />
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car" />
  <label for="vehicle2"> I have a car</label><br />
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat" />
  <label for="vehicle3"> I have a boat</label>
</form>
```

<form>
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  <label for="vehicle1"> I have a bike</label><br>
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  <label for="vehicle2"> I have a car</label><br>
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  <label for="vehicle3"> I have a boat</label>
</form>

### `type="file"`

- defines a `file-select field` and a "Browse" button for `file uploads`.

```html
<form>
  <label for="myfile">Select a file:</label>
  <input type="file" id="myfile" name="myfile" />
</form>
```

<form>
  <label for="myfile">Select a file:</label>
  <input type="file" id="myfile" name="myfile">
</form>

### `type="range"`

- control for entering a number whose exact value is not important (like a `slider control`)

```html
<form>
  <label for="vol">Volume (between 0 and 50):</label>
  <input type="range" id="vol" name="vol" min="0" max="50" />
</form>
```

<form>
  <label for="vol">Volume (between 0 and 50):</label>
  <input type="range" id="vol" name="vol" min="0" max="50">
</form>

### `type="search"`

- used for `search fields`

```html
<form>
  <label for="gsearch">Search Google:</label>
  <input type="search" id="gsearch" name="gsearch" />
</form>
```

<form>
  <label for="gsearch">Search Google:</label>
  <input type="search" id="gsearch" name="gsearch">
</form>

### `type="tel"`

- used for input fields that should contain a `telephone number`

```html
<form>
  <label for="phone">Enter your phone number:</label>
  <input
    type="tel"
    id="phone"
    name="phone"
    pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}"
  />
</form>
```

<form>
  <label for="phone">Enter your phone number:</label>
  <input type="tel" id="phone" name="phone" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}">
</form>

### `type="date"`

- used for input fields that should contain a `date`.

```html
<form>
  <label for="birthday">Birthday:</label>
  <input type="date" id="birthday" name="birthday" />
</form>
```

<form>
  <label for="birthday">Birthday:</label>
  <input type="date" id="birthday" name="birthday">
</form>

### `type="time"`

- used for input fields that should contain a `time`.

```html
<form>
  <label for="appt">Select a time:</label>
  <input type="time" id="appt" name="appt" />
</form>
```

<form>
  <label for="appt">Select a time:</label>
  <input type="time" id="appt" name="appt">
</form>

### `type="button"`

- defines a `button`

```html
<input type="button" onclick="alert('Hello World!')" value="Click Me!" />
```

<input type="button" onclick="alert('Hello World!')" value="Click Me!">

### `type="color"`

- used to `select color`

```html
<form>
  <label for="favcolor">Select your favorite color:</label>
  <input type="color" id="favcolor" name="favcolor" />
</form>
```

<form>
  <label for="favcolor">Select your favorite color:</label>
  <input type="color" id="favcolor" name="favcolor">
</form>

### `type="image"`

- defines an `image as a submit button`

```html
<form>
  <input
    type="image"
    src="img_submit.gif"
    alt="Submit"
    width="48"
    height="48"
  />
</form>
```

<form>
<input type="image" src="./images/greenArrow.png" alt="Submit" width="48" height="48">
</form>

### `type="url"`

- used for input fields that should contain a `URL address`

```html
<form>
  <label for="homepage">Add your homepage:</label>
  <input type="url" id="homepage" name="homepage" />
</form>
```

<form>
  <label for="homepage">Add your homepage:</label>
  <input type="url" id="homepage" name="homepage">
</form>

## HTML `<select>` Tag

- Create a `drop-down list`

- `<optgroup>` tag is used to `group related options` in a `<select>` element

- `<option>` tag defines an option in a select list.

```html
<label for="cars">Choose a car:</label>
<select name="cars" id="cars">
  <optgroup label="Swedish Cars">
    <option value="volvo">Volvo</option>
    <option value="saab">Saab</option>
  </optgroup>
  <optgroup label="German Cars">
    <option value="mercedes">Mercedes</option>
    <option value="audi">Audi</option>
  </optgroup>
</select>
```

<label for="cars">Choose a car:</label>
<select name="cars" id="cars">

 <option hidden value="">---Select---</option>
  <optgroup label="Swedish Cars">
    <option value="volvo">Volvo</option>
    <option value="saab">Saab</option>
  </optgroup>
  <optgroup label="German Cars">
    <option value="mercedes">Mercedes</option>
    <option value="audi">Audi</option>
  </optgroup>
</select>

## HTML Input Attributes

### `The value Attribute`

- specifies a `value for an input field`

### `The readonly Attribute`

- specifies that an input field is read-only( `cannot be modified` )

### `The disabled Attribute`

- specifies that an input field should be `disabled`
- it is `unusable` and `un-clickable`

```html
<form>
  <label for="fname">First name:</label><br />
  <input type="text" id="fname" name="fname" value="John" readonly /><br />
  <label for="lname">Last name:</label><br />
  <input type="text" id="lname" name="lname" value="Doe" disabled /><br />
</form>
```

<form>
  <label for="fname">First name:</label><br />
  <input type="text" id="fname" name="fname" value="John" readonly /><br/>
  <label for="lname">Last name:</label><br />
  <input type="text" id="lname" name="lname" value="Doe" disabled /><br/><br/>
</form>

### `The size Attribute`

- specifies the `visible width`, in characters, of an input field
- The default value for size is `20`.
- `Note`: works with : `text`, `search`, `tel`, `url`, `email`, and `password`.

### `The maxlength Attribute`

- specifies the `maximum number of characters allowed` in an input field

### `The min and max Attributes`

- specify the `minimum and maximum values` for an input field
- work with : `number`, `range`, `date`, `datetime-local`, `month`, `time` and `week`

### `The step Attribute`

- specifies the `legal number intervals` for an input field.
- eg: if step="3", legal numbers could be -3, 0, 3, 6, etc.

```html
<form>
  <label for="pin">PIN:</label><br />
  <input type="text" id="pin" name="pin" maxlength="6" size="15" />
  <label for="datemax">Enter a date before 1980-01-01:</label>
  <input type="date" id="datemax" name="datemax" max="1979-12-31" /><br /><br />

  <label for="datemin">Enter a date after 2000-01-01:</label>
  <input type="date" id="datemin" name="datemin" min="2000-01-02" /><br /><br />

  <label for="quantity">Quantity (between 0 and 10):</label>
  <input type="number" id="quantity" name="quantity" min="0" max="5" step="2" />
</form>
```

<form>
<label for="pin">PIN:</label><br />
<input type="text" id="pin" name="pin" maxlength="6" size="15" /><br />
<label for="datemax">Enter a date before 1980-01-01:</label><br />
<input type="date" id="datemax" name="datemax" max="1979-12-31" /><br />
<label for="datemin">Enter a date after 2000-01-01:</label><br />
<input type="date" id="datemin" name="datemin" min="2000-01-02" /><br />
<label for="quantity">Quantity (between 0 and 10):</label><br />
<input type="number" id="quantity" name="quantity" min="0" max="10" step="2" />

</form>

### `The autofocus Attribute`

- specifies that an input field should `automatically get focus` when the page loads

### `The autocomplete Attribute`

- specifies whether a form or an `input field should have autocomplete on or off`

### `The required Attribute`

- specifies that an input field `must be filled out before submitting` the form
- works with: `text`, `search`, `url`, `tel`, `email`, `password`, `date pickers`, `number`, `checkbox`, `radio`, and `file`

### `The placeholder Attribute`

- specifies a `short hint` that describes the expected value of an input field

```html
<form>
  <label for="fname">First name:</label><br />
  <input
    placeholder="name"
    type="text"
    id="fname"
    name="fname"
    autofocus
    autocomplete="off"
    required
  /><br />
</form>
```

<form>
  <label for="fname">First name:</label><br />
  <input
    type="text"
    id="fname"
    name="fname"
    autofocus
    autocomplete="off"
    required
  /><br />
</form>

### `The multiple Attribute`

- specifies that the user is `allowed to enter more than one value` in an input field
- works with : `email`, and `file`

```html
<form>
  <label for="files">Select files:</label>
  <input type="file" id="files" name="files" multiple />
</form>
```

<form>
  <label for="files">Select files:</label>
  <input type="file" id="files" name="files" multiple>
</form>

### `The pattern Attribute`

- specifies a regular expression that the input field's value is checked against, when the form is submitted.
- works with : `text`, `date`, `search`, `url`, `tel`, `email`, and `password`.

```html
<form>
  <label for="country_code">Country code:</label>
  <input
    type="text"
    id="country_code"
    name="country_code"
    pattern="[A-Za-z]{3}"
    title="Three letter country code"
  />
</form>
```

## HTML Input form Attributes

### `formaction Attribute`

- formaction attribute specifies the `URL of the file that will process the input` when the form is submitted

### `The formenctype Attribute`

- specifies how the `form-data should be encoded` when submitted (only for forms with `method="post"`).

```html
<form action="/action_page_binary.asp" method="post">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname" /><br /><br />
  <input type="submit" value="Submit" />
  <input
    type="submit"
    formenctype="multipart/form-data"
    value="Submit as Multipart/form-data"
  />
</form>
```

<form action="/action_page_binary.asp" method="post">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname" /><br /><br />
  <input type="submit" value="Submit" />
  <input
    type="submit"
    formenctype="multipart/form-data"
    value="Submit as Multipart/form-data"
  />
</form>

### `formmethod Attribute`

- defines the `HTTP method` for sending form-data to the action URL
- eg `method="get/post"`

## HTML Iframe

- used to `embed another document` within the `current HTML document`

```html
<iframe src="url" title="description"></iframe>
```

- `title` attribute used by `screen readers` to read out what the content of the iframe is

## HTML Computer Code Elements

### `<kbd>`

- used to define `keyboard input`

```html
<p>Save the document by pressing <kbd>Ctrl + S</kbd></p>
```

### _output :_

<p>Save the document by pressing <kbd>Ctrl + S</kbd></p>

### `<samp>`

- used to define `sample output from a computer program`

```html
<p>Message from my computer:</p>
<p>
  <samp>File not found.<br />Press F1 to continue</samp>
</p>
```

### _output :_

<p>Message from my computer:</p>
<p><samp>File not found.<br>Press F1 to continue</samp></p>

### `<code>`

- used to define a piece of `computer code`

```html
<code> x = 5; y = 6; z = x + y; </code>
```

### _output :_

<code>
x = 5;
y = 6;
z = x + y;
</code>

### `Notice`:

- `does not preserve extra whitespace and line-breaks`
- `to fix`,
<pre>
<code>
x = 5;
y = 6;
z = x + y;
</code>
</pre>

### HTML <var> For Variables

- used to define a `variable in programming` or in a `mathematical expression`
- displayed in `italic`

```html
<p>
  The area of a triangle is: 1/2 x <var>b</var> x <var>h</var>, where
  <var>b</var> is the base, and <var>h</var> is the vertical height.
</p>
```

### _output :_

<p>The area of a triangle is: 1/2 x <var>b</var> x <var>h</var>, where <var>b</var> is the base, and <var>h</var> is the vertical height.</p>

## HTML Semantic Elements

- `Semantic elements = elements with a meaning`
- `describes its meaning` to both the `browser` and the `developer`
- eg `non-semantic elements`: `<div>` and `<span>` - Tells nothing about its content.

- eg `semantic elements`: `<form>`, `<table>`, and `<article>` - Clearly defines its content

| Element        | Description                                                                                |
| -------------- | ------------------------------------------------------------------------------------------ |
| `<article>`    | Defines independent, self-contained content                                                |
| `<aside>`      | Defines content aside from the page content text                                           |
| `<details>`    | Defines additional details that the user can view or hide text                             |
| `<figure>`     | Specifies self-contained content, like illustrations, diagrams, photos, code listings, etc |
| `<figcaption>` | Defines a caption for a `<figure>` element text                                            |
| `<footer>`     | Defines a footer for a document or section                                                 |
| `<header>`     | Specifies a header for a document or section                                               |
| `<main>`       | Specifies the main content of a document                                                   |
| `<mark>`       | Defines marked/highlighted text                                                            |
| `<nav>`        | Defines navigation links                                                                   |
| `<section>`    | Defines a section in a document                                                            |
| `<summary>`    | Defines a visible heading for a `<details>` element                                        |
| `<time>`       | Defines a date/time                                                                        |

## HTML `<details>` and `<summary>` Elements

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

## HTML `<figure>` and `<figcaption>` Elements

```html
<figure>
  <img src="pic_trulli.jpg" alt="Trulli" />
  <figcaption>Fig1. - Trulli, Puglia, Italy.</figcaption>
</figure>
```

## HTML `<time>` Elements

```html
<p>I have a date on <time datetime="2008-02-14 20:00">Valentines day</time>.</p>
```

### _output:_

<p>I have a date on <time datetime="2008-02-14 20:00">Valentines day</time>.</p>

## HTML Entities

- Some characters are `reserved` in HTML.
- If you use the `less than (<)` or `greater than (>)` signs in your text, the browser `might mix` them with tags.
- `Character entities` are used to display reserved characters in HTML.

```
&entity_name;
OR
&#entity_number;
```

- To display `<` : `&lt;` or `&#60;`

## HTML Symbol Entities

- Many `mathematical`, `technical`, and `currency symbols`, are not present on a normal keyboard
- used to display it

```
<p>I will display &#8364;</p>
<p>I will display &#x20AC;</p>
<p>
&#128512; &#128516; &#128525; &#128151;
</p>
```

### _output:_

<p>I will display &#8364;</p>
<p>I will display &#x20AC;</p>
<p>
&#128512; &#128516; &#128525; &#128151;
</p>

## HTML Multimedia

- Only `MP3`, `WAV`, and `Ogg` audio are supported by the HTML standard
- Only `MP4`, `WebM`, and `Ogg` video are supported by the HTML standard.
- The `<source>` element allows you to `specify alternative video files` which the browser may choose from
- The browser will use the `first recognized format`

```html
<audio controls autoplay muted>
  <source src="horse.ogg" type="audio/ogg" />
  <source src="horse.mp3" type="audio/mpeg" />
  Your browser does not support the audio element.
</audio>

<video width="320" height="240" autoplay muted>
  <source src="movie.mp4" type="video/mp4" />
  <source src="movie.ogg" type="video/ogg" />
  Your browser does not support the video tag.
</video>
```

- [audio and video methods reference](https://www.w3schools.com/tags/ref_av_dom.asp)

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

## HTML Geolocation API

- used to get the `geographical position` of a user
- Since this can compromise `privacy`, the position is not available unless the `user approves` it
- `getCurrentPosition()` method is used to return the user's position.

```html
<script>
  function getLocation() {
    if (navigator.geolocation) {
      navigator.geolocation.getCurrentPosition(onSuccess, onError);
    } else {
      console.log("Geolocation is not supported by this browser.");
    }
  }

  function onSuccess(position) {
    console.log(
      "Latitude: " +
        position.coords.latitude +
        "Longitude: " +
        position.coords.longitude
    );
  }

  function onError(error) {
    console.log(error);
  }
</script>
```

- `watchPosition()` - Returns the `current position of the user and continues to return updated position as the user moves` (like the GPS in a car)
- clearWatch() - `Stops the watchPosition()` method

## HTML Colors

- specified with `predefined color names`, `RGB`, `HEX`, `HSL`, `RGBA`, or `HSLA` values

### RGB and RGBA Colors

- RGB (red, green, blue) defines the `intensity of the color`
- `value range  0 and 255`. eg. `rgb(255, 99, 71)`
- `RGBA` is RGB with an `Alpha channel (opacity)`,eg. `rgb(255, 99, 71,0.5)`

**Shades of Gray**

- defined using equal values for all three parameters
- `rgb(60, 60, 60)`, `rgb(100, 100, 100)` , `rgb(200, 200, 200)`

### HTML HEX Colors

- `hexadecimal color` is specified with: `#RRGGBB`
- `values between 00 and ff`, eg. `#ff6347`

**Shades of Gray**

- defined using equal values for all three parameters
- `#404040`, `#a0a0a0`, `#dcdcdc`

### HTML HSL and HSLA Colors

- HSL - `hue, saturation, and lightness`
- HSLA - `HSL with an Alpha channel (opacity)`
- `Hue is a degree on the color wheel from 0 to 360`. `0 is red`, `120 is green`, and `240 is blue`
- `Saturation is a percentage value`. `0% is shade of gray`, and `100% is full color`
- `Lightness is also a percentage value`. `0% is black`, and `100% is white`
- `hsl(0, 100%, 50%)`,`hsl(0, 60%, 50%,0.2)`

**Shades of Gray**

- defined by setting the `hue and saturation to 0`, and adjusting the `lightness from 0% to 100%` to get darker/lighter shades
- `hsl(0, 0%, 60%)`, `hsl(0, 0%, 20%)`
