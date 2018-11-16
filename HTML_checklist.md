# HTML Checklist


## Syntax

- [ ] All indents use soft tabs of 2 spaces.
- [ ] The document is indented consistently. See these [HTML indentation suggestions](https://learn-the-web.algonquindesign.ca/topics/html-indentation/).
- [ ] No trailing slashes in self-closing (void) elements. For example: `<br>`, not: `<br />`.
- [ ] Double quotes `""` are used for all attributes.
- [ ] Attributes are ordered like:
  - class
  - id
  - data-*
  - src, href, for, type, value
  - title, alt
  - role, aria-*
- [ ] Boolean attributes do not include values, for example:
  `<input type="checkbox" value="1" checked>`.
- [ ] Trailing white spaces are removed.

## Doctype & Head

- [ ] Document begins with a valid DTD `<!DOCTYPE html>`.
- [ ] The `<html>` element has a correct [lang](https://www.sitepoint.com/iso-2-letter-language-codes/) attribute, for example: `<html lang="en">`.
- [ ] Includes `<meta charset="utf-8">` immediately after `<head>`.
- [ ] The `<title>` comes after `<meta charset>`, is unique for every page—and isn’t *Untitled*.
- [ ] Uses the meta viewport element.
- [ ] Uses the meta description and any other meta elements according to preference.
- [ ] CSS files are linked inside the `<head>`.
- [ ] JS files are either linked in the `<head>` and use the `async` or `defer` attribute... or directly above the closing `</body>` depending on your preference.
- [ ] The `type` attribute is omitted for style sheets and scripts.
- [ ] The HTTPS protocol is used for embedded resources when possible, for example:
  `<link href="https://fonts.googleapis.com...">`.

## Document

- [ ] A `<header>` element is around the website’s masthead.
- [ ] A `<nav>` element is around the most important navigation.
- [ ] A `<main>` element is around the primary content.
- [ ] A `<footer>` element is around the copyright notice.
- [ ] Contains `<article>` and `<section>` elements where appropriate.
- [ ] Code is commented where appropriate and needed.

## Content

- [ ] All content has semantically appropriate elements & no content is outside of an element.
- [ ] There’s an appropriate `<h1>` element on every page.
- [ ] Headings are ordered properly.
- [ ] All links go somewhere. Use the [W3C link checker](http://validator.w3.org/checklink).
- [ ] The `<figure>` isn’t used without a `<figcaption>`.
- [ ] All email addresses and phone numbers are linked.
- [ ] Images have been optimized and where possible, **SVG is used**.
- [ ] Sprite Images are used where appropriate.
- [ ] All images contain appropriate `alt` and `title` text.
- [ ] Tables are only used to display tabular data.
- [ ] Form elements are paired with labels using the `for` attribute *or* labels wrap their input elements.

## Data

- [ ] All dates & times are marked up with `<time>`.
- [ ] All data points are marked up with `<data>`.
- [ ] All ranges of numbers are marked up with `<meter>`.

## Common Mistakes

- [ ] The `<em>` and `<i>` elements are not used to make text italic.
- [ ] The `<strong>` and `<b>` elements are not used to make text bold.
- [ ] The `<br>` element is used only for breaks that are part of the content, as in poems or addresses.
- [ ] The `<hr>` element is not used to make horizontal lines but a thematic change in the content.
- [ ] Code does not contain inline or in-document styling.
- [ ] Code does not contain deprecated elements & attributes.
- [ ] Script blocks are externalized to .js files.

## Validation

- [ ] Every HTML file has been validated. [W3C HTML Validator](http://validator.w3.org/)
- [ ] There’s nothing immediately inside `<ul>` & `<ol>` except `<li>` elements.
- [ ] No `<li>` elements are outside of `<ul>` or `<ol>`.
- [ ] No `<dt>` or `<dd>` elements are outside of a `<dl>`.
- [ ] The `<figcaption>` isn’t outside a `<figure>`.

## Accessibility

[Web Content Accessibility Guidelines (WCAG)](<https://www.w3.org/WAI/standards-guidelines/wcag/)  
TODO: summarize the standards here.
- [ ] [Run an accessibility check](http://www.cynthiasays.com/)

## Performance

- [ ] Site uses a cache buster for expiring .js, .css, and images.
- [ ] Run a performance check: [YSlow](http://yslow.org/)  
- [ ] Run a performance check: [PageSpeed](https://developers.google.com/speed/pagespeed/insights/)

## Search Engine Guidelines

[Search Engine Optimization (SEO) Starter Guide](https://support.google.com/webmasters/answer/7451184#)  
TODO: summarize the standards here.

--------

## Sources:  
[HTML5 Spec](https://w3c.github.io/html/)  
[codeguide.co](http://codeguide.co/)  
[algonquindesign.ca](https://learn-the-web.algonquindesign.ca/topics/html-semantics-checklist/)
