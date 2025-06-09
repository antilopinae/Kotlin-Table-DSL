# Kotlin Table DSL
> Kotlin Table DSL is a declarative mini Domain Specific Language that allows you to conveniently describe tables with columns and rows directly in Kotlin code.

## Examples
~~~
table {
    column("ID", Int::class)
    column("Name", String::class)
    column("Age", Int::class)
	
    row {
        cell("ID", 1)
        cell("Name", "Alice")
        cell("Age", 25)
    }
    row {
        cell("ID", 2)
        cell("Name", "Bob")
        cell("Age", 30)
    }
}.render()
~~~
## Expected Result:
---
~~~
+----+-------+-----+
| ID | Name  | Age |
+----+-------+-----+
|  1 | Alice |  25 |
|  2 | Bob   |  30 |
+----+-------+-----+
~~~

## License
[MIT License](LICENSE)
