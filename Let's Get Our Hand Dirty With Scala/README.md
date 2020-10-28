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

### Scala Nested if-else statement:

When an if else statement is present inside the body of another “if” or “else” then this is called nested if else
Syntax:
```
if(condition1){
// If block statements to be executed
if(condition2){
// If block statements to be executed
} else {
// Else bock statements to be executed
}
} else {
// Else bock statements to be executed
}
```
Example:
```
var Resume:String = "selected"
var interview:String = "not clear"
if(Resume == "selected") {
println("Welcome to Status Neo")
  if(interview == "clear")
println("congratulation,you are selected!")
  else
println("Sorry,not selected")
} else
println("Sorry,not selected")
```
Output:

![image018](https://user-images.githubusercontent.com/46487696/97302453-1f4d3980-187f-11eb-8117-18dbb9a838b0.png)
![image020](https://user-images.githubusercontent.com/46487696/97302460-2116fd00-187f-11eb-9bb4-1e30b582743a.png)

### Scala If-else-if ladder statement:

Flowchart:

![image022](https://user-images.githubusercontent.com/46487696/97302631-5885a980-187f-11eb-93c0-5559c9455ecc.png)

Here if-else-if ladder executes one condition among the multiple conditional statements

Syntax :
```
if (condition1){    
//Code to be executed if condition1 is true    
} else if (condition2){    
//Code to be executed if condition2 is true    
} else if (condition3){    
//Code to be executed if condition3 is true    
}    
...    
else {    
//Code to be executed if all the conditions are false    
}
```
Example :
```
var  resume:String ="selected not"
if( resume == "selected" ){
println("Welcome to Status Neo")
} else if( resume == "not selected" ){
println("Sorry, not selected")
} else if( resume == "in process" ){
println("waiting....")
} else{
println("This is else statement")
}
```

Output :

![image024](https://user-images.githubusercontent.com/46487696/97302875-a26e8f80-187f-11eb-8f06-e1c185d98a71.png)
![image026](https://user-images.githubusercontent.com/46487696/97302879-a39fbc80-187f-11eb-965e-8f5e5cc40020.png)
![image028](https://user-images.githubusercontent.com/46487696/97302894-a9959d80-187f-11eb-845d-4193bbca8e03.png)


## SCALA - Loops:

* There basically three types of loops which include
  * While loop
  * Do-While loop
  * For loop

### While-Loops =>

This loop is used to iterate code till the specified condition is true. It iterates again and again. You can use while loop if you don't know number of iterations prior.

**Flowchart:**

![image030](https://user-images.githubusercontent.com/46487696/97478924-a54cab80-1977-11eb-8dfd-a598d7372b4c.jpg)

Syntax :
```
While(Condition){ 
 // Statements to be executed  
} 
```
Example:

```
object loops {
  def main(args: Array[String]) {
    var a = 2;                       // Initialization
println("Table of 2")
    while( a<=20 ){                // Condition
println("Status Neo: "+a)
      a = a+2                        // Incrementation
    }
  }
}
```

Output:

![image032](https://user-images.githubusercontent.com/46487696/97479028-c8775b00-1977-11eb-8e8a-5954e3f776e2.png)

### Scala Do-while loop

This loop is similar to a while loop, except that it is confirmed to execute at least one time, because do...while loop checks its condition at the bottom of the loop.

Flowchart:

![image034](https://user-images.githubusercontent.com/46487696/97479127-e644c000-1977-11eb-9725-d5a2d4058c0c.jpg)

Syntax :
```
Do { 
 // Statements to be executed  
}
While(Condition)
```

Let's Try an Example =>

```
object loops {
  def main(args: Array[String]) {
    var a = 2;                       // Initialization
    do{
println("Status Neo: "+a)  //statement
      a = a+2
    }
    while( a<=20 )             // Condition
println("table of 2")
  }
}
```

Output :

![image036](https://user-images.githubusercontent.com/46487696/97479376-2a37c500-1978-11eb-9ffa-a14823d95011.png)

### Scala For-loop

This for loop is known as for-comprehensions. It is used to iterate, filter and return an iterated collection.

Syntax :
```
for ( i <- range){  
// statements to be executed  
} 
```

* We can implement for loop in Scala in many ways like using until keyword, to keyword, yield keyword, by keyword. We can also use it to filter our dataor to iterate in collections.

### Scala for -loop using until keyword

Let's Try an Example =>

object loops {
  def main(args: Array[String]) {
    for( x <- 0 until 5){
println("Value of X: "+x)
    }
  }
}

Output:

![image038](https://user-images.githubusercontent.com/46487696/97479576-64a16200-1978-11eb-8e59-42a6b17daf7c.png)

### Scala for-loop using yield keyword:

In this case we have used yield keyword this keyword returns a result after it completes the full loop of iterations. The for-loopuse buffer internally to store iterated result and when all iterations are completed it yields the final result from that buffer. It is slightly different from other loops

Let's Try an Example =>
```
object loops {
  def main(args: Array[String]) {
println("table of 5:")
    var output = for( x <- 5 to 50 if x%5==0) yield x
    for(y<-output){
println(y)
    }
  }
}
```

Output:

![image042](https://user-images.githubusercontent.com/46487696/97479916-bb0ea080-1978-11eb-8ed8-f2d92b5d4e5c.jpg)

