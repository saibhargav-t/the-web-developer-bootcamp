# HTML Elements Glossary

This document provides a comprehensive glossary of common HTML elements, their uses, and best practices.

## Document Metadata

* `<html>`: The root element of an HTML document.
* `<head>`: Contains machine-readable information (metadata) about the document, like its title, scripts, and style sheets.
* `<title>`: Defines the document's title that is shown in a browser's title bar or a page's tab.
* `<meta>`: Represents metadata that cannot be represented by other HTML meta-related elements.
  * **Common Attributes:** `charset`, `name`, `content`.
* `<link>`: Specifies relationships between the current document and an external resource.
  * **Common Attributes:** `href`, `rel` (e.g., `stylesheet`), `type`.
* `<style>`: Contains style information for a document, or part of a document.
* `<base>`: Specifies the base URL to use for all relative URLs in a document.
  * **Common Attributes:** `href`, `target`.

**Example:**

```html
<!DOCTYPE html>
<html>
<head>
  <title>Document Metadata Example</title>
  <meta charset="UTF-8">
  <meta name="description" content="Free Web tutorials">
  <link rel="stylesheet" href="styles.css">
  <style>
    body {
      background-color: lightblue;
    }
  </style>
</head>
<body>
  <p>This is a paragraph.</p>
</body>
</html>
```

## Scripting

* `<script>`: Used to embed or reference executable JavaScript code. It can be placed in the `<head>` or `<body>`.
  * **Common Attributes:**
    * `src`: Specifies the URL of an external script file.
    * `async`: (For external scripts) The script is executed asynchronously with the rest of the page.
    * `defer`: (For external scripts) The script is executed when the page has finished parsing.
* `<noscript>`: Defines a section of HTML to be inserted if a script type on the page is unsupported or if scripting is turned off in the browser.

## Global Attributes: `id` and `class`

The `id` and `class` attributes are "global," meaning they can be used on almost any HTML element. They are essential for applying CSS styles and for JavaScript manipulation.

* **The `id` Attribute:**
  * Provides a **unique** identifier for an element. No two elements in an HTML document should have the same `id`.
  * Used to target a specific element with CSS (`#my-id`) or JavaScript.
  * Can be used as a link anchor (e.g., `href="#my-unique-id"`).

* **The `class` Attribute:**
  * Specifies one or more class names for an element.
  * Used to group elements that share the same styling or behavior.
  * Multiple elements can share the same class.
  * A single element can have multiple classes, separated by spaces.

**Example:**

```html
<style>
  /* Target a single element by its unique ID */
  #main-header {
    background-color: navy;
    color: white;
  }

  /* Target all elements with the 'highlight' class */
  .highlight {
    background-color: yellow;
    font-weight: bold;
  }

  /* Target elements with the 'text-large' class */
  .text-large {
    font-size: 1.2em;
  }
</style>

<!-- 'id' is unique to this h1 -->
<h1 id="main-header">My Website</h1>

<!-- 'class' can be used on multiple elements -->
<p class="highlight">This paragraph is important.</p>
<p>This is a normal paragraph.</p>
<p>
  This sentence contains a <span class="highlight">highlighted word</span>.
</p>

<!-- This element has two classes -->
<p class="highlight text-large">This is a large, highlighted paragraph.</p>
```

## Block-level vs. Inline Elements

In HTML, most elements are either "block-level" or "inline" elements. Understanding the difference is crucial for CSS styling.

* **Block-level Elements:** These elements occupy the full width available to them and start on a new line. They can contain other block-level and inline elements.
  * **Examples:** `<div>`, `<p>`, `<h1>`–`<h6>`, `<form>`, `<ul>`, `<ol>`, `<li>`, `<header>`, `<footer>`, `<section>`.

* **Inline Elements:** These elements only occupy as much width as necessary and do not start on a new line. They are typically used for styling text or parts of text within a block-level element.
  * **Examples:** `<span>`, `<a>`, `<img>`, `<strong>`, `<em>`, `<code>`, `<input>`, `<button>`, `<label>`.

**Example:**

