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

## Scala Functions:
* As already told Scala supports functional programming approach. This language also gives us a great set of built-in functions and not only this we can also create user defined functions.
* In Scala, we can store function value, pass function as an argument and return function as a value from other function. 
* def keyword is used to define a function, but we have to keep one thing in mind while defining a function Is that we must give a return type of parameters while defining function and return type of a function is optional.
* Also, functions are a first-class value in Scala. ... It means that functions can be passed as arguments to other functions, and functions can return other functions

Syntax:

```
def FunctionName(parameters : typeofparameters) : returntypeoffunction = {  
// statements to be executed  
}  
```
* we can create function with or without = (equal) operator. If we use it, function will return value. If we don't use it, our function will not return anything.

### NON-PARAMETERIZED
* Scala Function Example WITHOUT using = Operator

Let's Try an Example =>

```
object functions {
  def main(args: Array[String]) {
WithouEqualTo()           // Calling function
  }
  def WithouEqualTo()  {        // Defining a function
println("Scala Function Example without using = Operator")
  }
}
```
Output :

![image044](https://user-images.githubusercontent.com/46487696/97480227-248eaf00-1979-11eb-83ba-05388dfd61f2.jpg)

* Scala Function Example WITH using = Operator

Let's Try an Example =>

```
object functions {
  def main(args: Array[String]) {
WithouEqualTo()           // Calling function
  }
  def WithouEqualTo()  {        // Defining a function
println("Scala Function Example without using = Operator")
  }
}
```
OutPut:

![image046](https://user-images.githubusercontent.com/46487696/97480368-4f790300-1979-11eb-8b98-b643b28641d6.jpg)

### PARAMETERIZED
* when using parameterized function we must mention type of parameters explicitly otherwise compiler throws an error and your code fails to compile.
Let's Try an Example =>
```
object functions {
  def main(args: Array[String]) {
Parameterized("Status Neo")
  }
  def Parameterized(x:String): Unit = {
val a = x
println("Company name is: " +a)
  }
}
```
OutPut:

![image048](https://user-images.githubusercontent.com/46487696/97480577-9cf57000-1979-11eb-8ce4-ba07f9f78712.jpg)

### Scala Higher Order Functions:

These are the functions that either takes a function as argument or returns a function. In simple language function which works with function are called higher order function. Using these functions, we can create function composition, lambda function or anonymous function etc.

**Passing a Function as Parameter in a Function :**

In this type of scenario, we pass a function in another function as a parameter you can see the example for better understanding

Let's Try an Example =>
```
object HigherOrderFunction {
  def main(args: Array[String]): Unit = {
Statusneo("Status ", add)                   // Passing a function as parameter
  }
  def Statusneo(x:String, f:String=>String):Unit = {
println(f(x))                                   // Calling that function
  }
  def add(x:String):String = {
x+"Neo"
  }
}
```
Output:

![image050](https://user-images.githubusercontent.com/46487696/97480788-e940b000-1979-11eb-81f7-9e7628b27438.jpg)

### Function Composition:

* This is a process of composing in which a function represents the application of two composed functions, lets understand it better with an example.

Let's Try an Example =>

```
object HigherOrderFunction {
  def main(args: Array[String]) = {
    var output = multiplyBy100(sub5(15))      // Function composition
println("Final result: "+output)
  }
  def sub5(x:Int):Int = {
    x-5
  }

  def multiplyBy100(x:Int):Int = {
    x*100
  }
}
```
OutPut:

![image052](https://user-images.githubusercontent.com/46487696/97480925-11c8aa00-197a-11eb-842e-4a2209a3c8e4.jpg)

### Function Currying

* Let’s suppose we have a function with multiple parameter list. But we called the function with fewer parameter lists, then it will yield a function taking the missing parameter lists as its arguments.
* In simple terms it is a process of transforming a multiple argument taking function into single argument taking. 
* Let’s understand it with an example

Example:
```
object HigherOrderFunction {
  def sum(x:Int)(y:Int):Int = {
x+y
  }
  def main(args: Array[String]):Unit = {
    //normal function
    var output = sum(2)(3)
println("sum of the numbers are: "+output)

    // function currying
    var add = sum(5)_  //Here, only the ‘_’ is added after the calling the function add for value of sum

    var output1 = add(2)
println("sum of the numbers are: "+output1)
  }
}
```

OutPut :

![image054](https://user-images.githubusercontent.com/46487696/97481109-56544580-197a-11eb-9f42-3e4833ad90c3.jpg)


## Scala OOPS Concept:

### Scala- Object and Classes

* An object is a real-world entity. It is also known as a runtime entity. An object can be created using a new keyword. A class is a blueprint for objects. Once the class is defined, can create objects to access all functionalities of the defined class. It is public by default. Class variables are known as fields.

Example :
```
class Employee{
  var id: Int = 0;                         // fields 
  var name: String = null;
}
object MainObject{
  def main(args:Array[String]){
    var e = new Employee()               //  object   
println(e.name);
  }
}  
```

Output :

![image055](https://user-images.githubusercontent.com/46487696/97593299-8efe2880-1a27-11eb-8467-849826b2c91a.png)

* A constructor with arguments is known as a primary constructor. Let's see an example of passing the values to the constructor.

Example:
```
class My_class (no: Int, Name: String){  // Primary Constructor

def display() {     // Class methiod
println(no +" "+ Name)

	}
}

object MainObject{
def main(args:Array[String]){

 var m = new My_class(116 , "Kushagra")    // Constructor values
m.display()

  }
}
```
Output :

![image056](https://user-images.githubusercontent.com/46487696/97593488-c076f400-1a27-11eb-84f0-4dba2ea2feeb.png)


### Class Extending and Overriding

* Like java, Scala can inherit another class too with two restrictions. In the case of method overriding, we required the ‘override’ keyword and the Primary constructor is the only constructor that can pass the arguments to the base constructor. Scala does not allow multiple inheritances.

Example :
```
class cars (valgearVal:Int, valspeedVal: Int)
{
  var gear: Int = gearVal	// field
  var speed: Int = speedVal   // field

  def gearcheck(dec: Int)	// method
  {
gear = gear - dec
println("gear efficiency will be: " + gear);
  }
  def range(inc: Int)
  {
speed = speed + inc;
println("new speed range is : " + speed);
  }
}
class sportscar(override valgearVal: Int,
                   override valspeedVal: Int,
valairbagsVal : Int)
  extends cars(gearVal, speedVal)   // derived class

{
  var airbags: Int = airbagsVal

  def addbags(newVal: Int)
  {
airbags = airbags + newVal
println("new airbags available : " + airbags);
  }
}
object MainObject
{
  def main(args: Array[String])
  {
val bike = new sportscar(10, 20, 15);
bike.addbags(5);
bike.range(100);
bike.gearcheck(5);
  }
} 
```

```
Note: In this program, a copy of all methods and fields of the parent class acquire memory in this object when the object of a sportscar(derived class) is created.
```

Output :

![image059](https://user-images.githubusercontent.com/46487696/97593934-29f70280-1a28-11eb-8f4b-babf20b20161.png)

### Anonymous object:

* An object without any reference name is known as an Anonymous object. It makes code shorter and more understandable. It’s good when you would prefer not to reuse it further.

Example :
```
class Cal{
  def add(x:Int, y:Int){
    var add = x+y;
println("result : " +add);
  }
}

object MainObject{
  def main(args:Array[String]){
    new Cal().add(10,10);

  }
}  
```

Output:

![image061](https://user-images.githubusercontent.com/46487696/97594097-54e15680-1a28-11eb-96d5-8abdee3534e5.png)

### Scala Singleton Object

Unlike java having static concept, Scala use Singleton object means no object is required , Methods can be call directly. Method inside this singleton Object can be access globally . As Earlier, we have seen Scala class extend means class inherited by another class. Here Singleton Object can also extend the class.

Note: Scala is pure object-oriented programming than java. You cannot pass the parameters to any Singleton object. You can have Multiple Singleton object in a program.	

Example :
```
object Mainobject{
  def main(args:Array[String]){
    Mainobject1.LetsDo()        // no object required
  }
}


object Mainobject1{
  def LetsDo(){
println("OH! you just create a Singleton Object")
  }
}  
```
Output :

![image062](https://user-images.githubusercontent.com/46487696/97594348-996cf200-1a28-11eb-84a2-8baaecd1d190.png)


### Scala Companion Object:

* In a Scala program, Scala class and Singleton object name are the same it is called a Companion Object. The object must be required to call the method inside the Companion object.

Example :
```
object Mainobject{
  def main(args:Array[String]){
    Mainobject1.LetsDo() // no object required

    Mainobject2.LetsDo()
val o = new Mainobject2()
o.LetsDo();
    new Mainobject2().LetsDo()
  }
}


object Mainobject1{
  def LetsDo(){
println("OH! you just create a Singleton Object")
  }
}
object Mainobject2{
  def LetsDo(){
println("OH! you just create a Singleton Object")
  }
}

class Mainobject2{
  def LetsDo(){
println("OH! you just create a Singleton Object")
  }
}
```

Output:

![image064](https://user-images.githubusercontent.com/46487696/97595001-42b3e800-1a29-11eb-99f4-4ed9b8207c53.png)


## This Keyword

This operator invokes the Primary Constructor as well as can be used to refer to the instance variables.

Example :
```
class Project(P_name: String  )
{
  // Using this keyword
  def this(P_name:String, R_Team:String )
    {
      this (P_name)
println("Project Title :  " + P_name +
        "\nRole of team members are :  " + R_Team )
    }
}

object MainObject
{
  def main(args: Array[String])
  {
      var p = new Project( "Scala Blog", "Developer evangelist")
  }
}
```

This operator invokes the Primary Constructor.

Output :

![image070](https://user-images.githubusercontent.com/46487696/97886722-f5988480-1d4e-11eb-9aba-21f3767de46b.png)

Example-2 :
```
class Project
{
  var P_name: String = ""
  var R_Team:String  = ""
  // Using this keyword

  def this(P_name:String, R_Team:String ) {
    this()
this.P_name= P_name        // Refering the variable
this.R_Team= R_Team
  }
  def display()
  {
println("Project Title :  " + P_name+
      "\nRole of team members are :  " + R_Team)
  }
}
object MainObject
{
  def main(args: Array[String])
  {
    var p = new Project( "Scala Blog", "Developer evangelist")
p.display()
  }
}
```

Output :

![image071](https://user-images.githubusercontent.com/46487696/97886751-034e0a00-1d4f-11eb-988a-cdfb18377452.png)

## Scala Method Overloading

> It helps to define methods of the same name with a different number of parameters and data types to customize the code.
But it only permits to define of the method of an identical name within a class. Here also we can change the type of the data type of the parameters.

Example :
```
class Statusneo{
  def add(name:String, age:Int){
println(name + " " + age)
  }
  def add(name:String, age:Double, branch:String){

println(name + " " + age + " " + branch)
  }
}
object MainObject{
  def main(args:Array[String]){
    var a  = new Statusneo();
a.add("sumyak",19);
a.add("Kushagra",19,"CSE-DevOps");
  }
}
```
Output:

![image072](https://user-images.githubusercontent.com/46487696/97886771-0cd77200-1d4f-11eb-8e17-b57ff39140ac.png)


## Scala Method Overriding

> The first method with both Val or var can override. Subclass always overrides the method of the superclass that’s the rule.

> Second, the override keyword is used to override that method which also belongs to a superclass.

> Third, if the method parameter data type is Val we can’t change it to var It will throw an error.

Example:
```
class Statusneo{
  def result(){
println("Are you here for the interview")
  }
}

class interview extends Statusneo{
  override def result(){
println("You are the part of this intern now ")
  }
}

object MainObject{
  def main(args:Array[String]){
    var b = new interview()
b.result()
  }
}
```

Output:

![image073](https://user-images.githubusercontent.com/46487696/97886801-18c33400-1d4f-11eb-9453-ad712a80a9b4.png)


## Scala Field Overriding:

> This is The Best Thing in Scala, We can Override the field but which are immutable i.e type ‘Val’. Because Val Is only readable and we can override it to a particular class to customize our code. Here also ‘override’ annotation is required. 

> In the field, as we cannot override mutable value but also we cant override an Immutable value to a mutable value. (Like Val to override var ). The system will throw an error.

Example =>

```
class Statusneo{
valrate:Int = 60
}
class Github extends Statusneo{

  override valrate:Int = 100
  def show(){
println("Rank yourself in github : " + rate)
  }
}
object MainObject{
  def main(args:Array[String]){
    var g = new Github()
g.show()
  }
}
```
Output :

![image074](https://user-images.githubusercontent.com/46487696/98266737-a81b5200-1fb0-11eb-8cfb-ca0e2841422a.png)

## Scala Final :

> It’s used to avoid a descent into the derived class of superclass members. The final keyword can be used by fields, Methods, and Classes.

Syntax :
* Final val s:Int 
* Final  def show(){  }
* Final class Class_name { }

Example =>
```
class Statusneo{
  final valrate:Int = 60
}
class Github extends Statusneo{

  override valrate:Int = 100
  def show(){
println("Rank yourself in github : " + rate)
  }
}
object MainObject{
  def main(args:Array[String]){
    var g = new Github()
g.show()
  }
}
```
> Here this will throw an error as the final variable is inherited to sub-class Github. The same goes for Class Methods and Classes.

Output :

![image075](https://user-images.githubusercontent.com/46487696/98266951-ddc03b00-1fb0-11eb-81de-83a520754785.png)


## Scala Inheritance :

> Inheritance use the concept of reusability. A class can be extent (super class) to a sub class to use the features of the class. A child class or sub class can have only one super class. “extends” keyword is used to inherit the class.

Types of inheritance =>

* Single Inheritance				* Multilevel Inheritance
* Hierarchical Inheritance 			* Hybrid Inheritance
* Multiple Inheritance	

> Multiple & Hybrid Inheritance are not allowed in scala as only one class can be extend to the child class at a time. Though, can be achieve by Traits which have been explained in Scala-trait

Let’s try an Example =>

```
 class Stausneo
{
    var Name: String = "You are Kushagra."
}
class Introduction extends Stausneo
{
    var intro: String = "Tell me about yourself not the CV which i have already gone through"
}

class LetsStart extends Introduction
{
    def Display(){
        print("Okay then lets start Mr ")
        println(Name)
        print(intro)
    }
}
object MainObject
{
    def main(args: Array[String])
    {
        val S = new LetsStart();
        S.Display();
    }
}
```
Output :

![image077](https://user-images.githubusercontent.com/46487696/98267291-38599700-1fb1-11eb-8fe0-7e23f23e309c.png)

