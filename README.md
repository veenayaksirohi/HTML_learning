# HTML Tags Notes

## Table of Contents
- [Introduction](#introduction)
- [Basic Structure Tags](#basic-structure-tags)
- [Text Formatting Tags](#text-formatting-tags)
- [Sectioning Tags](#sectioning-tags)
- [Link and Navigation Tags](#link-and-navigation-tags)
- [List Tags](#list-tags)
- [Table Tags](#table-tags)
- [Image Tag](#image-tag)
- [Other Tags](#other-tags)
- [Accessibility Tips](#accessibility-tips)
- [Common Mistakes](#common-mistakes)
- [References](#references)

---

## Introduction
This document provides notes and examples for the main HTML tags used in this project. Understanding these tags will help you structure and style your web pages effectively. Good HTML structure improves accessibility, SEO, and maintainability.

---

## Basic Structure Tags
- `<!DOCTYPE html>`: Declares the document type and version of HTML. Always place this at the very top of your HTML files.
- `<html>`: The root element of an HTML page. Use the `lang` attribute for language (e.g., `<html lang="en">`).
- `<head>`: Contains meta-information about the document (e.g., `<meta>`, `<title>`, `<style>`, `<link>` for CSS, `<script>` for JS).
- `<body>`: Contains the visible content of the web page.

**Example:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Content here -->
</body>
</html>
```
**Best Practices:**
- Always include `<meta charset="UTF-8">` for character encoding.
- Use `<meta name="viewport" content="width=device-width, initial-scale=1.0">` for responsive design.

---

## Text Formatting Tags
- `<h1>` to `<h6>`: Headings, from most to least important. Use only one `<h1>` per page for the main title.
- `<p>`: Paragraph. Use for blocks of text.
- `<b>`: Bold text (stylistic, not semantic). Prefer `<strong>` for importance.
- `<strong>`: Important text (semantic bold). Screen readers emphasize this.
- `<i>`: Italic text (stylistic). Prefer `<em>` for emphasis.
- `<em>`: Emphasized text (semantic italic).
- `<sub>`: Subscript text (e.g., H<sub>2</sub>O).
- `<sup>`: Superscript text (e.g., x<sup>2</sup>).
- `<del>`: Deleted (strikethrough) text.
- `<mark>`: Marked or highlighted text.
- `<br>`: Line break. Use sparingly; prefer CSS for spacing.
- `<pre>`: Preformatted text (preserves whitespace and line breaks).

**Example:**
```html
<h1>Main Heading</h1>
<h2>Subheading</h2>
<p>This is a <strong>very important</strong> word and <em>emphasized</em> text.</p>
<p>H<sub>2</sub>O and E = mc<sup>2</sup></p>
<pre>
  line1
  line2
</pre>
<mark>Highlight this text</mark>
<del>Old text</del>
```
**Tips:**
- Use headings in order (do not skip levels).
- Use semantic tags (`<strong>`, `<em>`) for meaning, not just appearance.

---

## Sectioning Tags
- `<header>`: Introductory content or navigation links. Usually at the top of the page or section.
- `<nav>`: Navigation links. Use for menus, table of contents, etc.
- `<main>`: Main content of the document. Only one `<main>` per page.
- `<section>`: Thematic grouping of content. Use headings inside sections.
- `<article>`: Self-contained content (e.g., blog post, news article).
- `<aside>`: Content tangentially related to the main content (e.g., sidebar, callout).
- `<footer>`: Footer for a section or page. Use for copyright, contact info, etc.
- `<address>`: Contact information.

**Example:**
```html
<header>
  <h1>Site Title</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
  </nav>
</header>
<main>
  <section>
    <h2>About</h2>
    <p>Some info here.</p>
  </section>
  <aside>
    <p>Related links or ads here.</p>
  </aside>
</main>
<footer>
  <address>Contact us at ...</address>
  <p>&copy; 2024 Your Name</p>
</footer>
```
**Best Practices:**
- Use semantic tags for better accessibility and SEO.
- Only one `<main>` per page.
- Use `<section>` for logical groupings, each with a heading.

---

## Link and Navigation Tags
- `<a>`: Anchor (hyperlink) tag. Use `href` for the link destination. Use `target="_blank"` to open in a new tab (add `rel="noopener noreferrer"` for security).

**Example:**
```html
<a href="https://www.example.com" target="_blank" rel="noopener noreferrer">Visit Example</a>
<a href="#section1">Jump to Section 1</a>
```
**Tips:**
- Always use descriptive link text (avoid "click here").
- For internal page links, use `#id` and match with an element's `id` attribute.

---

## List Tags
- `<ul>`: Unordered (bulleted) list.
- `<ol>`: Ordered (numbered) list.
- `<li>`: List item. Can be nested.
- `<dl>`: Description list.
- `<dt>`: Term in a description list.
- `<dd>`: Description in a description list.

**Example:**
```html
<ul>
  <li>Item 1</li>
  <li>Item 2
    <ul>
      <li>Subitem 2.1</li>
    </ul>
  </li>
</ul>
<ol>
  <li>First</li>
  <li>Second</li>
</ol>
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
</dl>
```
**Best Practices:**
- Use lists for navigation, steps, or grouped data.
- Nest lists for sub-items.

---

## Table Tags
- `<table>`: Table container.
- `<caption>`: Table caption/title.
- `<thead>`: Table header group.
- `<tbody>`: Table body group.
- `<tfoot>`: Table footer group.
- `<tr>`: Table row.
- `<th>`: Table header cell (use for headings, not data).
- `<td>`: Table data cell.

**Example:**
```html
<table>
  <caption>Country Codes</caption>
  <thead>
    <tr>
      <th>Country</th>
      <th>Code</th>
      <th>Email</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>India</td>
      <td>+91</td>
      <td>example@email.com</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="3">End of table</td>
    </tr>
  </tfoot>
</table>
```
**Tips:**
- Use `<th>` for headers, `<td>` for data.
- Add `<caption>` for accessibility.
- Use `<thead>`, `<tbody>`, and `<tfoot>` for complex tables.

---

## Image Tag
- `<img>`: Embeds an image. Use `src` for the image URL, `alt` for alternative text, and optionally `width`/`height`.

**Example:**
```html
<img src="https://example.com/image.jpg" alt="Description of image" width="200" height="200">
```
**Best Practices:**
- Always provide meaningful `alt` text for accessibility and SEO.
- Use relative paths for local images, absolute URLs for remote images.
- Use CSS for advanced image styling.

---

## Other Tags
- `<style>`: Embeds CSS styles in the document. Prefer external CSS for large projects.
- `<meta>`: Metadata about the HTML document (e.g., character set, viewport, description).
- `<title>`: Title of the document (shown in browser tab).
- `<script>`: Embeds or links to JavaScript.
- `<link>`: Links to external resources (e.g., CSS files).

**Example:**
```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="A sample HTML page.">
  <title>Sample Page</title>
  <link rel="stylesheet" href="styles.css">
  <script src="script.js"></script>
</head>
```

---

## Accessibility Tips
- Use semantic HTML tags for structure (e.g., `<header>`, `<nav>`, `<main>`, `<footer>`).
- Always provide `alt` text for images.
- Use headings in order and do not skip levels.
- Ensure sufficient color contrast between text and background.
- Use labels for form elements.
- Use descriptive link text.
- Test your site with a screen reader.

**Resources:**
- [MDN Accessibility](https://developer.mozilla.org/en-US/docs/Learn/Accessibility)
- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)

---

## Common Mistakes
- Missing or incorrect `<!DOCTYPE html>` declaration.
- Not using semantic tags (using `<div>` everywhere).
- Missing `alt` attributes on images.
- Skipping heading levels (e.g., `<h1>` to `<h3>`).
- Using inline styles instead of CSS.
- Using non-descriptive link text (e.g., "click here").
- Forgetting to close tags.
- Invalid nesting of elements (e.g., `<a>` inside `<a>`).

**How to Avoid:**
- Validate your HTML with [W3C Validator](https://validator.w3.org/).
- Follow best practices from [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML).
- Review your code for accessibility and structure.

---

## References
- [MDN: Structuring documents](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)
- [GitHub Markdown HTML tags](https://gist.github.com/seanh/13a93686bf4c2cb16e658b3cf96807f2)
- [How to write a great README](https://github.com/gAmadorH/make-a-great-readme)
- [How to write a README in Markdown](https://github.com/amarpan/how-to-write-a-README)
