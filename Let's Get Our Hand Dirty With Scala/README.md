## Scala Variable and DataTypes

### Variables:
* They are nothing but reserved memory locations to store values. Which means when you create a variable, you reserve some space in memory.
* We can declare a variable in two ways
  * Var(Mutable variable) 
  * Val (Immutable variable)

Var is a keyword. It’s a mutable reference to a value. Since it’s mutable, its value can change throughout the program. 
On the other side, val keyword represents a value. It’s an immutable reference, meaning that its value never changes. Once assigned it will always keep the same value

Example Using “var keyword”
```
var company = "Status Neo"
print(company)
company ="Neo"
print(company)

// No Error
```

Output :

![image004](https://user-images.githubusercontent.com/46487696/97300792-eca24180-187c-11eb-842c-e45e54fb5a8a.png)


Example Using “val keyword”

```
val company = "Status Neo"
print(company)
company ="Neo"
print(company)

// it will show the Error
```
Output:

![image006](https://user-images.githubusercontent.com/46487696/97300918-13607800-187d-11eb-985e-bb9662a23001.jpg)

### Data Types
```
DATA        TYPE	        DEFAULT VALUE	SIZE
Boolean	    False     	True or false
Byte	      0	          8 bit signed value (-27 to 27-1)
Short	      0         	16 bit signed value(-215 to 215-1)
Ch	      '\u0000'      	16 bit unsigned Unicode character(0 to 216-1)
Int       	0         	32 bit signed value(-231 to 231-1)
Long      	0L          	64 bit signed value(-263 to 263-1)
Float     	0.0F	      32 bit IEEE 754 single-precision float
Double	    0.0D	      64 bit IEEE 754 double-precision float
String	    Null	      A sequence of characters
```

## Scala Conditional Expressions:

* There basically four types of conditions which include
  * If statement
  * If-else statement
  * Nested if-else statement
  * If-else-if ladder statement
  
### Scala if statement:
Flowchart:

![image008](https://user-images.githubusercontent.com/46487696/97301365-b0231580-187d-11eb-9b1b-a6c17004756f.jpg)

here if condition is only executed if condition block is true.

Syntax:
```
if(condition){  
 // Statements to be executed  
}
```


Example:
```
var Resume:String = "selected"
if(Resume == "selected"){
println("Welcome to Status Neo")
}
```

Output:

![image010](https://user-images.githubusercontent.com/46487696/97301533-e6609500-187d-11eb-9333-110723015b3e.jpg)

### Scala If-Else Statement
Flowchart :

![image012](https://user-images.githubusercontent.com/46487696/97301639-01cba000-187e-11eb-9862-9cafd254decb.jpg)

Here if the condition is true then the if block will execute otherwise the else block

Syntax:

```
if(condition){
// If block statements to be executed
} else {
// Else bock statements to be executed
}
```
Note: If there is just one condition we don’t need to provide braces

Example:

```
var Resume:String = "not selected"
if(Resume == "selected")
println("Welcome to Status Neo")
else
println("Sorry,not selected")
```

Output:

![image014](https://user-images.githubusercontent.com/46487696/97301918-5b33cf00-187e-11eb-8a2f-242467d1271e.png)
![image016](https://user-images.githubusercontent.com/46487696/97301928-5ec75600-187e-11eb-9369-1f4a49efffd4.png)

