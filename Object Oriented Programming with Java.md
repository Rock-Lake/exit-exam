# Introduction
Structured Programming involves organizing processes into procedures that perform a specific task. This raises the following limitations:
- **Tight coupling:** any changes in one part of the code can affect the entire program.
- **Poor Real-world Modeling:** functions and data are unrelated to the state of real-world provide a poor model of the real world.
- **Limited Data Type:** the traditional data types may not be enough for real scenarios.
- **Tight memory management:** procedural code often requires manual memory management, which can lead to memory leaks

Object oriented programming allows the programmer to break down a program into self contained entities that hold both data and operations called **Objects**.

Here are the basic concepts of object-oriented programming:
## Objects
Objects is a model of any entity with specific state, behavior and identity. This object is an instance of a class that is available during runtime.The variables inside an object are called **instance variables** and the functions are called **methods**.


## Class
To create (instantiate) an object, a **class** is required. A class is the definition of a set of objects consisting of a class name, data and functionality. A defined class is a user-defined [[Variables#^c136b3|datatype]] that behaves similar to built-in datatypes. 
Classes that require variables or methods with a single common value/function can be defined using **static** keyword. This allows for maintaining all objects state and/or behavior across its execution.

**NB:** static methods can only run on static variables.

During the instantiation of a class, there is a piece of code called **constructor** that automatically initializes the variables in the object. Usually, the default values are 0 and all references are NULL. However, complex classes require a custom constructor. The syntax is as follows:
```java
public class MyClass {
    private int myField;

    public MyClass(int field) {
    //This is a constructor, they can't be hidden, inherited or overloaded.
        myField = field;
    }

    public void printField() {
        System.out.println(myField);
    }
}
```
The constructor has the same name as the class and initialize the variables. However a simpler way is the following:
```java
public class MyClass {
    private int myField;

    public MyClass(int myField) {
    //This is a constructor, they can't be hidden, inherited or overloaded.
    // By using "this" keyword, it refers to all instance variables in the class
        this.myField = myField;
    }

    public void printField() {
        System.out.println(myField);
    }
}
```

## Data Abstraction
The instantiation of an object doesn't require the programmer to understand the underlying working of the class, simplifying its use. Classes that use this property called **abstraction** are known as [[Data Structures and Algorithms#^035aa0|Abstract Data Type]].

## Encapsulation
Some data and functionality of a class must not be accessible to all. This allows from accidental or wrong usage and provides easier maintenance. Access specifiers provide restrictions on access; they are:
- **Public** - applied to classes, variables, and methods; it is accessible to all.
- **Private** - applied to variables and methods, its accessible to the class only, not [[inheritable]]
- **Protected** - applied to variables and methods; it is accessible to classes, subclasses in the same package
- **Default** -  applied to classes, variables and methods; it is accessible to the parent class and the same package

**NB:** Classes with variables that have the *private* modifier require special methods to retrieve and/or set the values after instantiation.The following is its implementation:
```java
class MyClass {
    private int myField;

    public MyClass(int myField) {
    //This is a constructor, they can't be hidden, inherited or overloaded.
    // By using "this" keyword, it refers to all instance variables in the class
        this.myField = myField;
    }
    //This method returns the value of myField from outside the class
    void int getMyField(){
	    return myField;
	}
	//This method sets the value of myField to the given parameter from outside the class
	void int setMyField(int myField){
		this.myField = myField;}
    public void printField() {
        System.out.println(myField);
    }
}
public class App{
	public static void main(String[] args){
		MyClass test = new MyClass(4);
		System.out.println(test.getMyField());
		test.setMyField(2);
		System.out.println(test.getMyField());
	}
}
```
An instantiated class acts as a new datatype, where its variables and methods are accessed using the dot (.) operator.

## Inheritance
There are two ways to _reuse_ existing classes, namely, _composition_ and _inheritance_. With _composition_ (aka _aggregation_), you define a new class, which is composed of existing classes. With _inheritance_, you derive a new class based on an existing class, with modifications or extensions.

The existing class is called **parent/superclass** and the the new class is called **derived/subclass**. ^ebdbb2

The subclass inherits all non-private methods and fields from the superclass, including the constructor. This means the constructor of the subclass must call the superclass constructor using the **super** keyword. ^7506bd
```java
/**
 * Superclass Shape maintain the common properties of all shapes
 */
public class Shape {
   // Private member variable
   private String color;
   
   /** Constructs a Shape instance with the given color */
   public Shape (String color) {
      this.color = color;
   }
   /** All shapes must provide a method called getArea() */
   public double getArea() {
      // We have a problem here!
      // We need to return some value to compile the program.
      System.err.println("Shape unknown! Cannot compute area!");
      return 0;
   }
   public double getPerimeter() {
	   System.err.println("Shape unknown! Cannot compute perimeter!")
	   return 0;
	}
}
//The Rectangle class, subclass of Shape
public class Rectangle extends Shape {
   // Private member variables
   private int length, width;
   
   /** Constructs a Rectangle instance with the given color, length and width */
   public Rectangle(String color, int length, int width) {
      super(color);//This keyword calls its parent class constructor/method/field
      this.length = length;
      this.width = width;
   }

   /** Override the inherited getArea() to provide the proper implementation for rectangle */
   @Override
   public double getArea() {
      return length*width;
   }
}
public class App{
	public static void main(String[] args){
		Rectangle fence = new Rectangle("Red", 4, 6);
		/* This will return 24 as area. If this function wasn't overriden 
		it will display a "Shape unknown! Cannot compute area!" message */
		fence.getArea();
	}
}
```
There can be a chain of inherited classes, such as **multi-level, hierarchical, or hybrid inheritance**. However, a class can't inherit more than one superclass at a time that don't have a common grandparent class.

To check if an object is an instance of a subclass or a superclass we can use the **instanceof** operator; this returns either true or false.The syntax is as follows:

`_anObject_ instanceof _aClass_`
## Polymorphism
Polymorphism is the ability of a function to respond in many different ways. This can be don using two methods:
### Method Overloading
Some objects can have methods with similar name, but different behavior; this is done using **method overloading**, where object methods are differentiated by its amount, type or sequence of parameters. This overloading can extend to **constructor overloading**, so that initializing classes can output different object based on the used parameters.
```java
class Box {
	double width, height, depth;
	// constructor used when all dimensions specified
	Box(double w, double h, double d) {
		width = w; height = h; depth = d;
	}
	// constructor used when no dimensions specified
	Box() {
		width = -1; height = -1; depth = -1;
	}
	// constructor used when cube is created
	Box(double len) {
	width = height = depth = len;
	}
}
```
### Method Overriding
Objects which are instances of a [[#^7506bd|subclass]] can overwrite the inherited methods with their own version, providing different implementations of a [[#^ebdbb2|superclass]] method. 
```java
/**
 * The superclass Monster defines the expected common behaviors for its subclasses.
 */
public class **Monster** {
   // private instance variable
   private String name;

   /** Constructs a Monster instance with the given name */
   public Monster(String name) {
      this.name = name;
   }

   /** Defines a common behavior called attack() for all its subclasses */
   public String attack() {
      return "!^_&^$@+%$* I don't know how to attack!";
      // We have a problem here!
      // We need to return a String; else, compilation error!
   }
}
public class **FireMonster extends Monster** {
   /** Constructs a FireMonster with the given name */
   public FireMonster(String name) {
      super(name);
   }
   /** Subclass provides actual implementation for attack() */
   @Override
   public String attack() {
      return "Attack with fire!"; 
   }
}
```
Some variables, methods and classes should be uninheritable/unmodifiable; we use the **final** keyword to do that.

**NB:** Some classes are too general to have concise fields/methods but other classes inherit that. This can be implemented using an Abstract class.
```java
/**
 * Superclass Shape maintain the common properties of all shapes
 */
abstract class Shape {
   // Private member variable
   private String color;
   
   /** Constructs a Shape instance with the given color */
   public Shape (String color) {
      this.color = coloir;
   }
   /** All shapes must provide  methods called getArea() and getPerimeter()*/
   abstract public double getArea();
   abstract public double getPerimeter();
}
//The Rectangle class, subclass of Shape
class Rectangle extends Shape {
   // Private member variables
   private int length, width;
   
   /** Constructs a Rectangle instance with the given color, length and width */
   public Rectangle(String color, int length, int width) {
      super(color);//This keyword calls its parent class constructor/method/field
      this.length = length;
      this.width = width;
   }

   /** Override the inherited getArea() to provide the proper implementation for rectangle */
   @Override
   public double getArea() {
      return length*width;
   }
   @Override
   public double getPerimeter(){
	   return 2*(length+width);
	}
}
public class App{
	public static void main(String[] args){
		Rectangle fence = new Rectangle("Red", 4, 6);
		/* This will return 24 as area. If this function wasn't overriden 
		it will display a "Shape unknown! Cannot compute area!" message */
		fence.getArea();
	}
}
```

Abstract classes with vague features that are somewhat common in multiple objects can be implemented using **interfaces**. Variables in interfaces are usually unmodifiable(final) and methods don't have inner scopes; this includes constructors.
```java
interface Shape
{ 
	void area ();
	void volume ();
	double pi = 3.14;
}
class Circle implements Shape
{ 
	double r;
	Circle (double radius){ 
		r = radius;
	}
	public void area (){
		System.out.println("Area of a circle is:" + pi*r*r );
	}
	public void volume (){
		System.out.println("Volume of a circle is:" + 2*pi*r);
	}
}
```
Java can mimic multiple inheritances using interfaces; by defining the implementation of the superclass methods in the subclass.