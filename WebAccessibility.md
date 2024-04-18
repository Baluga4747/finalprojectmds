---
author: Lucas Williams
copyright: Lucas Williams
title: What is D3 in web development
---

# Web Accessibility

Web accessibility refers to the practice of designing web applications so that people with disabilities can navigate and interact with them effectively. It is an essential duty of developers because it ensures that all users, regardless of their abilities, are able to access and use the web equally. Web accessibility is not only a moral responsibility but often a legal requirement in many states and countrys.

## key practices

Semantic HTML: Use proper HTML elements to convey the structure and meaning of content. For example, use <nav> for navigation links, <header> for page headers, <main> for main content, <footer> for footers, etc.

Provide Alternative Text: Use the alt attribute in <img> tags to describe the content of images. This helps users with visual impairments understand the purpose of the image.

Use ARIA Landmarks: ARIA (Accessible Rich Internet Applications) landmarks help screen readers and other assistive technologies understand the structure of your page. You can use ARIA roles like role="navigation", role="main", role="banner", role="contentinfo", etc., to define different sections of your page.

Keyboard Accessibility: Ensure that all functionality of your website is operable through a keyboard alone. Users who cannot use a mouse rely on keyboard navigation.

Color Contrast: Make sure that there is sufficient contrast between text and background colors to ensure readability for users with low vision or color blindness.

# ARIA attributes

aria-label: This attribute defines a string value that labels the current element. It is particularly useful when an element's content does not adequately describe its purpose.

```
<button aria-label="Close">X</button>
```

aria-labelledby: This attribute points to the ID of another element on the page that serves as the label for the current element.

```
<h2 id="modal-title">Modal Title</h2>
<div role="dialog" aria-labelledby="modal-title">
  <!-- Modal content -->
</div>
```

aria-describedby: Similar to aria-labelledby, this attribute points to the ID of another element that provides a description of the current element.

```
<input type="text" aria-describedby="username-help">
<div id="username-help">Please enter your username</div>
```

aria-hidden: This attribute indicates whether an element is visible or hidden to assistive technologies.

```
<div aria-hidden="true">This text is hidden from screen readers</div>
```

aria-expanded: This attribute indicates whether a collapsible element is currently expanded or collapsed.

```
<button aria-expanded="false" aria-controls="collapse-content">Expand</button>
<div id="collapse-content" aria-hidden="true">Collapsible content</div>
```

# Resources 

[Web Content Accessibility Guidelines (WCAG) Overview](https://www.w3.org/WAI/standards-guidelines/wcag/)
[MDN Web Docs: ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
[Intro to ARIA](https://web.dev/articles/semantics-aria)
[Intro to Web Accessibility](https://www.w3.org/WAI/fundamentals/accessibility-intro/)
[The A11Y Project](https://www.a11yproject.com/)

