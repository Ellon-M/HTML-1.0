#### Tables

The `table` tag: - Inside the table we’ll define the data. 

We reason in terms of rows, which means we add rows into a table (not columns). We’ll define columns inside a row.

A row is added using the `tr` tag, and that’s the only thing we can add into a `table` element:

    <table>
      <tr></tr>
      <tr></tr>
      <tr></tr>
    </table>

The first row can take the role of the header.

We define the header using the `th` tag.

    <table>
      <tr>
        <th>Column 1</th>
        <th>Column 2</th>
        <th>Column 3</th>
      </tr>
      <tr></tr>
      <tr></tr>
    </table>

The content of the table is defined using `td` tags, inside the other `tr` elements.


	  <table>
      <tr>
        <th>Column 1</th>
        <th>Column 2</th>
        <th>Column 3</th>
      </tr>
      <tr>
        <td>Row 1 Column 1</td>
        <td>Row 1 Column 2</td>
        <td>Row 1 Column 3</td>
      </tr>
      <tr>
        <td>Row 2 Column 1</td>
        <td>Row 2 Column 2</td>
        <td>Row 2 Column 3</td>
      </tr>
    </table>


A row can decide to span over 2 or more columns, using the `colspan` attribute.

Or it can span over 2 or more rows, using the `rowspan` attribute.

You can add a `th` tag as the first element inside a `tr` that’s not the first tr of the table, to have row headings.

You can add 3 more tags into a table, to have it more organized. 

This is best when using big tables. And to properly define a header and a footer, too.

These tags are:
`thead`, `tbody`, `tfoot`

They wrap the `tr` tags to clearly define the different sections of the table. Here’s an example:

    <table>
      <thead>
    	   <tr>
    	      <th></th>
    	      <th>Column 2</th>
    	      <th>Column 3</th>
    	   </tr>      
      </thead>
      <tbody>
         <tr>
    	     <th>Row 1</th>
    	     <td>Column 2</td>
    	     <td>Column 3</td>  
        </tr>
        <tr>
    	     <th>Row 2</th>
    	     <td>Column 2</td>
    	     <td>Column 3</td>  
        </tr>
      </tbody>
      <tfoot>
          <tr>
             <td></td>
             <td>Footer of Col 2</td>
             <td>Footer of Col 3</td>
          </tr>
      </tfoot>
    </table>

A table should have a `caption` tag that describes its content. That tag should be put immediately after the opening table tag.