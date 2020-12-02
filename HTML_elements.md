# HTML Element Reference

See [MDN's HTML elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
See [Native Forms Elements Demo](http://nativeformelements.com/)

## Table of Contents

<!-- toc -->

- [Document](#document)
- [Text](#text)
- [Embedded Content](#embedded-content)
- [Scripting](#scripting)
- [Lists](#lists)
- [Forms](#forms)
- [Tables](#tables)
- [Data & code](#data--code)
- [Meaningless (non-semantic) elements](#meaningless-non-semantic-elements)
- [Often misused elements](#often-misused-elements)
- [Links](#links)
- [Attributes](#attributes)
  * [Datetime](#datetime)

<!-- tocstop -->

## Document

**`<!DOCTYPE html>`**  
This declaration must be the very first thing in the HTML doc, before the `<html>` element. Technically not an element; it is an instruction to the web browser about what version of HTML the page is written in.

**`<html>`**  
Tells the browser that this is an HTML document. It represents the root of the document and is the container for all other HTML elements (except for the `<!DOCTYPE>`).

**`<title>`**  
Shown in the browser tab & search results. Should be unique for every page on the site.

**`<meta>`**  
The `<meta>` element provides metadata about the HTML document. Metadata will not be displayed on the page, but will be machine parseable.

**`<link>`**  
For linking CSS and other resources. The `rel` attribute indicates the type of resource.

**`<style>`**  
Used to define style information in an HTML document. Consider attaching a stylesheet instead.

**`<script>`**  
Used to define a client-side script (JavaScript).

**`<noscript>`**  
Defines alternate content for users that have disabled scripts in their browser or have a browser that doesn't support scripts. Can be used in both `<head>` and `<body>`. When used inside the `<head>`: `<noscript>` must contain only `<link>`, `<style>`, and `<meta>` elements. The content inside the `<noscript>` element will be displayed if scripts are not supported, or are disabled in the user's browser.

**`<body>`**  
The `<body>` element contains all the contents of an HTML document.

**`<header>`**  
Represents a container for introductory content or a set of navigational links. It typically contains: one or more heading elements, logo or icon, authorship information. You can have several `<header>` elements in one document. An element like `<article>` should have its own header. Note: A `<header>` cannot be placed within a `<footer>`, `<address>` or another `<header>` element.

**`<main>`**  
Primary content of the page.

**`<footer>`**  
When inside `<body>` it’s the website footer. An element like `<article>` should have its own footer.
Typically contains information about its section, such as who wrote it, links to related documents, copyright data, and the like. Can also contain entire sections representing appendices, indexes, long colophons, verbose license agreements, and other such content.

**`<nav>`**  
Defines a group a navigation links.

```html
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#">About</a></li>
        <li><a href="#">Store</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <h1>Example.co</h1>
  </main>

  <footer>
    <p>© 2018 Example.co</p>
  </footer>
</body>
```

**`<article>`**  
Represents a complete, or self-contained, composition in a document, page, application, or site. This could be a news story, technical article, essay, report, a blog post, comment or other social media post. A general rule is that the `<article>` element is appropriate only if the contents would be listed explicitly in the document’s outline. Each article should be identified, typically by including a heading. An article is independent, self-contained content. It should make sense on its own and it should be possible to distribute it independently from the rest of the site.

When article elements are nested, the inner article elements represent articles that are in principle related to the contents of the outer article. For instance, a blog entry on a site could consist of summaries of other blog entries in article elements nested within the article element for the blog entry.

**`<section>`**  
The `<section>` element represents a generic section of a document or application. A section, in this context, is a thematic grouping of content. Each section should be identified, typically by including a heading. Examples of sections would be chapters, the tabbed sections in a dialog box, or the numbered sections of a thesis. A Web site’s home page could be split into sections for an introduction, news items, and contact information.

Like articles, a general rule is that the section element is appropriate only if the element’s contents would be listed explicitly in the document’s outline. Authors are encouraged to use the article element instead of the section element when the content is a complete, or self-contained, composition.

**`<aside>`**  
The `<aside>` element defines some content aside from the content it is placed in. In other words, the aside content should be related to the surrounding content. It can be used for typographical effects like pull quotes or sidebars, for advertising, for groups of nav elements, and for other content that is considered separate from the main content.

**`<details>`**  
The `<details>` element specifies additional information that the user can view or hide on demand. It can be used to create an interactive widget that the user can open and close. Any sort of content can be put inside the `<details>` element. The content should not be visible unless the open attribute is set.

**`<summary>`**  
Defines a visible heading for the `<details>` element. The heading can be clicked to view/hide the details.

```html
<details>
  <summary>System Requirements...</summary>
  <p>Requires a minimum of...</p>
  <p>Blah blah blah, etc, an so on...</p>
</details>
```

**`<dialog>`**  
The `<dialog>` element represents a part of an application that a user interacts with to perform a task, for example a dialog box, inspector, or window.


## Text

**`<a>`**  
For making hyperlinks. The `href` attribute contains the path.

```html
<a href="https://developer.mozilla.org/" target="_blank" rel="noopener noreferrer">example</a>
```
The `rel` attribute of anchor tag specifies the relationship between the current document/web page and the linked web page/document. You can enter a space-separated list of [link types](https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types).

The `noopener` type is useful when opening untrusted links, in order to ensure they cannot tamper with the originating document via the `Window.opener` property.

**`<h1>`**  
The topmost heading in a page or article. On the home page this should be the site’s name. On inside pages this should be the page title.

**`<h2>, <h3>, <h4>, <h5>, <h6>`**  
Content headings, each a sub-heading of the one above.

**`<p>`**  
A generic paragraph of text.

**`<blockquote>`**  
A large, stand alone quote from another source (optionally with a citation which must be within a `footer` or `cite` element).

**`<cite>`**  
A citation for another source, often used with quotations. A person’s name, a URL, a book, a movie title, etc.

```html
<blockquote>
  <p>Dinosaurs may be extinct from the face of the planet, but they are alive and well in our imaginations.</p>
  <footer>— <cite>Steve Miller</cite></footer>
</blockquote>
```

**`<q>`**  
A small inline quote embedded within other content.

**`<em>`**  
A string of emphasized, slightly more important text. Screen readers will change their voice for this text.

**`<strong>`**  
A string of highly emphasized, much more important text. Screen readers will change their voice for this text.

**`<ins>`**  
Content that was inserted after the document was published. The `datetime` attribute defines when it was added.

**`<del>`**  
Content that was deleted after the document was published. The `datetime` attribute defines when it was removed.

```html
<p>Launchpad 39A owned by <del datetime="2014-04-14">NASA</del> <ins datetime="2014-04-14">SpaceX</ins></p>
```

**`<abbr>`**  
An acronym or abbreviation, like *HTML*, *CSS*, etc. The `title` attribute contains the expanded version, like “Hypertext Markup Language”.

**`<dfn>`**  
Represents the defining instance of a term in HTML. The defining instance is often the first use of a term in a document. The nearest parent of the `<dfn>` element must also contain the definition/explanation for the term inside `<dfn>`.

```html
<p><dfn>HTML</dfn> is the standard markup language for creating web pages.</p>
```

**`<mark>`**  
Used to highlight a piece of text for reference. The keywords in a search results page, the current navigation item.

**`<i>`**  
Defines a span of text in an alternate voice or mood. A technical term, a ship name, a book title, a thought, sarcasm, another language. Terms in languages different from the main text should be annotated with lang attributes:

```html
<i lang="fr">je ne sais quoi</i>
```

**`<b>`**  
Defines a span of text to which attention is being drawn for utilitarian purposes like a keyword, a product name in a review, a lead sentence in a paragraph, actionable words in interactive text-driven software. There is no implication of an alternate voice or mood with this element.

**`<s>`**  
Once deprecated this element is now back to represent text that is no longer correct, accurate or relevant. Use the `<del>` element to define replaced or deleted text.

**`<u>`**  
Represents some text that should be stylistically different from normal text, such as misspelled words or proper nouns in Chinese.  Avoid using the `<u>` element where it could be confused for a hyperlink.
The HTML 5 specification reminds developers that other elements are almost always more appropriate than `<u>`.

**`<small>`**  
Represents side comments and fine print.

**`<address>`**  
Contact information, email, tel, postal address, etc.

```html
<address>
  Jet Propulsion Laboratory
  <br>4800 Oak Grove Drive
  <br>Pasadena, California
  <br>91109
</address>
```


## Embedded Content

**`<img>`**  
Embeds an image that’s important to the content. The `src` attribute is the path to the image file.
The `alt` attribute describes the image if it cannot be seen.

**`<map>`**  
Used to define a client-side image-map. An image-map is an image with clickable areas. The required name attribute of the `<map>` element is associated with the `<img>` `usemap` attribute and creates a relationship between the image and the map. The `<map>` element contains a number of `<area>` elements, that define the clickable areas in the image map.

**`<area>`**  
Defines an area inside an image-map. The `<area>` element is always nested inside a `<map>`.

**`<figure>`**  
Embeds annotated images, illustrations, photos, code, etc. Could be moved out of place and would still make sense.

**`<figcaption>`**  
For adding a caption/annotation to the `<figure>`. Must be inside a `<figure>` element—cannot stand alone.

```html
<figure>
  <img src="images/dino-small.jpg" alt="">
  <figcaption>So many dinosaurs I can’t even count!</figcaption>
</figure>
```

**`<picture>`**  
The `<picture>` element gives web developers more flexibility in specifying image resources. The most common use is in responsive designs. Instead of having one image that is scaled up or down based on the viewport width, multiple images can be designed to better fill the browser viewport. See [W3schools](https://www.w3schools.com/tags/tag_picture.asp).

**`<source>`**  
Must be inside `<picture>`, `<video>` or `<audio>` to define the different versions of content.
For example, in video it gives paths to the MP4 and WEBM formats.

```html
<picture>
  <source media="(min-width: 650px)" srcset="img/cat-wide.jpg">
  <source media="(min-width: 450px)" srcset="img/cat-square.jpg">
  <img src="img/cat-small.jpg" alt="A fuzzy kitty." style="width:auto;">
</picture>
```

**`<video>`**  
For embedding movies into a website, for example: `<video poster="" autoplay loop muted controls>`.  
`poster` is the path to an image that’s displayed before the video plays.  
`autoplay` will hint the video to start automatically.  
`loop` triggers whether the video should repeat or not.  
`muted` can be added to not play sound by default.  
`controls` shows or hides the browser’s player buttons.  

**`<audio>`**  
For embedding sounds into a website, for example: `<audio autoplay loop muted controls>`.
`autoplay` will hint the audio to start automatically.  
`loop` triggers whether the audio should repeat or not.  
`muted` can be added to not play sound by default.  
`controls` shows or hides the browser’s player buttons.  

**`<track>`**  
Specifies text tracks for media elements (<audio> and <video>). It's used to specify subtitles, caption files or other files containing text, that should be visible when the media is playing.

```html
<video width="320" height="240" controls>
  <source src="forrest_gump.mp4" type="video/mp4">
  <source src="forrest_gump.ogg" type="video/ogg">
  <track src="subtitles_en.vtt" kind="subtitles" srclang="en" label="English">
  <track src="subtitles_no.vtt" kind="subtitles" srclang="no" label="Norwegian">
</video>
```

**`<iframe>`**  
The `<iframe>` element specifies an inline frame which is used to embed another HTML document within the current HTML document. Primarily used to include resources from other domains or subdomains but can be used to include content from the same domain as well. The `<iframe>`'s strength is that the embedded code is 'live' and can communicate with the parent document.

**`<embed>`**  
The `<embed>` element defines a container for an external application or interactive content (typically non-HTML). It's used to embed content for browser plugins. Exceptions to this are SVG and HTML that are handled differently according to the standard.

**`<object>`**  
The `<object>` element defines an embedded multimedia object (like SVG animations, audio, video, Java applets, ActiveX, PDF, and Flash). You can also use the <object> element to embed another webpage into your HTML document. You can use the <param> element to pass parameters to plugins that have been embedded with the <object> element.

> Note: `<embed>`, `<object>` and `<iframe>` are confusingly similar in functionality... plus you have the fairly new `<video>` and `<audio>`. Think/research before choosing.

**`<param>`**  
Used to define parameters for plugins embedded with an `<object>` element.

**`<svg>`**  
The `<svg>` element defines a container for SVG graphics. For more information see [W3schools SVG Tutorial](https://www.w3schools.com/graphics/svg_intro.asp)


## Scripting

**`<template>`**  
The template element is used to declare fragments of HTML that can be cloned and inserted in the document by script. The `<template>` element holds its content hidden from the client. The content can be visible and rendered later by using JavaScript. Use the `<template>` element when you have HTML code you want to use over and over again, but not until you ask for it.

**`<canvas>`**  
The `<canvas>` element is used to draw graphics, on the fly, via scripting (usually JavaScript). The `<canvas>` element is only a container for graphics, you use a script to actually draw the graphics.


## Lists

**`<ul>`**  
An unordered list—the order of items isn’t important.
Can only have `<li>` elements as direct children.

**`<ol>`**  
An ordered list—the order of the items is important.
Could be alphabetical, numerical, etc.
Can only have `<li>` elements as direct children.

**`<li>`**  
A single list item.
Must be inside a `<ul>` or `<ol>`.
Can have most other elements inside it.

**`<dl>`**  
A description list—a grouping of terms and definitions.
Words & definitions, titles & summaries, data points, etc.
Can only have `<dt>` and `<dd>` elements as direct children.

**`<dt>`**  
Description title, the term of the item.
Must come before the `<dd>`.

**`<dd>`**  
Description definition, the data, or text of the item.
Can be multiple `<dd>` elementss underneath one `<dt>`.

```html
<dl>
  <dt>Length</dt>
  <dd>2.3 m</dd>
  <dt>Weight</dt>
  <dd>4 tonnes</dd>
</dl>
```


## Forms

**`<form>`**  
The `<form>` element defines a form that is used to collect user input. It is used as a parent container to hold form fields.

**`<input>`**  
`<input>` elements are used within a `<form>` element to declare input controls that allow users to input data. An input field can vary in many ways, depending on the `type` attribute and various other attributes.

For example:

```html
<!-- define an input element as a number with min, max and steps -->
<input title="Scale of 1-10" placeholder="1-10" type="number" min="0" max="10" step="0.1" name="num_input" required>

<!-- define an input as email (will validate for correct format) -->
<input title="Enter your email" placeholder="Email Address" type="email" name="email_input" required>
```

**`<label>`**  
Defines a label for an `<input>` element.

**`<output>`**  
The `<output>` element represents the result of a calculation (like one performed by a script).

**`<textarea>`**  
Defines a multi-line text input.

**`<fieldset>`**  
The `<fieldset>` element is used to group related elements in a form under a common name. The name of the group is given by the first legend element that is a child of the `<fieldset>` element. The `<fieldset>` element draws a box around the related elements.

**`<legend>`**  
Defines a caption for the `<fieldset>` element.

```html
<form>
 <fieldset>
   <legend>Personalia:</legend>
   Name: <input type="text"><br>
   Email: <input type="text"><br>
   Date of birth: <input type="text">
 </fieldset>
</form>
```

**`<datalist>`**  
The `<datalist>` element specifies a list of pre-defined options for an `<input>` element. The `<datalist>` element is used to provide an autocomplete feature on `<input>` elements. Users will see a drop-down list of pre-defined options as they input data. Use the `<input>` element's `list` attribute to bind it together with a `<datalist>` element:

```html
<input list="browsers">

<datalist id="browsers">
 <option value="Internet Explorer">
 <option value="Firefox">
 <option value="Chrome">
 <option value="Opera">
 <option value="Safari">
</datalist>
```

**`<select>`**  
Used to create a drop-down list.

**`<option>`**  
Defines an option in a select list.

**`<optgroup>`**  
Used to group related options in a select list.

```html
<select>
 <optgroup label="Swedish Cars">
   <option value="volvo">Volvo</option>
   <option value="saab">Saab</option>
 </optgroup>
 <optgroup label="German Cars">
   <option value="mercedes">Mercedes</option>
   <option value="audi">Audi</option>
 </optgroup>
</select>
````

## Tables

**`<table>`**  
Defines an HTML table. An HTML table consists of the `<table>` element and one or more `<tr>`, `<th>`, and `<td>` elements. A more complex HTML table may also include `<caption>`, `<col>`, `<colgroup>`, `<thead>`, `<tfoot>`, and `<tbody>` elements.

**`<caption>`**  
Defines a table caption. The `<caption>` element must be inserted immediately after the `<table>` element.

**`<colgroup>`**  
Specifies a group of one or more columns in a table for formatting. The `<colgroup>` element is useful for applying styles to entire columns, instead of repeating the styles for each cell, for each row.

Note: The `<colgroup>` element must be a child of a `<table>` element, after any `<caption>` elements and before any `<thead>`, `<tbody>`, `<tfoot>`, and `<tr>` elements.

**`<col>`**  
Specifies column properties for each column within a `<colgroup>` element. The `<col>` element is useful for applying styles to entire columns, instead of repeating the styles for each cell, for each row.

**`<thead>`, `<tbody>`, `<tfoot>`**  
These elements are used together to specify each part of a table (body, header, footer). Browsers can use these elements to enable scrolling of the table body independently of the header and footer. Also, when printing a large table that spans multiple pages, these elements can enable the table header and footer to be printed at the top and bottom of each page. The `<tbody>` element must be a child of a `<table>` element, and come after any `<caption>`, `<colgroup>`, and `<thead>` elements.

**`<tr>`, `<th>`, `<td>`**  
Defines a table row `<tr>`, a header cell `<th>`, a standard data cell `<td>`**  

```html
<table>
  <caption>Monthly savings</caption>
  <colgroup>
    <col span="2" style="background-color:white">
    <col style="background-color:red">
  </colgroup>
  <thead>
    <tr>
      <th>Month</th>
      <th>Savings</th>
      <th>Other</th>
    </tr>
  </thead>
  <tbody>
   <tr>
     <td>January</td>
     <td>$100</td>
     <td>$10</td>
    </tr>
    <tr>
      <td>February</td>
      <td>$80</td>
      <td>$10</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Sum</td>
      <td>$180</td>
      <td>$20</td>
    </tr>
  </tfoot>
</table>
```

## Data & code

**`<sub>`**  
Defines text as being subscript.

**`<sup>`**  
Defines text as being superscript.

**`<var>`**  
Represents a variable in math or programming.

**`<time>`**  
Marks some text as a time or date. The `datetime` attribute defines the machine readable version.

```html
Apollo 11 landed on the moon <time datetime="1969-07-20T20:18">July 20, 1969</time>
```

**`<data>`**  
Marks elements as being a numerical piece of information. The `value` attribute provides the machine readable version.

```html
Argentinosaurus weighted approximately <data value="90">90 tonnes</data>
```

**`<meter>`**  
Represents a single number in a range of numbers, for example: `<meter value="" min="" max="">`.  
`value` is the current number.  
`min` is the minimum number.  
`max` is the maximum number.  

**`<progress>`**  
Represents the current position in a series of steps, for example: `<progress value="" min="" max="">`.  
`value` is the current position.  
`min` is the minimum position.  
`max` is the maximum position.  

**`<code>`**  
Defines a piece of text as a code sample.

**`<pre>`**  
A piece of text that has a specific formatting, where tabs, whitespaces, etc. should be maintained.

**`<kbd>`**  
Defines keyboard input; something a user should type into their computer.

**`<samp>`**  
The `<samp>` element is a phrase element. It defines sample output from a computer program.


## Meaningless (non-semantic) elements

**`<div>`**  
Defines a division or a section in an HTML document. The`<div>` element is often used as a container for other HTML elements to style them with CSS or to perform certain tasks with JavaScript.

**`<span>`**  
Used to group inline-elements in a document. The `<span>` element provides no visual change by itself but provides a way to add a hook to a part of a text.


## Often misused elements

**`<br>`**  
Creates a line break that’s significant to the content.
Useful in poems and addresses where the division of lines is important.
Do not use to create space in a design—use margins and padding.

**`<hr>`**  
Represents a thematic break in the content.
For example, a scene change or topic change.
Do not use to create a horizontal line—use CSS borders.

**`<button>`**  
Represents a interactive, clickable button.
Can be used in forms instead of `<input type="button">`. Unlike `input`, the button can wrap around other elements (`<img>` for example).
Do not use to link to another page—use the `<a>` element.

**`<wbr>`**  
Presents an opportunity for the browser to add a line-break if necessary. This could be in the middle of a long word, title or sentence.


## Links

Links that go nowhere:
```html
<a href="#">Nowhere</a>
```

Links on the same page:
```html
<a href="#herbivores">See the herbivores</a>

<h2 id="herbivores">Herbivores</h2>
```

Links to other files:
```html
<a href="herbivores/stegosaurus.html">Stegosaurus</a>
```

Links to other websites (always start with `https://` or less ideally `http://`):
```html
<a href="https://www.wikipedia.org/">Wikipedia</a>

<!-- Adding `rel="external"` for outward-bound sites is good -->
<a href="https://www.wikipedia.org/" rel="external">Wikipedia</a>
```

Links to phone numbers (start with tel:, use international format):
```html
<a href="tel:+18005551234">Call Me!</a>
```
Send a text message with sms:
```html
<a href="sms:+18005551234&body=Text%20me%20please">Text Me!</a>

<!-- or without a default number -->
<a href="sms:&body=Text%20me%20please">Text Me!</a>
```

Links to email addresses:
```html
<a href="mailto:hello@example.co">Thomas</a>

<!-- Add a subject too -->
<a href="mailto:hello@example.co?subject=How%20are%20you?">Thomas</a>

<!-- Even a default body -->
<a href="mailto:hello@example.co?subject=How%20are%20you?&body=Hey%20Thomas">Thomas</a>
```

## Attributes

See [MDN's HTML attribute reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes).

### Datetime

The following formats apply to the `datetime=""` attribute of the `<time>`, `<del>` & `<ins>` elements.

**Year**

Format: `YYYY`  
Example: `1963`

**Year, month**

Format: `YYYY-MM`  
Example: `1963-11`  
Nov. 1963

**Year, month, day**

Format: `YYYY-MM-DD`  
Example: `1963-11-23`  
Nov. 23, 1963  

**Year, week**

Format: `YYYY-Wdd`  
Example: `1963-W47`  
1936, the week of Nov. 18–24  

**Hour, minute**

Format: `HH:MM`  
Example: `17:16`  
5:16 PM  

**Hour, minute, second**

Format: `HH:MM:SS`  
Example: `17:16:20`  
5:16:20 PM  

**Hour, minute, second, millisecond**

Format: `HH:MM:SS.sss`  
Example: `17:16:20.258`  
5:16:20.258 PM  

**UTC timezone**

Format: `Z`  
Example: `Z`  
UTC timezone  

**Timezone offsets**

Format: `±HH:MM`  
Example: `-05:00`  
Eastern Standard Time, Daylight Savings  

**Year, month, day, hour, minute**

Format: `YYYY-MM-DDTHH:MM`  
Example: `1963-11-23T17:16`  
Nov. 23, `1963 at 5:16 PM`  

**Year, month, day, hour, minute, second**

Format: `YYYY-MM-DDTHH:MM:SS`  
Example: `1963-11-23T17:16:20`  
Nov. 23, 1963 at 5:16:20 PM  

**Year, month, day, hour, minute, second, millisecond**

Format: `YYYY-MM-DDTHH:MM:SS.sss`  
Example: `1963-11-23T17:16:20.258`  
Nov. 23, 1963 at 5:16:20.258 PM  

**Year, month, day, hour, minute, UTC**

Format: `YYYY-MM-DDTHH:MMZ`  
Example: `1963-11-23T17:16Z`  
Nov. 23, 1963 at 5:16 PM UTC  

**Year, month, day, hour, minute, timezone**

Format: `YYYY-MM-DDTHH:MM±HH:MM`  
Example: `1963-11-23T12:16-05:00`  
Nov. 23, 1963 at 12:16 AM EST  

**Year, month, day, hour, minute, second, timezone**

Format: `YYYY-MM-DDTHH:MM:SS±HH:MM`  
Example: `1963-11-23T12:16:20-05:00`  
Nov. 23, 1963 at 12:16:20 AM EST  

**Year, month, day, hour, minute, second, millisecond, timezone**

Format: `YYYY-MM-DDTHH:MM:SS.sss±HH:MM`  
Example: `1963-11-23T12:16:20.258-05:00`  
Nov. 23, 1963 at 12:16:20.258 AM EST  

**Period of days**

Format: `PddD`  
Example: `P686D`  
686 days  

**Period of days, hours**

Format: `PddDhhH`  
Example: `P686D23H`  
686 days, 23 hours  

**Period of days, hours, minutes**

Format: PddDhhHmmM  
Example: P686D23H18M  
686 days, 23 hours, 18 minutes  

**Period of days, hours, minutes, seconds**

Format: `PddDhhHmmMssS`  
Example: `P686D23H18M14S`  
686 days, 23 hours, 18 minutes, 14 seconds  

**Period of days, hours, minutes, seconds, milliseconds**

Format: `PddDhhHmmMss.sssS`  
Example: `P686D23H18M14.400S`  
686 days, 23 hours, 18 minutes, 14 seconds, 400 milliseconds  

Exact date example:
```html
<time datetime="1963-11-23T12:16:20Z">Premiere of the most important TV show of all time!</time>
```

Simple time period:
```html
<time datetime="P365D6H8M">Earth’s orbital period</time>
```

Range of time periods:
```html
Opossum gestation period: <time datetime="P12D">twelve</time> to <time datetime="P13D">thirteen</time> days.
```
-----
sources:
- [W3schools](https://www.w3schools.com/tags/)
- [W3C](https://www.w3.org/TR/html5/)
- [algonquindesign.ca](https://learn-the-web.algonquindesign.ca/topics/html-semantics-cheat-sheet/)
