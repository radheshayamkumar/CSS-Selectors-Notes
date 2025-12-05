# 🎨 CSS Selectors: The Complete Classroom Guide

**Subject:** Web Development / CSS  
**Topic:** CSS Selectors & Specificity  
**Level:** Beginner to Intermediate

---

## 📖 Overview
This repository contains comprehensive notes and examples for **CSS Selectors**. Selectors are the fundamental patterns used to "select" the HTML elements you want to style. Mastering them is essential for writing clean, efficient, and maintainable CSS.

## 🚀 Table of Contents
1. [Basic Selectors](#1-basic-selectors)
2. [Combinator Selectors](#2-combinator-selectors-relationships)
3. [Attribute & Grouping](#3-attribute--grouping-selectors)
4. [Pseudo-Classes & Elements](#4-pseudo-classes--pseudo-elements)
5. [🎓 Expert Corner: Specificity](#-expert-corner-specificity)

---

## 1. Basic Selectors
These are the most common ways to target elements in the DOM.

### 🌟 Universal Selector
* **Symbol:** `*`
* **Description:** Selects **every single element** on the page. Often used for resetting browser defaults.
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
````

### 🏷️ Type (Element) Selector

  * **Symbol:** HTML Tag Name (e.g., `p`, `h1`, `div`)
  * **Description:** Selects all elements of that specific type.

<!-- end list -->

```css
p {
  font-size: 16px;
  margin-bottom: 10px;
}
```

### 🎯 Class Selector

  * **Symbol:** `.` (dot) + `classname`
  * **Description:** Selects elements with a specific class attribute. **Reusable** on multiple elements.

<!-- end list -->

```css
.highlight {
  background-color: #21a2c9;
}
```

### 🆔 ID Selector

  * **Symbol:** `#` (hash) + `id_name`
  * **Description:** Selects a **single** element with a specific ID. Must be unique on the page.

<!-- end list -->

```css
#header {
  background-color: #860303;
}
```

-----

## 2\. Combinator Selectors (Relationships)

Target elements based on their relationship to other elements.

### 👨‍👦 Descendant Selector

  * **Syntax:** `Parent Child` (Space)
  * **Description:** Selects an element nested **anywhere** inside the parent (child, grandchild, etc.).

<!-- end list -->

```css
/* Selects any <p> inside an <article> */
article p {
  font-style: italic;
  background-color: #1a1a1a;
  color: #fff;
  padding: 10px;
}
```

### 👶 Child Selector

  * **Syntax:** `Parent > Child`
  * **Description:** Selects the element **only if** it is a direct child of the parent.

<!-- end list -->

```css
/* Selects <p> only if it is a direct child of <div> */
div > p {
  background-color: #880404;
}
```

### ⏭️ Adjacent Sibling Selector

  * **Syntax:** `Element1 + Element2`
  * **Description:** Selects `Element2` only if it is placed **immediately after** `Element1`.

<!-- end list -->

```css
/* Selects <p> immediately following an <h1> */
h1 + p {
  font-weight: bold;
}
```

### 🌊 General Sibling Selector

  * **Syntax:** `Element1 ~ Element2`
  * **Description:** Selects all `Element2` instances that follow `Element1` (must share the same parent).

<!-- end list -->

```css
/* Selects all <p> tags that come after an <h2> */
h2 ~ p {
  color: #860303;
}
```

-----

## 3\. Attribute & Grouping Selectors

### 🔍 Attribute Selector

  * **Syntax:** `[attribute="value"]`
  * **Description:** Selects elements based on the presence or specific value of an attribute.

<!-- end list -->

```css
/* Selects only input fields where type is "text" */
input[type="text"] {
  border: 2px solid #21a2c9;
}
```

### 📦 Grouping Selector

  * **Syntax:** `Selector1, Selector2` (Comma)
  * **Description:** Applies the same styles to multiple selectors to reduce code duplication.

<!-- end list -->

```css
h1, h2, h3 {
  color: orange;
}
```

-----

## 4\. Pseudo-Classes & Pseudo-Elements

### 🖱️ Pseudo-class Selector

  * **Syntax:** `:state`
  * **Description:** Defines a special state of an element (e.g., hover, active, focus).

<!-- end list -->

```css
/* Changes style when mouse hovers over a link */
a:hover {
  background-color: #14a50e;
  text-decoration: none;
  color: #1a1a1a;
  padding: 5px;
}
```

### ✨ Pseudo-element Selector

  * **Syntax:** `::part`
  * **Description:** Styles a specific part of the selected element.

<!-- end list -->

```css
/* Styles the first letter of every paragraph */
p::first-letter {
  font-weight: bold;
  font-size: 30px;
}
```

-----

## 🎓 Expert Corner: Specificity

When two rules compete for the same element, **Specificity** determines which rule wins. It is calculated as a point system:

1.  **High Priority:** ID Selectors (`#header`)
2.  **Medium Priority:** Classes, Attributes, Pseudo-classes (`.highlight`, `:hover`)
3.  **Low Priority:** Type Selectors (`p`, `div`)

**The Rule:** A more specific selector will always override a less specific one, regardless of order in the CSS file.

> **Pro Tip:** Avoid using `!important` as it breaks the natural cascading nature of CSS and makes debugging difficult.

-----

*Notes prepared for the Department of Computer Science / MCA Curriculum.*

```
```
