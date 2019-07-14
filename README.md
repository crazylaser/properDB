```javascript
<script>
    createSql = 'CREATE TABLE "todo" ( "id"  INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL, "text"  TEXT, "flag"  INTEGER, "rowno"  INTEGER, "data"  TIMESTAMP DEFAULT (datetime(\'now\',\'localtime\')) )'
    myTable = new properDB().getTable("todo",createSql);
</script>

<!--user orm-->
myTable.get("flag = 1",function(result) {
            for (var i = 0; i < result.length; i++) {
                var text = result[i].text;
                $("#ullist").prepend("  <li><span><i class=\"fa fa-trash-o\"></i></span>" + text + "</li> ");
            }
        });

<!--use Sql-->
t.execute("Select * from xxx", function (results) {}
```
数据库位置为
用navicat查看Chrome\User Data\Default\databases\Databases.db 

对应“mydbname”的名字 在下级的file__0目录下（实质是sqlite）