```html
<div style="background-color: lightgray;">This is a block-level div.</div>
<p style="background-color: lightblue;">This is a block-level paragraph.</p>
<span style="background-color: yellow;">This is an inline span.</span>
<a href="#" style="background-color: lightgreen;">This is an inline link.</a>
<span>Another inline span.</span>
```

## Sectioning & Semantic

* `<body>`: Represents the content of an HTML document.
* `<header>`: Represents introductory content, typically a group of introductory or navigational aids.
* `<footer>`: Represents a footer for its nearest sectioning content.
* `<nav>`: Represents a section of a page whose purpose is to provide navigation links.
* `<main>`: Represents the dominant content of the `<body>` of a document.
* `<article>`: Represents a self-contained composition (e.g., a blog post, forum post).
* `<section>`: Represents a generic standalone section of a document.
* `<aside>`: Represents content only indirectly related to the document's main content (e.g., a sidebar).
* `<h1>`–`<h6>`: Represent six levels of section headings. `<h1>` is the highest and `<h6>` is the lowest.
* `<address>`: Provides contact information for a person, people, or an organization.

**Example:**

```html
<body>
  <header>
    <h1>Main Title</h1>
    <nav>
      <a href="/">Home</a>
    </nav>
  </header>
  <main>
    <article>
      <h2>Article Title</h2>
      <p>This is an article.</p>
    </article>
  </main>
  <footer>
    <address>
      Contact us at <a href="mailto:example@example.com">example@example.com</a>
    </address>
  </footer>
</body>
```

## Text Content

* `<p>`: Represents a paragraph.
* `<hr>`: Represents a thematic break between paragraph-level elements (e.g., a horizontal rule).
* `<pre>`: Represents preformatted text, preserving spaces and line breaks.
* `<blockquote>`: Indicates that the enclosed text is an extended quotation.
* `<ol>`: Represents an ordered list of items (numbered).
* `<ul>`: Represents an unordered list of items (bulleted).
* `<li>`: Represents an item in a list.
* `<dl>`: Represents a description list.
* `<dt>`: Specifies a term in a description list.
* `<dd>`: Provides the description for the preceding term (`<dt>`).
* `<div>`: The generic container for flow content. It has no semantic meaning.
* `<span>`: A generic inline container for phrasing content, with no semantic meaning.

**Example:**

```html
<p>This is a paragraph.</p>
<hr>
<pre>
  This is
  preformatted text.
</pre>
<blockquote>
  This is a blockquote.
</blockquote>
<ol>
  <li>First item</li>
  <li>Second item</li>
</ol>
<ul>
  <li>Bullet item</li>
</ul>
<dl>
  <dt>Term</dt>
  <dd>Description</dd>
</dl>
```

## Inline Text Semantics

* `<a>`: Creates a hyperlink.
  * **Common Attributes:** `href`, `target` (`_blank`, `_self`), `rel`, `download`.
* `<strong>`: Indicates strong importance, seriousness, or urgency (usually bold).
* `<em>`: Marks text with stress emphasis (usually italics).
* `<br>`: Produces a line break in text.
* `<code>`: Indicates a short fragment of computer code.
* `<abbr>`: Represents an abbreviation or acronym. The `title` attribute can be used to provide the full expansion.
* `<cite>`: Represents a reference to a creative work.
* `<kbd>`: Represents user input from a keyboard.
* `<mark>`: Represents text which is marked or highlighted.
* `<q>`: Indicates a short inline quotation.
* `<small>`: Represents side-comments and small print.
* `<sub>`: Specifies subscript text.
* `<sup>`: Specifies superscript text.
* `<time>`: Represents a specific period in time. The `datetime` attribute can be used for machine-readable formats.
* `<u>`: Represents text with a non-textual annotation, like a misspelling (often rendered with an underline).

**Example:**

```html
<p>This is a <a href="#">link</a>.</p>
<p><strong>Bold</strong> and <em>italic</em> text.</p>
<p>This is a line<br>break.</p>
<p><code>&lt;code&gt;</code> example.</p>
<p><abbr title="Abbreviation">Abbr.</abbr></p>
<p><cite>The Scream</cite> by Edward Munch.</p>
<p>Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.</p>
<p>This text is <mark>highlighted</mark>.</p>
<p>This is a <q>short quote</q>.</p>
```

