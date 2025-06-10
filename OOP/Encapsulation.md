Some data and functionality of a class must not be accessible to all. This allows from accidental or wrong usage and provides easier maintenance. Access specifiers provide restrictions on access; they are:
- **Public** - applied to classes, variables, and methods; it is accessible to all.
- **Private** - applied to variables and methods, its accessible to the class only, not [[Inheritance|inheritable]]
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
