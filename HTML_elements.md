# HTML Reference


## Document

#### `<title>`

Shown in the browser tab & search results.
Should be unique for every page on the site.

#### `<link href="…" rel="stylesheet">`

For linking CSS and other resources like feeds.
rel has different values for other resources.

#### `<header>`

When inside `<body>` it’s the website masthead.
When inside `<article>` it’s the most important information.

#### `<footer>`

When inside `<body>` it’s the website footer.
When inside `<article>` it’s the least important information.

#### `<main>`

Primary content of the page.

#### `<nav>`

Defines a group a navigation links.

#### `<article>`

A piece of content that’s independent.
Could be removed from this website and still make sense.

#### `<section>`

A group in a series of related content pieces.

#### `<aside>`

Secondary content not required to understand the main content.

*Example: Navigation inside header*
```html
<header>
  <nav>
    <ul>
      <li><a href="#">About</a></li>
      <li><a href="#">Store</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>
</header>
```

*Example: Main content groups*
```html
<body>
  <header>
    <nav>…</nav>
  </header>

  <main>
    <h1>Example.co</h1>
  </main>

  <footer>
    <p>© 2018 Example.co</p>
  </footer>
</body>
```


## Lists

#### `<ul>`

An unordered list—the order of items isn’t important.
Can only have `<li>` elements as direct children.

#### `<ol>`

An ordered list—the order of the items is important.
Could be alphabetical, numerical, etc.
Can only have `<li>` elements as direct children.

#### `<li>`

A single list item.
Must be inside a `<ul>` or `<ol>`.
Can have most other elements inside it.

#### `<dl>`

A description list—a grouping of terms and definitions.
Words & definitions, titles & summaries, data points, etc.
Can only have `<dt>` and `<dd>` elements as direct children.

#### `<dt>`

Description title, the term of the item.
Must come before the `<dd>`.

#### `<dd>`

Description definition, the data, or text of the item.
Can be multiple `<dd>` tags underneath one `<dt>`.

*Example: Description list*
```html
<dl>
  <dt>Length</dt>
  <dd>2.3 m</dd>
  <dt>Weight</dt>
  <dd>4 tonnes</dd>
</dl>
```


## Text

#### `<a href="…">`

For making hyperlinks.
href is the path to where the link should go.

#### `<h1>`

On the homepage this should be the site’s name.
On inside pages this should be the page title.

#### `<h2>, <h3>, <h4>, <h5>, <h6>`

Content headings, each a sub-heading of the one above.
The `<h2>` is a sub-heading of `<h1>`,` <h3>` a sub-heading of `<h2>`, etc.

#### `<p>`

A generic paragraph of text.

#### `<blockquote>`

A large, stand alone quote from another source.

#### `<cite>`

A citation for another source, often used with quotations.
A person’s name, a URL, a book, a movie title, etc.

#### `<q>`

A small quotation embedded within other content.

#### `<em>`

A string of emphasized, slightly more important text.
Screen readers will change their voice for this text.

#### `<strong>`

A string of highly emphasized, much more important text.
Screen readers will change their voice for this text.

#### `<ins datetime="…">`

Content that was inserted after the document was published.
datetime defines when it was added.

#### `<del datetime="…">`

Content that was deleted after the document was published.
datetime defines when it was removed.

#### `<abbr title="…">`

An acronym or abbreviation, like “HTML”, “CSS”, etc.
title contains the expanded version, like “Hypertext Markup Language”.

#### `<dfn>`

A definition of a term on the page.
Should only be used once of the term.

#### `<mark>`

Used to highlight a piece of text for reference.
The keywords in a search results page, the current navigation item.

#### `<i>`

Defines a span of text in an alternate voice or mood. A technical term, a ship name, a book title, a thought, sarcasm, another language. Terms in languages different from the main text should be annotated with lang attributes: `<i lang="fr">je ne sais quoi</i>`.

#### `<b>`

Defines a keyword, like product name in a review, a lead sentence in a paragraph.

#### `<s>`

Content that’s no longer relevant to the document.
Consider if the `<del>` element is better suited first.

#### `<u>`

Labels the text as having a non-textual annotation.
A misspelled word, a Chinese proper name, etc.

#### `<small>`

Represents side comments and fine print.

#### `<address>`

Contact information, email, tel, postal address, etc.

*Example: Blockquotes*
```html
<blockquote>
  <p>Dinosaurs may be extinct from the face of the planet, but they are alive and well in our imaginations.</p>
  <footer>— <cite>Steve Miller</cite></footer>
</blockquote>
```

*Example: Addresses*
```html
<address>
  Jet Propulsion Laboratory
  <br>4800 Oak Grove Drive
  <br>Pasadena, California
  <br>91109
</address>
```

