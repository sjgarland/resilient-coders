# HTML Interview Questions

> Good answers to questions about HTML are on the website for [W3Schools](https://www.w3schools.com/).

What does a doctype do?

> The doctype tag at the beginning of an HTML document tells the version of HTML in which the document is written.  `<!DOCTYPE html>` indicates HTML5 and instructs browsers to ignore the quirks present (or absent) in earlier versions of HTML.

How do you serve a page with content in multiple languages?

> The primary language for a document is described in a tag like `<html lang="en">` at the beginning of the document.  Alternative languages for elements within the document can be specified in tags like `<p lang="fr">`.  These tags help screen readers use the correct pronunciation when the document contains content in multiple languages.

What kind of things must you be wary of when design or developing for multilingual sites?

> Be aware of different notational conventions in different languages.  The British write dates 10 January 2021 and 10/1/2021 instead of as January 10, 2021 and 1/10/2021.   The French write decimals as 10,5 instead of as 10.5.  If content is embedded in images, provide a way for screen readers to access that content.

What are data- attributes good for?

> I had to look this one up.  I never used data attributes (or did not realize I was using them if I did).

Consider HTML5 as an open web platform. What are the building blocks of HTML5?

> I don't understand what this question is asking or why it is important.  Is it asking about what makes HTML5 different from earlier versions of HTML?

Describe the difference between a cookie, sessionStorage and localStorage.

Describe the difference between `<script>`, `<script async>` and `<script defer>`.

> I can guess that the difference lies in when the script is loaded, but would have to look up the details.

Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before </body>? Do you know any exceptions?

> CSS links tell browsers how to render the page.  They should be in the header to avoid the need for re-rendering.  Pages will load faster if scripts are placed before `</body>`.  However, if scripts are needed to render the page (e.g., by handling an onload event, they should be placed in the header.

What is progressive rendering?

> Progressive rendering gives users faster access to a page by choosing a good order in which to load its contents (e.g., by using lazy loading for images).

Why you would use a srcset attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.

> The srcset attribute lets browsers select images that are appropriate for the user's device (in terms of size and/or resolution).  I would have to look up details about how browsers use this attribute.

Have you used different HTML templating languages before?

> I have used Angular directives.
