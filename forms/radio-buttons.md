
# Radio Buttons

## Keyboard Interaction

### For Radio Groups Not Contained in a Toolbar
- <code>Tab</code> and <code>Shift + Tab</code>
  - Move focus into and out of the radio group. When focus moves into a radio group:
  - If a radio button is checked, focus is set on the checked button.
  - If none of the radio buttons are checked, focus is set on the first radio button in the group.
- <code>Space</code>
  - Checks the focused radio button if it is not already checked.
- <code>Right Arrow</code> and <code>Down Arrow</code>
  - Move focus to the next radio button in the group, uncheck the previously focused button, and check the newly focused button. 
    If focus is on the last button, focus moves to the first button.
- <code>Left Arrow</code> and <code>Up Arrow</code>
  - Move focus to the previous radio button in the group, uncheck the previously focused button, and check the newly focused button. 
    If focus is on the first button, focus moves to the last button.
- The initial focus behavior described above differs slightly from the behavior provided by some browsers for native HTML radio groups.

## WAI-ARIA Roles, States, and Properties
- The radio buttons are contained in or owned by an element with role radiogroup.
- Each radio button element has role radio.
- If a radio button is checked, the radio element has aria-checked set to true. If it is not checked, it has aria-checked set to false.
- Each radio element is labelled by its content, has a visible label referenced by aria-labelledby, or has a label specified with aria-label.
- The radiogroup element has a visible label referenced by aria-labelledby or has a label specified with aria-label.
- If elements providing additional information about either the radio group or each radio button are present, 
  those elements are referenced by the radiogroup element or radio elements with the aria-describedby property.

## Examples
- [Radio Group Example Using Roving tabindex](https://www.w3.org/WAI/ARIA/apg/patterns/radio/examples/radio/)
- [Radio Group Example Using aria-activedescendant](https://www.w3.org/WAI/ARIA/apg/patterns/radio/examples/radio-activedescendant/)
- [Rating Radio Group Example](https://www.w3.org/WAI/ARIA/apg/patterns/radio/examples/radio-rating/)

# References
- https://www.w3.org/WAI/ARIA/apg/patterns/radio/
