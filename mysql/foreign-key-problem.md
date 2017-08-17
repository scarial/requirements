# Foreign key problem when updating a table field
When we need to update a field in a database, the following problem can happend :
```
Error Code: 1833. Cannot change column 'person_id': used in a foreign key constraint 'fk_fav_food_person_id' of table 'table.favorite_food'
```

#### Link to found solution :
https://stackoverflow.com/questions/13606469/cannot-change-column-used-in-a-foreign-key-constraint

## There are 2 ways to resolve this:
### In Production
The type and definition of foreign key field and reference must be equal. This means your foreign key disallows changing the type of your field.

One solution would be this:
```
LOCK TABLES 
    favorite_food WRITE,
    person WRITE;

ALTER TABLE favorite_food
    DROP FOREIGN KEY fk_fav_food_person_id,
    MODIFY person_id SMALLINT UNSIGNED;
```
Now you can change you person_id
```
ALTER TABLE person MODIFY person_id SMALLINT UNSIGNED AUTO_INCREMENT;
recreate foreign key

ALTER TABLE favorite_food
    ADD CONSTRAINT fk_fav_food_person_id FOREIGN KEY (person_id)
          REFERENCES person (person_id);

UNLOCK TABLES;
```

You have to disallow writing to the database while you do this, otherwise you risk data integrity problems.

### In Development (Because can induce data integrity problems)

SET FOREIGN_KEY_CHECKS = 0;

/* DO WHAT YOU NEED HERE */

SET FOREIGN_KEY_CHECKS = 1;
