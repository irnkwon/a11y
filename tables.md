
# Tables
- Header cells must be marked up with <code>\<th></code>, and data cells with <code>\<td></code> to make tables accessible.
- For more complex tables, explicit associations may be needed using <code>scope</code>, <code>id</code>, and <code>headers</code> attributes.
- As a general rule, tables aren’t meant to be used for layout purposes. Instead, a best practice is to use CSS for visual presentation.

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

## Example
- https://www.magentaa11y.com/checklist-web/table/

# References
- https://www.w3.org/WAI/tutorials/tables/
- https://webaim.org/techniques/tables/
