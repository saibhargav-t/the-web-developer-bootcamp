# HTML Elements Glossary

## Document Metadata

* `<html>`: The root element of an HTML document.
* `<head>`: Contains machine-readable information (metadata) about the document, like its title, scripts, and style sheets.
* `<title>`: Defines the document's title that is shown in a browser's title bar or a page's tab.
* `<meta>`: Represents metadata that cannot be represented by other HTML meta-related elements, like `<base>`, `<link>`, `<script>`, `<style>` or `<title>`.
* `<link>`: Specifies relationships between the current document and an external resource (commonly used for CSS).
* `<style>`: Contains style information for a document, or part of a document.
* `<base>`: Specifies the base URL to use for all relative URLs in a document.

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

## Sectioning & Semantic

* `<body>`: Represents the content of an HTML document. There can be only one `<body>` element in a document.
* `<header>`: Represents introductory content, typically a group of introductory or navigational aids.
* `<footer>`: Represents a footer for its nearest sectioning content or sectioning root element.
* `<nav>`: Represents a section of a page whose purpose is to provide navigation links.
* `<main>`: Represents the dominant content of the `<body>` of a document.
* `<article>`: Represents a self-contained composition in a document, page, application, or site.
* `<section>`: Represents a generic standalone section of a document, which doesn't have a more specific semantic element to represent it.
* `<aside>`: Represents a portion of a document whose content is only indirectly related to the document's main content.
* `<h1>`–`<h6>`: Represent six levels of section headings. `<h1>` is the highest section level and `<h6>` is the lowest.
* `<address>`: Indicates that the enclosed HTML provides contact information for a person or people, or for an organization.

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
* `<hr>`: Represents a thematic break between paragraph-level elements.
* `<pre>`: Represents preformatted text which is to be presented exactly as written in the HTML file.
* `<blockquote>`: Indicates that the enclosed text is an extended quotation.
* `<ol>`: Represents an ordered list of items (typically rendered as a numbered list).
* `<ul>`: Represents an unordered list of items (typically rendered as a bulleted list).
* `<li>`: Represents an item in a list.
* `<dl>`: Represents a description list.
* `<dt>`: Specifies a term in a description list.
* `<dd>`: Provides the description, definition, or value for the preceding term (`<dt>`) in a description list (`<dl>`).
* `<div>`: The generic container for flow content. It has no effect on the content or layout until styled in some way using CSS.
* `<span>`: A generic inline container for phrasing content, which does not inherently represent anything.

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

* `<a>`: Creates a hyperlink to web pages, files, email addresses, locations in the same page, or anything else a URL can address.
* `<strong>`: Indicates that its contents have strong importance, seriousness, or urgency (usually bold).
* `<em>`: Marks text that has stress emphasis (usually italics).
* `<br>`: Produces a line break in text (carriage-return).
* `<code>`: Displays its contents styled in a fashion intended to indicate that the text is a short fragment of computer code.
* `<abbr>`: Represents an abbreviation or acronym.
* `<bdi>`: Tells the browser's bidirectional algorithm to treat the text it contains in isolation from its surrounding text.
* `<bdo>`: Overrides the current text directionality.
* `<cite>`: Represents a reference to a creative work.
* `<data>`: Links a given piece of content with a machine-readable translation.
* `<dfn>`: Represents the defining instance of a term.
* `<kbd>`: Represents a span of inline text denoting textual user input from a keyboard, voice input, or any other text entry device.
* `<mark>`: Represents text which is marked or highlighted for reference or notation purposes.
* `<q>`: Indicates that the enclosed text is a short inline quotation.
* `<small>`: Represents side-comments and small print.
* `<sub>`: Specifies inline text which should be displayed as subscript for solely typographical reasons.
* `<sup>`: Specifies inline text which is to be displayed as superscript for solely typographical reasons.
* `<time>`: Represents a specific period in time.
* `<u>`: Represents a span of inline text which should be rendered in a way that indicates that it has a non-textual annotation.
* `<wbr>`: Represents a word break opportunity.

**Example:**

```html
<p>This is a <a href="#">link</a>.</p>
<p><strong>Bold</strong> and <em>italic</em> text.</p>
<p>This is a line<br>break.</p>
<p><code>&lt;code&gt;</code> example.</p>
<p><abbr title="Abbreviation">Abbr.</abbr></p>
<p><cite>The Scream</cite> by Edward Munch.</p>
<p>You can find more information in <dfn>HTML</dfn>.</p>
<p>Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.</p>
<p>This text is <mark>highlighted</mark>.</p>
<p>This is a <q>short quote</q>.</p>
```

