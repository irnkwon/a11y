
# Accordion
- The entire accordion header should be clickable and relay hover and focus states.

## Keyboard Interaction
- <code>Enter</code> or <code>Space</code>
  - When focus is on the accordion header for a collapsed panel, expands the associated panel. 
    If the implementation allows only one panel to be expanded, and if another panel is expanded, collapses that panel.
  - When focus is on the accordion header for an expanded panel, collapses the panel if the implementation supports collapsing. 
    Some implementations require one panel to be expanded at all times and allow only one panel to be expanded; 
    so, they do not support a collapse function.
- <code>Tab</code>
  - Moves focus to the next focusable element; all focusable elements in the accordion are included in the page <code>Tab</code> sequence.
- <code>Shift + Tab</code>
  - Moves focus to the previous focusable element; all focusable elements in the accordion are included in the page <code>Tab</code> sequence.
- <code>Down Arrow</code> (Optional)
  - If focus is on an accordion header, moves focus to the next accordion header. 
    If focus is on the last accordion header, either does nothing or moves focus to the first accordion header.
- <code>Up Arrow</code> (Optional)
  - If focus is on an accordion header, moves focus to the previous accordion header. 
    If focus is on the first accordion header, either does nothing or moves focus to the last accordion header.
- <code>Home</code> (Optional)
  - When focus is on an accordion header, moves focus to the first accordion header.
- <code>End</code> (Optional)
  - When focus is on an accordion header, moves focus to the last accordion header.

## WAI-ARIA Roles, States, and Properties
- The title of each accordion header is contained in an element with role <code>button</code>.
- Each accordion header button is wrapped in an element with role <code>heading</code> that has a value set for <code>aria-level</code> 
  that is appropriate for the information architecture of the page.
  - If the native host language has an element with an implicit heading and aria-level, such as an HTML heading tag, a native host language element may be used.
  - The button element is the only element inside the heading element. That is, if there are other visually persistent elements, they are not included inside the heading element.
- If the accordion panel associated with an accordion header is visible, the header button element has <code>aria-expanded</code> set to true. 
  If the panel is not visible, aria-expanded is set to false.
- The accordion header button element has <code>aria-controls</code> set to the ID of the element containing the accordion panel content.
- If the accordion panel associated with an accordion header is visible, and if the accordion does not permit the panel to be collapsed, 
  the header button element has <code>aria-disabled</code> set to true.
- Optionally, each element that serves as a container for panel content has role <code>region</code> and <code>aria-labelledby</code> with a value 
  that refers to the button that controls display of the panel.
  - Avoid using the region role in circumstances that create landmark region proliferation, e.g., in an accordion that contains more than approximately 6 panels that can be expanded at the same time.
  - Role region is especially helpful to the perception of structure by screen reader users when panels contain heading elements or a nested accordion.

## Examples
- [W3C Accordion Example](https://www.w3.org/WAI/ARIA/apg/patterns/accordion/examples/accordion/)
- [MagentaA11y Expander Accordion Example](https://www.magentaa11y.com/checklist-web/expander/)

# References
- https://www.w3.org/WAI/ARIA/apg/patterns/accordion/
- https://www.aditus.io/patterns/accordion/
