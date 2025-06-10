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