## Image & Multimedia

* `<img>`: Embeds an image. It is an empty element.
  * **Common Attributes:** `src` (required), `alt` (required for accessibility), `width`, `height`.
* `<audio>`: Embeds sound content.
  * **Common Attributes:** `src`, `controls`, `autoplay`, `loop`, `muted`.
* `<video>`: Embeds video content.
  * **Common Attributes:** `src`, `controls`, `autoplay`, `loop`, `muted`, `poster`.
* `<figure>`: Represents self-contained content, like an image, diagram, or code snippet.
* `<figcaption>`: Represents a caption for a `<figure>`.
* `<iframe>`: Represents a nested browsing context, embedding another HTML page.
  * **Common Attributes:** `src`, `width`, `height`, `frameborder`.
* `<canvas>`: Used with JavaScript to draw graphics on the fly.

**Example:**

```html
<img src="image.jpg" alt="My Image">
<audio controls src="audio.mp3"></audio>
<video controls src="video.mp4"></video>
<figure>
  <img src="image.jpg" alt="My Image">
  <figcaption>Fig.1 - My Image.</figcaption>
</figure>
<iframe src="https://www.example.com" width="600" height="400"></iframe>
```

## Table

* `<table>`: Represents tabular data.
* `<caption>`: Specifies the caption (or title) of a table.
* `<thead>`: Defines a set of rows defining the head of the columns.
* `<tbody>`: Encapsulates a set of rows corresponding to the body of the table.
* `<tfoot>`: Defines a set of rows summarizing the columns of the table.
* `<tr>`: Defines a row of cells.
* `<th>`: Defines a header cell.
* `<td>`: Defines a data cell.
* `<colgroup>`: Defines a group of columns within a table.
* `<col>`: Defines a column within a table for styling.

**Example:**

```html
<table>
  <caption>My Table</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John</td>
      <td>25</td>
    </tr>
    <tr>
      <td>Jane</td>
      <td>30</td>
    </tr>
  </tbody>
</table>
```

## Forms

* `<form>`: Represents a section containing interactive controls for submitting information.
  * **Common Attributes:** `action`, `method`, `enctype`, `novalidate`.
* `<input>`: Used to create interactive controls for web-based forms in order to accept data from the user.
* `<button>`: An interactive element activated by a user. It is more flexible than `<input>` of type button.
  * **Type Attribute:**
    * `submit`: (Default) Submits the form data to the server.
    * `reset`: Resets all controls to their initial values.
    * `button`: Has no default behavior. Its actions are typically controlled by JavaScript.
  * **Other Common Attributes:** `name`, `value`, `disabled`, `autofocus`.
* `<select>`: Represents a control that provides a menu of options.
* `<option>`: Used to define an item contained in a `<select>`, an `<optgroup>`, or a `<datalist>` element.
* `<textarea>`: Represents a multi-line plain-text editing control.
  * **Common Attributes:** `rows`, `cols`, `name`, `placeholder`, `required`, `disabled`, `readonly`, `maxlength`.
* `<label>`: Represents a caption for an item in a user interface.
* `<fieldset>`: Used to group several controls as well as labels within a web form.
* `<legend>`: Represents a caption for the content of its parent `<fieldset>`.
* `<datalist>`: Contains a set of `<option>` elements that represent the permissible or recommended options available to choose from within other controls.
* `<optgroup>`: Creates a grouping of options within a `<select>` element.
* `<output>`: A container element into which a site or app can inject the results of a calculation or the outcome of a user action.
* `<progress>`: Displays an indicator showing the completion progress of a task, typically displayed as a progress bar.
* `<meter>`: Represents either a scalar value within a known range or a fractional value.

### Input Types

The `<input>` tag's `type` attribute can be one of many values:

