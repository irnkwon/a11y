
# Tables
- Header cells must be marked up with <code>\<th></code>, and data cells with <code>\<td></code> to make tables accessible.
- For more complex tables, explicit associations may be needed using <code>scope</code>, <code>id</code>, and <code>headers</code> attributes.
- As a general rule, tables aren’t meant to be used for layout purposes. Instead, a best practice is to use CSS for visual presentation.
- Not an interactive widget; its cells are not focusable or selectable.
  - The [grid pattern](https://www.w3.org/WAI/ARIA/apg/patterns/grid/) is used to make an interactive widget that has a tabular structure.

## Caption and Summary
- A caption functions like a heading for a table
- A summary conveys information about the organization of the data in a table and helps users navigate it.
  - Usually only needed for complex tables.
- While they are not required in every case to meet WCAG, captions and summaries are fairly straightforward ways to provide such information that is often needed.

## The <code>scope</code> Attribute
- All <code>\<th></code> elements should generally always have a scope attribute.
- The scope attribute identifies whether a table header is a column header (<code>scope="col"</code>) or a row (<code>scope="row"</code>) header.

## The <code>id</code> and <code>headers</code> Attributes
- Another way to associate data cells and headers is to use the headers and id attributes.
- Not generally recommended because scope is usually sufficient for most tables, even if the table is complex with multiple levels of headers.

## <code>thead</code>, <code>tbody</code>, and <code>tfoot</code> Attributes
- Provide no accessibility functionality and are generally only of use when a long table is printed.
- No harm in using it for table styling or other reasons.

## WAI-ARIA Roles, States, and Properties
- The table container has role <code>table</code>.
- Each row container has role <code>row</code> and is either a DOM descendant of or owned by the table element or an element with role <code>rowgroup</code>.
- Each cell is either a DOM descendant of or owned by a row element and has one of the following roles:
  - <code>columnheader</code> if the cell contains a title or header information for the column.
  - <code>rowheader</code> if the cell contains title or header information for the row.
  - <code>cell</code> if the cell does not contain column or row header information.
- If there is an element in the user interface that serves as a label for the table, <code>aria-labelledby</code> is set on the table element with a value that refers to the labelling element. Otherwise, a label is specified for the table element using <code>aria-label</code>.
- If the table has a caption or description, <code>aria-describedby</code> is set on the table element with a value referring to the element containing the description.
- If the table contains sortable columns or rows, <code>aria-sort</code> is set to an appropriate value on the header cell element for the sorted column or row as described in the [Grid and Table Properties Practice](https://www.w3.org/WAI/ARIA/apg/practices/grid-and-table-properties/#gridAndTableProperties_sort).
- If there are conditions where some rows or columns are hidden or not present in the DOM, e.g., there are widgets on the page for hiding rows or columns, the following properties are applied as described in the [Grid and Table Properties Practice](https://www.w3.org/WAI/ARIA/apg/practices/grid-and-table-properties/).
  - <code>aria-colcount</code> or <code>aria-rowcount</code> is set to the total number of columns or rows, respectively.
  - <code>aria-colindex</code> or <code>aria-rowindex</code> is set to the position of a cell within a row or column, respectively.
- If the table includes cells that span multiple rows or multiple columns, then <code>aria-rowspan</code> or <code>aria-colspan</code> is applied as described in the [Grid and Table Properties Practice](https://www.w3.org/WAI/ARIA/apg/practices/grid-and-table-properties/#gridAndTableProperties_spans).
- If rows or cells are included in a table via <code>aria-owns</code>, they will be presented to assistive technologies after the DOM descendants of the table element unless the DOM descendants are also included in the aria-owns attribute.

## Example
- [W3C Table Example](https://www.w3.org/WAI/ARIA/apg/patterns/table/examples/table/)
- [MagentaA11y Table Examples](https://www.magentaa11y.com/checklist-web/table/)
- [Sortable Table Example](https://www.w3.org/WAI/ARIA/apg/patterns/table/examples/sortable-table/)

# References
- https://www.w3.org/WAI/tutorials/tables/
- https://www.w3.org/WAI/ARIA/apg/patterns/table/
- https://webaim.org/techniques/tables/
