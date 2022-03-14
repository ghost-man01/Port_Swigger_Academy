This method evolves *UNION SELECT* payload specifying different number of null values.
> ' UNION SELECT NULL--<br>
> ' UNION SELCT NULL,NULL--<br>
> ' UNION  SELECT NULL,NULL,NULL<br>

- If the number of *Null* doesn't match the number of columns, database returns an error.

### Result

-  The application return error in HTTP response
-  Generic error
-  No result returned
* NullPointerException error
* Worst case is response might be indistinguishable 