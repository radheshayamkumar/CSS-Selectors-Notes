##🎨 Master Notes: CSS Selectors
Overview: CSS Selectors are patterns used to select the element(s) you want to style. They are the bridge between your HTML structure and your visual design.

1. The Basic Selectors
These are the most fundamental ways to target elements.

A. Universal Selector
Symbol: *

Usage: Selects every single element on the page.

Common Use Case: resetting margins and padding to ensure consistency across different browsers.

CSS

/* From your file */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box; /* Ensures padding doesn't increase element width */
}
B. Type (Element) Selector
Symbol: The HTML tag name (e.g., p, h1, div).

Usage: Selects all elements of that specific type.

CSS

/* From your file */
p {
  font-size: 16px;
  margin-bottom: 10px;
}
C. Class Selector
Symbol: . (dot) followed by the class name.

Usage: Selects elements with a specific class attribute.

Key Rule: Classes can be reused on multiple elements.

CSS

/* From your file */
.highlight {
  background-color: #21a2c9;
}
D. ID Selector
Symbol: # (hash) followed by the ID name.

Usage: Selects a single element with a specific id.

Key Rule: An ID must be unique within a page (used only once).

CSS

/* From your file */
#header {
  background-color: #860303;
}
2. Combinator Selectors (Relationships)
These selectors target elements based on their relationship to other elements (parents, children, siblings).

A. Descendant Selector
Symbol: (Space)

Syntax: Parent Child

Usage: Selects the element if it is nested anywhere inside the specified parent (can be a child, grandchild, etc.).

CSS

/* From your file: Targets any <p> inside an <article> */
article p {
  font-style: italic;
  background-color: #1a1a1a;
  color: #fff;
  padding: 10px;
}
B. Child Selector
Symbol: >

Syntax: Parent > Child

Usage: Selects the element only if it is a direct child of the parent. It will not select grandchildren.

CSS

/* From your file: Targets <p> only if it is directly inside a <div> */
div > p {
  background-color: #880404;
}
C. Adjacent Sibling Selector
Symbol: +

Syntax: Element1 + Element2

Usage: Selects Element2 only if it immediately follows Element1.

CSS

/* From your file: Targets a <p> that comes immediately after an <h1> */
h1 + p {
  font-weight: bold;
}
D. General Sibling Selector
Symbol: ~

Syntax: Element1 ~ Element2

Usage: Selects all instances of Element2 that follow Element1, as long as they share the same parent. They do not need to be immediately adjacent.

CSS

/* From your file: Targets all <p> tags that come after <h2> */
h2 ~ p {
  color: #860303;
}
3. Attribute & Grouping Selectors
Advanced targeting based on properties or efficiency.

A. Attribute Selector
Symbol: []

Usage: Selects elements based on the presence or value of a specific attribute.

CSS

/* From your file: Targets only input fields where type="text" */
input[type="text"] {
  border: 2px solid #21a2c9;
}
B. Grouping Selector
Symbol: , (comma)

Usage: Applies the same styles to multiple different selectors to save code.

CSS

/* From your file: Applies orange color to h1, h2, AND h3 */
h1,
h2,
h3 {
  color: orange;
}
4. Pseudo-Classes & Pseudo-Elements
Targeting specific states or parts of an element.

A. Pseudo-class Selector
Symbol: : (single colon)

Usage: Defines a special state of an element (e.g., when a user hovers over it, visits a link, or focuses an input).

CSS

/* From your file: Changes style when mouse hovers over a link */
a:hover {
  background-color: #14a50e;
  text-decoration: none;
  color: #1a1a1a;
}
B. Pseudo-element Selector
Symbol: :: (double colon)

Usage: Styles a specific part of the selected element (e.g., the first letter or the first line).

CSS

/* From your file: Makes the first letter of paragraphs large and bold */
p::first-letter {
  font-weight: bold;
  font-size: 30px;
}
🧠 Expert Corner: Specificity (The Priority Game)
Since you are teaching this, it is vital to mention Specificity. What happens if a <p> tag has a Class and an ID with conflicting colors? Who wins?

CSS uses a point system to decide:

ID Selector (#id): Most powerful (Highest Priority).

Class / Attribute / Pseudo-class (.class): Medium Priority.

Type Selector (p): Lowest Priority.

Example: If you have p { color: red; } and #header { color: blue; }, the text will be blue because IDs outweigh Type selectors.

Tip for Students: Try to avoid using !important in CSS. It overrides all specificity rules and makes debugging difficult later!
