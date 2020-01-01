---
layout: page
title: Accessibility
---

## WAI-ARIA

> WAI-ARIA is a technology that can help with such problems by adding in further semantics that browsers and assistive technologies can recognize and use to let users know what is going on.
> WAI-ARIA is a specification written by the W3C, defining a set of additional HTML attributes that can be applied to elements to provide additional semantics and improve accessibility wherever it is lacking.

- [WAI-ARIA Basics](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/WAI-ARIA_basics)
- [ARIA Roles](https://www.w3.org/TR/wai-aria-1.1/#role_definitions)

## WCAG 2.1

- [MDN: Understanding WCAG](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG)

> WCAG 2.1 is the most recent and relevant accessibility standard. Use WCAG 2.1 to help more people with disabilities and reduce the future legal risk for web site owners. Target WCAG 2.0 first when allocating resources. Then step up to WCAG 2.1.

The four principles:

1. Perceivable
2. Operable
3. Understandable
4. Robust

### Differences between WCAG 2.0 and 2.1

- [W3C: What’s New in WCAG 2.1](https://www.w3.org/WAI/standards-guidelines/wcag/new-in-21/)
- [WCAG 2.1 vs 2.0: What’s The Difference?](https://www.mannixmarketing.com/blog/wcag-2-1-vs-2-0/)
- [The new guidelines in WCAG 2.1 explained](https://alexanderskogberg.com/2018/02/new-guidelines-wcag-2-1-explained/)

## [HTTP Archive Web Almanac](https://almanac.httparchive.org/en/2019/accessibility)

1. Contrast
2. `<alt>` tags
3. Language identification (`<lang>`)
4. Captions on audio or video (`<track>` element!)
5. Headings: Don't skip a level (going from `h1` to `h3`)
6. Use `<main>` to let screen readers know where the main part of the site is
7. Use HTML section elements (`<header>`, `<footer>`, `<navigation>`, `<main>`, `<article>`, `<hr>`, `<aside>`)
8. Use `[aria-keyshortcuts](https://www.w3.org/TR/wai-aria-1.1/#aria-keyshortcuts)` to define shortcuts on the page. `[accesskey](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/accesskey)` is similar, but inadvisable to use.
9. Tables: Markup tableheaders using `<th>` properly
10. Use `<caption>` for tables
11. Use `aria`-elements properly.
    > The "role" attribute is the most important attribute in the entire ARIA specification. It's used to inform the browser what the purpose of a given HTML element is (i.e., the semantic meaning). For example, a `<div>` element, visually styled as a button using CSS, should be given the ARIA role of button.
12. Use `posinset` and `setsize` to convey to screen readers how big a menu is, and where the user is currently:
    > For example, we found that the `posinset` and `setsize attributes were only used on 0.01% of pages. These attributes convey to a screen reader user how many items are in a list or menu and which item is currently selected. So, if a visually impaired user is trying to navigate through a menu, they might hear index announcements like: "Home, 1 of 5", "Products, 2 of 5", "Downloads, 3 of 5", etc.
13. Mark up `dialog`s correctly [using the `dialog` role in `ARIA`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/dialog_role).
14. Labels on interactive elements: Use labels on buttons instead of only icons (e.g. left-pointing chevron and the label "back")
15. Use labels on form elements, e.g. the `<label>` element, `aria-label` or `aria-labelledby` for each input
16. Use `required`, `aria-required` and `aria-invalid` to signify which input fields are required in a form.
    > As a nice bonus, when you inform browsers what fields are required, they'll [validate parts of your forms](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Form_validation) for you. No JavaScript required.
17. Use IDs only once:
    > IDs can be used in HTML to link two elements together. For example, the `<label>` element works this way. You specify the ID of the input field this label is describing and the browser links them together. The result? Users can now click on this label to focus on the input field, and screen readers will use this label as the description.
    > [...] many ARIA attributes, such as `aria-describedby` and `aria-labelledby`, work similarly to the `label` element detailed above

## Forms

1. Use CSS pseudo-classes [`:valid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:valid) and [`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid) to style input fields that meet or don't meet validation criteria. Link: [MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Form_validation).
2. Use the CSS pseudo class [`:required`](https://developer.mozilla.org/en-US/docs/Web/CSS/:required) to style required inputs
3. Use the right "Validation-related attributes". [See the full list on MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/Constraint_validation#Validation-related_attributes).

- [Full list of `<input>` attributes from MDN.](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#Form_%3Cinput%3E_types)

## SEO

From the HTTP Archive Almanac:

1. Use the right headings
2. A `<title>` tag should contain 50-60 characters (as this is what Google SERPs ususally display)
3. A `<description>` tag should contain 155-160 characters at most
4. Use `alt` tags on images
5. Use descriptive text for links, not just "click here", "go" or "learn more".
6. Use [an FAQ Page with proper markup](https://developers.google.com/search/docs/data-types/faqpage) to display rich results on Google.
7. Use [Schemas to enrich SERPs](https://schema.org/WebPage).

## [GitHub Primer Accessibility](https://primer.style/css/principles/accessibility)

> Always use semantic HTML elements, like `button`, `ul`, `nav`. Most modern browsers implement the accessibility features outlined in the specs for these elements; without them, elements will need additional `ARIA` attributes and roles to be recognized by assistive technologies.
> Only use a `div` or a `span` to markup up content when there isn't another HTML element that would semantically be more appropriate [...]
> When using JavaScript to change the content on the page, always make sure that screen reader users are informed about the change. This can be done with `aria-live`, or focus management.

- [GitHub Collection of Web accessibility tools](https://github.com/collections/web-accessibility)
- [Alix](https://github.com/ffoodd/a11y.css)
- [Awesome a11y Development Testing and Validators](https://github.com/brunopulis/awesome-a11y/blob/master/topics/validators.md)
- [a11y project](https://a11yproject.com)
- [Web Accessibility Guide](https://webaccessibility.guide)
- [How to meet WCAG](https://www.w3.org/WAI/WCAG21/quickref/)
- [Inclusive Design Checklist](https://github.com/Heydon/inclusive-design-checklist)
- [What is ARIA](https://blog.benmyers.dev/aria/)