*Example: Text Edits*
```html
<p>Launchpad 39A owned by <del datetime="2014-04-14">NASA</del> <ins datetime="2014-04-14">SpaceX</ins></p>
```


## Images & media

#### `<img src="…" alt="…">`

Embeds an image that’s important to the content.
src is a path to the image file.
alt describes the image if it cannot be seen.

#### `<figure>`

Embeds annotated images, illustrations, photos, code, etc.
Could be moved out of place and would still make sense.

#### `<figcaption>`

For adding a caption/annotation to the `<figure>`.
Must be inside a `<figure>` element—cannot stand alone.

#### `<picture>`

Responsive image insertion—allows developers to provide different images for different contexts.

#### `<video poster="…" autoplay loop muted controls>`

For embedding movies into a website.
poster is the path to an image that’s displayed before the video plays.
autoplay will hint the video to start automatically.
loop triggers whether the video should repeat or not.
muted can be added to not play sound by default.
controls shows or hides the browser’s player buttons.

#### `<audio autoplay loop muted controls>`

For embedding sounds into a website.
autoplay will hint the audio to start automatically.
loop triggers whether the audio should repeat or not.
muted can be added to not play sound by default.
controls shows or hides the browser’s player buttons.

#### `<source>`

Must be inside `<picture>`, `<video>` or `<audio>` to define the different versions of content.
For example, in video it gives paths to the MP4 and WEBM formats.

#### `<track>`

Used to pair captions, chapters, etc. with `<video>` elements.

*Example: Figures & captions (use only if there’s a caption)*
```html
<figure>
  <img src="images/dino-small.jpg" alt="">
  <figcaption>So many dinosaurs I can’t even count!</figcaption>
</figure>
```