* `text`: A single-line text field.
* `password`: A single-line text field whose value is obscured.
* `checkbox`: A checkbox.
* `radio`: A radio button (part of a group with the same `name`).
* `submit`: A button that submits the form.
* `button`: A clickable button (often used with JavaScript).
* `file`: A control for selecting a file.
* `date`: A control for entering a date.
* `number`: A control for entering a number.
* `email`: A field for an email address with validation.
* `color`: A control for specifying a color.
* `range`: A slider control for a number within a range.
* `hidden`: An input that is not visible to the user but whose value is submitted with the form.
* `reset`: A button that resets the form to its initial values.
* `search`: A text field designed for search queries.
* `tel`: A field for a telephone number.
* `url`: A field for a URL with validation.

### Common Input Attributes

These attributes are used with `<input>` elements to control their behavior and validation.

* `name`: The name of the control, which is submitted with the form data.
* `value`: The initial value of the control.
* `placeholder`: Hint text that appears in the input field when it is empty.
* `required`: Specifies that the user must fill in a value before submitting.
* `disabled`: Disables the input field, preventing user interaction.
* `readonly`: The input field cannot be changed, but its value is still submitted.
* `id`: A unique identifier for the element, used by `<label>` or JavaScript.
* `maxlength`: The maximum number of characters allowed.
* `min` & `max`: The minimum and maximum values (for `number`, `range`, `date` types).
* `step`: The legal number intervals (for `number`, `range` types).
* `autofocus`: Automatically gives focus to the input field when the page loads.
* `checked`: For `radio` and `checkbox` types, specifies that the element should be pre-selected.

**Form Example:**

```html
<form action="/submit-form" method="post">
  <fieldset>
    <legend>Personal Information</legend>
    <label for="name">Name:</label>
    <input type="text" id="name" name="user_name" placeholder="John Doe" required>
    <br>
    <label for="email">Email:</label>
    <input type="email" id="email" name="user_email" required>
    <br>
    <label for="password">Password:</label>
    <input type="password" id="password" name="user_password" minlength="8" required>
    <br>
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">Male</label>
    <input type="radio" id="female" name="gender" value="female">
    <label for="female">Female</label>
    <br>
    <input type="checkbox" id="subscribe" name="subscribe" value="yes" checked>
    <label for="subscribe">Subscribe to newsletter</label>
    <br>
    <button type="submit">Submit</button>
  </fieldset>
</form>
```

## Interactive Elements

* `<details>`: Creates a disclosure widget in which information is only visible when the widget is toggled into an "open" state.
* `<summary>`: Specifies a summary, caption, or legend for a `<details>` element's disclosure box.
* `<dialog>`: Represents a dialog box or other interactive component, such as a dismissible alert, inspector, or subwindow.

**Example:**

```html
<details>
  <summary>Click for details</summary>
  <p>More information is available here.</p>
</details>

<dialog id="myDialog">
  <p>This is a dialog window.</p>
  <button onclick="document.getElementById('myDialog').close()">Close</button>
</dialog>
<button onclick="document.getElementById('myDialog').showModal()">Show Dialog</button>
```

## HTML Best Practices

1. **Use Semantic HTML:** Use elements like `<header>`, `<footer>`, `<article>`, and `<nav>` to describe your content's structure. This improves accessibility and SEO. Avoid using `<div>` for everything (a phenomenon known as "divitis").
2. **Validate Your HTML:** Use tools like the W3C Markup Validation Service to check for errors in your code.
3. **Provide `alt` Attributes for Images:** Always include a descriptive `alt` attribute for `<img>` tags. This is crucial for screen readers and is displayed if the image fails to load.
4. **Use Labels for Form Inputs:** Connect every form control with a `<label>` using the `for` and `id` attributes. This improves usability and accessibility.
5. **Keep Code Clean and Readable:** Use consistent indentation and formatting. Add comments (`<!-- comment -->`) to explain complex or non-obvious parts of your markup.
6. **Close All Tags:** While some tags are self-closing (e.g., `<img>`, `<br>`), make sure to properly close all container tags (e.g., `<div></div>`, `<p></p>`).
7. **Use Lowercase:** Conventionally, HTML tags and attributes are written in lowercase.
8. **Specify Character Encoding:** Always declare your character encoding in the `<head>` using `<meta charset="UTF-8">`. This prevents issues with special characters.
9. **Avoid Inline Styles:** Keep your content (HTML) separate from your presentation (CSS). Use external stylesheets instead of the `style` attribute whenever possible.
