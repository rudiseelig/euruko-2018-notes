### Trees
 * getting descendants
 * getting ancestors
 * deleting/counting/updating/...
 => everything very complex -> anti pattern

#### Possible solutions
  * closure trees: https://github.com/ClosureTree/closure_tree
  * materialized path: https://github.com/stefankroes/ancestry

### Polymorphic Relationships
 * No foreign key -> No fk constraints
 * No cascading delete
 * wastes a lot of space (type column)

#### Possible solutions
   * separate tables (don't combine all into one)
   * one table with multiple foreign keys (for all related tables)
     -> many indexes
     -> more migrations
  * base parent table (kinda like inheritance)
    * DRY
    * 2 joins
    * 1 way street
    * still error prone


 * in general: 
 
   * performance vs simplicity
   * correctness vs convenience
