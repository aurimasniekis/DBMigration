DBMigration
===========

XML Version of migration file
--
```xml
<?xml version="1.0" encoding="UTF-8"?>
<migration name="add_column_title" date="201309200947">
    <up>
        <addColumn table="users" name="title" type="string" null="false" default="Pavadinimas" />
    </up>
    <down>
        <removeColumn table="users" name="title" />
    </down>
</migration>
```

Javascript Version of migration file
--
```javascript
migration("201309200947_add_column_title", function(m){
  m.up = function(db) {
  	db.addColumn("users", "title", "string", "Pavadinimas", false);
  }
  
  m.down = function(db) {
  	db.removeColumn("users", "title");
  }
});
```

JSON Version of migration file
--
```json
{
  "name": "201309200947_add_column_title",
  "up": {
      "add_column": {
          "table": "users",
          "name": "title",
          "type": "string",
          "default": "Pavadinimas",
          "null": false
      }
  },
  "down": {
      "remove_column": {
          "table": "users",
          "name": "title"
      }
  }
}
```
