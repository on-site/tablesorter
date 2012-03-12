# Summary

This is the tablesorter jQuery plugin found from
http://tablesorter.com but with some enhancements added to support
additional functionality.

# Enhancements

In particular, this extension adds a "mixed" parser which uses a new
"array" data type for sorting mixed numeric and string content.  The
parser will split data into text and numeric segments, returning the
data as an array.  The sorter will then take the "array" type and
expect an array.  It will sort each element in the array as a separate
segment.  It starts at the first segments and continues until the 2
elements differ, at which point the difference will determine the sort
order.  If the arrays of the 2 table cells are equal in length and
content, they are considered equal.  If one starts out the same but
has an extra element, it is considered bigger.

## Example

    // This will sort the third column using the "mixed" sorter, so it
    // will properly sort things like "Street 11" versus "Street 2".
    $("table.sortable").tablesorter({ headers: { 2: { sorter: "mixed" } } });

# License

This code is considered licensed under the same license(s) that the
original source at http://tablesorter.com is licensed under.
