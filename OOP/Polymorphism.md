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
Objects which are instances of a [[Inheritance#^7506bd|subclass]] can overwrite the inherited methods with their own version, providing different implementations of a [[Inheritance#^ebdbb2|superclass]] method. 
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
   
   /** Constructs a Rectangle instance 
   with the given color, length and width */
   public Rectangle(String color, int length, int width) {
      /*This keyword calls its parent class
       constructor method field */
      super(color);
      this.length = length;
      this.width = width;
   }

   /** Override the inherited getArea() to provide the proper implementation for rectangle */
   @Override
   public double getArea() {
      return length*width;
   }
   // However there's no implementation fo the getPerimeter function, thus the class will ignore its existence.
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