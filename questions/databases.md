# Databases interview questions

<table>
   <tr>
      <td>⚠️</td>
      <td>
         The answers here are given by the community. Be careful and double check the answers before using them. <br>
         If you see an error, please create a PR with a fix
      </td>
   </tr>
</table>

### What is 'nested loops join'?

It's a basic approach databse engine takes to join two tables: for every value (external loop) of the 'left' table's join key column, the engine loops (inner loop) over the values of the 'right' table's join key column and selects the matching rows. This approach is basic and has the time complexity of O(n**2).

Reference:
- https://use-the-index-luke.com/sql/join/nested-loops-join-n1-problem
- https://www.youtube.com/watch?v=WfuLUE7lccs

ID: 1AF0D60C-F02E-4EDB-9D97-3982216FA788

Last updated: 2020-05-18

### What is 'hash join'?

Hash join is an optimizaton approach database engine may take to speed up a process of tables join. In this case, a in-memory hash table(s) is being generated using the values of the 'left' table's join key column(s). The hash table values are used afterward to find matching rows of the 'right' table. 

The hash join approach is faster compared to the nested loops join, it however has a limitation: whole hash table must fit into memory of the database machine. Another pro of hash join is, one doesn't need to index join key columns.

The time complexity of such algorithm is O(n_left + n_right), where n_left = number of 'left' table's rows,  n_right = number of 'right' table's rows."

References:
- https://use-the-index-luke.com/sql/join/hash-join-partial-objects
- https://www.youtube.com/watch?v=mlokdBiaMek

ID: C048455B-87FC-442F-97C5-B14DF96CEFEF
Last updated: 2020-05-18