*Example: Responsive images (see [responsive & retina images for details](https://learn-the-web.algonquindesign.ca/topics/responsive-retina-images/))*
```html
<picture>
  <source media="(min-width: 60em)" srcset="images/dino-wide.jpg">
  <source media="(min-width: 38em)" srcset="images/dino-rectangle.jpg">
  <img src="images/dino-small.jpg" alt="All the dinosaurs!">
</picture>
```


## Data & code

#### `<sub>`

Defines text as being subscript.

#### `<sup>`

Defines text as being superscript.

#### `<var>`

Represents a variable in math or programming.

#### `<time datetime="…">`

Marks some text as a time or date.
datetime defines the machine readable version.

#### `<data value="…">`

Marks elements as being a numerical piece of information.
value provides the machine readable version.

#### `<meter value="…" min="…" max="…">`

Represents a single number in a range of numbers.
value is the current number.
min is the minimum number.
max is the maximum number.

#### `<progress value="…" min="…" max="…">`

Represents the current position in a series of steps.
value is the current position.
min is the minimum position.
max is the maximum position.

#### `<code>`

Defines a piece of text as a code sample.

#### `<pre>`

A piece of text that has a specific formatting, where tabs, whitespaces, etc. should be maintained.

#### `<kbd>`

Something a user should type into their computer.

#### `<samp>`

Something a user should see output from a computer.

*Example: Time*
```html
Apollo 11 landed on the moon <time datetime="1969-07-20T20:18">July 20, 1969</time>
```

*Example: Data*
```html
Argentinosaurus weighted approximately <data value="90">90 tonnes</data>
```

*Example: Maths*
```html
E = mc<sup>2</sup>
```


## Meaningless (non-semantic) tags

#### `<div>`

Inherits meaning from its children.
Divides content into logical groups, when no other tag is better suited.
Has restrictions on what elements it can be inside.

#### `<span>`

Inherits meaning from its children.


## Be careful

#### `<br>`

Creates a line break that’s significant to the content.
Useful in poems and addresses where the division of lines is important.
Do not use to create space in a design—use margins and padding.

#### `<hr>`

Represents a thematic break in the content.
For example, a scene change or topic change.
Do not use to create a horizontal line—use CSS borders.

#### `<button>`

Represents a interactive, clickable button.
Can be used in forms instead of `<input type="button">`. Unlike `input`, the button can wrap around other elements (`<img>` for example).
Do not use to link to another page—use the `<a>` tag.

#### `<wbr>`

Presents an opportunity for the browser to add a line-break if necessary. This could be in the middle of a long word, title or sentence.

## Links

#### Links that go nowhere
```html
<a href="#">Nowhere</a>
```
#### Links on the same page
```html
<a href="#herbivores">See the herbivores</a>

<h2 id="herbivores">Herbivores</h2>
```
#### Links to other files
```html
<a href="herbivores/stegosaurus.html">Stegosaurus</a>
```

#### Links to other websites

Always start with https:// or less ideally http://
```html
<a href="https://www.wikipedia.org/">Wikipedia</a>

<!-- Adding `rel="external"` for outward-bound sites is good -->
<a href="https://www.wikipedia.org/" rel="external">Wikipedia</a>
```

#### Links to phone numbers

Start with tel:, use international format
```html
<a href="tel:+18005551234">Call Me!</a>
```
Send a text message with sms:
```html
<a href="sms:+18005551234&body=Text%20me%20please">Text Me!</a>

<!-- or without a default number -->
<a href="sms:&body=Text%20me%20please">Text Me!</a>
```

#### Links to email addresses

Pops open a new email message, start with mailto:
```html
<a href="mailto:hello@example.co">Thomas</a>

<!-- Add a subject too -->
<a href="mailto:hello@example.co?subject=How%20are%20you?">Thomas</a>

<!-- Even a default body -->
<a href="mailto:hello@example.co?subject=How%20are%20you?&body=Hey%20Thomas">Thomas</a>
```


## Date/time formats

Apply to the datetime="" attribute of the `<time>`, `<del>` & `<ins>` elements.

#### Year

Format: `YYYY`  
Example: `1963`

#### Year, month

Format: `YYYY-MM`  
Example: `1963-11`  
Nov. 1963

#### Year, month, day

Format: `YYYY-MM-DD`  
Example: `1963-11-23`  
Nov. 23, 1963  

#### Year, week

Format: `YYYY-Wdd`  
Example: `1963-W47`  
1936, the week of Nov. 18–24  

#### Hour, minute

Format: `HH:MM`  
Example: `17:16`  
5:16 PM  

#### Hour, minute, second

Format: `HH:MM:SS`  
Example: `17:16:20`  
5:16:20 PM  

#### Hour, minute, second, millisecond

Format: `HH:MM:SS.sss`  
Example: `17:16:20.258`  
5:16:20.258 PM  

#### UTC timezone

Format: `Z`  
Example: `Z`  
UTC timezone  

#### Timezone offsets

Format: `±HH:MM`  
Example: `-05:00`  
Eastern Standard Time, Daylight Savings  

#### Year, month, day, hour, minute

Format: `YYYY-MM-DDTHH:MM`  
Example: `1963-11-23T17:16`  
Nov. 23, `1963 at 5:16 PM`  

#### Year, month, day, hour, minute, second

Format: `YYYY-MM-DDTHH:MM:SS`  
Example: `1963-11-23T17:16:20`  
Nov. 23, 1963 at 5:16:20 PM  

#### Year, month, day, hour, minute, second, millisecond

Format: `YYYY-MM-DDTHH:MM:SS.sss`  
Example: `1963-11-23T17:16:20.258`  
Nov. 23, 1963 at 5:16:20.258 PM  

#### Year, month, day, hour, minute, UTC

Format: `YYYY-MM-DDTHH:MMZ`  
Example: `1963-11-23T17:16Z`  
Nov. 23, 1963 at 5:16 PM UTC  

#### Year, month, day, hour, minute, timezone

Format: `YYYY-MM-DDTHH:MM±HH:MM`  
Example: `1963-11-23T12:16-05:00`  
Nov. 23, 1963 at 12:16 AM EST  

#### Year, month, day, hour, minute, second, timezone

Format: `YYYY-MM-DDTHH:MM:SS±HH:MM`  
Example: `1963-11-23T12:16:20-05:00`  
Nov. 23, 1963 at 12:16:20 AM EST  

#### Year, month, day, hour, minute, second, millisecond, timezone

Format: `YYYY-MM-DDTHH:MM:SS.sss±HH:MM`  
Example: `1963-11-23T12:16:20.258-05:00`  
Nov. 23, 1963 at 12:16:20.258 AM EST  

#### Period of days

Format: `PddD`  
Example: `P686D`  
686 days  

#### Period of days, hours

Format: `PddDhhH`  
Example: `P686D23H`  
686 days, 23 hours  

#### Period of days, hours, minutes

Format: PddDhhHmmM  
Example: P686D23H18M  
686 days, 23 hours, 18 minutes  

#### Period of days, hours, minutes, seconds

Format: `PddDhhHmmMssS`  
Example: `P686D23H18M14S`  
686 days, 23 hours, 18 minutes, 14 seconds  

#### Period of days, hours, minutes, seconds, milliseconds

Format: `PddDhhHmmMss.sssS`  
Example: `P686D23H18M14.400S`  
686 days, 23 hours, 18 minutes, 14 seconds, 400 milliseconds  

#### Exact date example
```html
<time datetime="1963-11-23T12:16:20Z">Premiere of the most important TV show of all time!</time>
```

#### Simple time period
```html
<time datetime="P365D6H8M">Earth’s orbital period</time>
```

#### Range of time periods
```html
Opossum gestation period: <time datetime="P12D">twelve</time> to <time datetime="P13D">thirteen</time> days.
```
-----
credit: [algonquindesign.ca](https://learn-the-web.algonquindesign.ca/topics/html-semantics-cheat-sheet/)