## Image & Multimedia

* `<img>`: Embeds an image into the document.
* `<audio>`: Used to embed sound content in documents.
* `<video>`: Used to embed video content in a document.
* `<figure>`: Represents self-contained content, potentially with an optional caption, which is specified using the `<figcaption>` element.
* `<figcaption>`: Represents a caption or legend for the rest of the content of its parent `<figure>` element.
* `<area>`: Defines an area inside an image map that has predefined clickable areas.
* `<map>`: Used with `<area>` elements to define an image map.
* `<track>`: Used as a child of the media elements, `<audio>` and `<video>`. It lets you specify timed text tracks.
* `<embed>`: Embeds external content at the specified point in the document.
* `<iframe>`: Represents a nested browsing context, embedding another HTML page into the current one.
* `<object>`: Represents an external resource, which can be treated as an image, a nested browsing context, or content to be handled by a plugin.
* `<picture>`: Contains zero or more `<source>` elements and one `<img>` element to offer alternative versions of an image for different display/device scenarios.
* `<source>`: Specifies multiple media resources for the `<picture>`, the `<audio>` element, or the `<video>` element.

**Example:**

```html
<img src="image.jpg" alt="My Image">
<audio controls src="audio.mp3"></audio>
<video controls src="video.mp4"></video>
<figure>
  <img src="image.jpg" alt="My Image">
  <figcaption>Fig.1 - My Image.</figcaption>
</figure>
<map name="infographic">
  <area shape="rect" coords="34,44,270,350" href="https://developer.mozilla.org/">
</map>
<iframe src="https://www.example.com"></iframe>
```

## Table

* `<table>`: Represents tabular data — that is, information presented in a two-dimensional table comprised of rows and columns.
* `<caption>`: Specifies the caption (or title) of a table.
* `<thead>`: Defines a set of rows defining the head of the columns of the table.
* `<tbody>`: Encapsulates a set of rows corresponding to the body of the table.
* `<tfoot>`: Defines a set of rows summarizing the columns of the table.
* `<tr>`: Defines a row of cells in a table.
* `<th>`: Defines a cell as a header of a group of table cells.
* `<td>`: Defines a cell of a table that contains data.
* `<colgroup>`: Defines a group of columns within a table.
* `<col>`: Defines a column within a table and is used for defining common semantics on all common cells.

**Example:**

```html
<table>
  <caption>My Table</caption>
  <colgroup>
    <col span="2" style="background-color:red">
    <col style="background-color:yellow">
  </colgroup>
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
  </tbody>
</table>
```

## Forms

* `<form>`: Represents a document section containing interactive controls for submitting information.
* `<input>`: Used to create interactive controls for web-based forms in order to accept data from the user.
* `<button>`: An interactive element activated by a user with a mouse, keyboard, finger, voice command, or other assistive technology.
* `<select>`: Represents a control that provides a menu of options.
* `<option>`: Used to define an item contained in a `<select>`, an `<optgroup>`, or a `<datalist>` element.
* `<textarea>`: Represents a multi-line plain-text editing control.
* `<label>`: Represents a caption for an item in a user interface.
* `<fieldset>`: Used to group several controls as well as labels within a web form.
* `<legend>`: Represents a caption for the content of its parent `<fieldset>`.
* `<datalist>`: Contains a set of `<option>` elements that represent the permissible or recommended options available to choose from within other controls.
* `<optgroup>`: Creates a grouping of options within a `<select>` element.
* `<output>`: A container element into which a site or app can inject the results of a calculation or the outcome of a user action.
* `<progress>`: Displays an indicator showing the completion progress of a task, typically displayed as a progress bar.
* `<meter>`: Represents either a scalar value within a known range or a fractional value.

**Example:**

```html
<form>
  <fieldset>
    <legend>User Information</legend>
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">
    <br>
    <label for="email">Email:</label>
    <input type="email" id="email" name="email">
    <br>
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
    <br>
    <input list="browsers" name="browser" id="browser">
    <datalist id="browsers">
      <option value="Edge">
      <option value="Firefox">
      <option value="Chrome">
      <option value="Opera">
      <option value="Safari">
    </datalist>
    <br>
    <progress value="70" max="100">70 %</progress>
    <br>
    <meter value="2" min="0" max="10">2 out of 10</meter>
    <br>
    <button type="submit">Submit</button>
  </fieldset>
</form>
```
