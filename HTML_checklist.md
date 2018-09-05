# HTML Checklist


## Doctype & Head

- [ ] Document begins with a valid DTD `<!doctype html>`
- [ ] The `<html>` tag has a correct lang attribute.
- [ ] Includes `<meta charset="utf-8">` immediately after `<head>`.
- [ ] The `<title>` comes after `<meta charset>`.
- [ ] The `<title>` is unique for every page—and isn’t *Untitled*.
- [ ] Uses the meta viewport tag.
- [ ] Uses the meta description and any other meta tags according to preference.
- [ ] CSS files are inside the `<head>`.
- [ ] JS files are either in the `<head>` and use the `async` or `defer` attribute... or directly above the closing `</body>` depending on your preference.

## Document

- [ ] A `<header>` tag is around the website’s masthead.
- [ ] A `<nav>` tag is around the most important navigation.
- [ ] A `<main>` element is around the primary content.
- [ ] A `<footer>` tag is around the copyright notice.
- [ ] Contains `<article>` and `<section>` tags where appropriate.
- [ ] Code is commented where appropriate

## Content

- [ ] All content has semantically appropriate elements & no content is outside of an element.
- [ ] There’s an appropriate `<h1>` tag on every page.
- [ ] Headings are ordered properly.
- [ ] All links go somewhere. Use the [W3C link checker](http://validator.w3.org/checklink)
- [ ] The `<figure>` isn’t used without a `<figcaption>`.
- [ ] All email addresses and phone numbers are linked.
- [ ] Images have been optimized and where possible, SVG is used.
- [ ] Sprite Images are used where appropriate
- [ ] All images contain appropriate `alt` and `title` text.
- [ ] Tables are only used to display tabular data
- [ ] Form elements are paired with labels using the for attribute OR labels wrap their input elements.

## Data

- [ ] All dates & times are marked up with `<time>`.
- [ ] All data points are marked up with `<data>`.
- [ ] All ranges of numbers are marked up with `<meter>`.

## Don't

- [ ] The `<em>` and `<i>` tags are not used to make text italic.
- [ ] The `<strong>` and `<b>` tags are not used to make text bold.
- [ ] The `<br>` tag is used only for breaks that are part of the content, as in poems or addresses.
- [ ] The `<hr>` tag is not used to make horizontal lines but a thematic change in the content.
- [ ] Code does not contain inline style attributes
- [ ] Code does not contain deprecated elements & attributes
- [ ] Script blocks are externalized to .js files

## Validation

- [ ] The document is indented consistently. [HTML indentation suggestions](https://learn-the-web.algonquindesign.ca/topics/html-indentation/)
- [ ] Every HTML file has been validated. [W3C HTML Validator](http://validator.w3.org/)
- [ ] There’s nothing immediately inside `<ul>` & `<ol>` except `<li>` elements.
- [ ] No `<li>` tags are outside of `<ul>` or `<ol>`.
- [ ] No `<dt>` or `<dd>` tags are outside of a `<dl>`.
- [ ] The `<figcaption>` isn’t outside a `<figure>`.

## Accessibility

[Web Content Accessibility Guidelines (WCAG)](<https://www.w3.org/WAI/standards-guidelines/wcag/)  
TODO: summarize the standards here
- [ ] [Run an accessibility check](http://www.cynthiasays.com/)

## Performance

- [ ] Site uses a cache buster for expiring .js, .css, and images
- [ ] Run a performance check: [YSlow](http://yslow.org/)  
- [ ] Run a performance check: [PageSpeed](https://developers.google.com/speed/pagespeed/insights/)

## Search Engine Guidelines

[Search Engine Optimization (SEO) Starter Guide](https://support.google.com/webmasters/answer/7451184#)  
TODO: summarize the standards here
