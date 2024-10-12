# MULTIPLE CHOICE QUESTIONS – PL2

## 1.Which of the following are correct?
   a) The native keyword indicates that the method is implemented in another language like C/C++  
   b) The only statements that can appear before an import statement in a Java file are comments.  
   c) The method definitions inside interfaces are public and abstract. They cannot be private or protected.  
   d) A class constructor may have public or protected keyword before them, nothing else.  

## 2.Which of the following are valid definitions of an application’s main() method?
   a) `public static void main();`  
   b) `public static void main ( String args );`  
   c) `public static void main ( String args[ ] );`  
   d) `public static void main ( Graphics g );`  
   e) `public static boolean main ( String args [ ] );`  

## 3.Abstract class cannot have final methods. True or false?
   a) True  
   b) False  

## 4.Name the keyword that makes a variable belong to a class, rather than being defined for each instance of the class. Select the one correct answer.
   a) static  
   b) final  
   c) abstract  
   d) native  
   e) volatile  
   f) transient  

## 5.Method Overriding is an example of
   a) Static Binding.  
   b) Dynamic Binding.  
   c) Both of the above.  
   d) None of the above.  

## 6.Can we have multiple classes in the same Java file?
   a) true  
   b) false  

## 7.Assume that class A extends class B, which extends class C. Also, all three classes implement the method test(). How can a method in class A invoke the test() method defined in class C (without creating a new instance of class C)? Select the one correct answer.
   a) test();  
   b) super.test();  
   c) super.super.test();  
   d) ::test();  
   e) C.test();  
   f) It is not possible to invoke the test() method defined in C from a method in A.  

## 8.Given the following code. 

    void func( ) {
        String str = null;
        try {
            if( str.length( ) == 0 ) {
                System.out.print(“The”);
            }
            System.out.print(“ Cow”);
        } catch (Exception e) {
            System.out.print(“ and”);
            System.exit(0);
        } finally {
            System.out.print(“ Chicken”);
        }
        System.out.println(“ show”);
    }


## What will be printed? Select the correct answer(s): 
   a) The  
   b) Cow  
   c) and  
   d) Chicken  
   e) show  

## 9.When does the finally block get executed?
   a) Always when the try block gets executed, no matter if an exception occurred or not.  
   b) Always when a method is executed, no matter if an exception occurred or not.  
   c) Always when a try block gets executed, if an exception does not occur.  
   d) Only when an exception occurs in the try block code.  


## 10.Consider the code below:

    void myMethod( ) 
    {
    try 
    {
    fragile( );
    } 
    catch ( NullPointerException npex) 
    {
    System.out.println( “NullPointerException thrown”);
    } 
    catch ( Exception ex) 
    {
    System.out.println( “Exception thrown “);
    }
    finally 
    {
    System.out.println( “Done with exceptions “);
    }
    System.out.println( “myMethod is done”);
What is printed to standard output if `fragile()` throws an IllegalArgumentException / NullPointerException? (2 DIFFERENT Q’S MIGHT APPEAR)
   a) “NullPointerException thrown”  
   b) “Exception thrown”  
   c) “Done with exceptions” 
   d) “myMethod is done”  
   e) Nothing is printed  

## 11.Which of the following are Java keywords?
   a) array  
   b) boolean  
   c) integer  
   d) protect  
   e) super  

## 12.What of the following is the default value of an instance variable? 
   a) null  
   b) 0  
   c) Depends upon the type of variable  


# CHAPTER 11
## Homework Questions given by Professor + discussed questions on class:
### 1.What is Syntactic Unit?(HW)
    sequences of tokens.(tokens can be identifiers, literals )

### 2.Why variable name cannot be started with digits?
    if variable starts with digits , it cannot be an identifier anymore . It becomes a literal.

### 3.When did Java appeared ?
    1995

### 4.What is Abstract Data type?

    An abstract data type is a user-defined data type that satisfies the following two conditions:
    1.the packaging of data with their associated operations
    2.information hiding (encapsulation)

### 5.Explain the three reasons accessors to private types are better than making types public

    1.Reliability--by hiding the data representations, user code cannot directly access objects of the type 
    or depend on the representation, allowing the representation to be changed without affecting user code
    2.Reduces the range of code and variables of which the programmer must be aware
    3.Name conflicts are less likely

### 6.What is the maximum length of Java variable?

    no limit

### 7.What are constructors and destructors?

    Functions to initialize the data members of instances (they do not create the objects)-->constructor
    Functions to cleanup after an instance is destroyed; usually just to reclaim heap storage -->destructor

### 8.Which keyword is responsible for Object creation in Java?
    new

### 9.What is Friend functions or classes?(HW)

    to provide access to private members to some unrelated units or functions
    Necessary in C++
    little bit similar to Java package
    it can access private members too
    its one directional thats why its better than Java Package

### 10.How to call private constructor?(HW)

    using public static method

### 11.What is a java package and what is its purpose?

    Java includes a naming encapsulation construct: the package. Packages can
    contain more than one type definition, and the types in a package are partial
    friends of one another. Partial here means that the entities defined in a type in
    a package that either are public or protected or have no access specifier are
    visible to all other types in the package. (from slide)

    1.reduces naming conflicts
    2.Logically related classes are arranged together
    3.structerally its like folder

### 12.What is the difference between a class and an instance variable?

    Instance variable are accessed through objects but class variable can be accessed through class name
    static variable are class variable and non static variables are instance variable

### 13.What is the difference between a pointer and reference type?

    Both store the memory addresses but we can know the exact address using pointer , with
    reference there is no way to know the exact memory addresses

### 14.From where java objects are allocated?
    In Java, all objects are allocated from the heap and accessed through reference
    variables. Most objects are allocated with the new operator, but there is no 
    explicit deallocation operator. Garbage collection is used for storage 
    reclamation.

### 15.Which version of Java introduced Generics?

    Java 5
### 16. How the Java way of parametrized abstract data types?

    previously parameterized ADT can be achieved through Object class.
    but now they introduced Generic Classes from Java 5
    Generic parameters must be classes
    Most common generic types are the collection types, such as LinkedList and ArrayList
    • Eliminate the need to cast objects that are removed
    • Eliminate the problem of having multiple types in a structure

### 17. Why are properties (getter/setter) better than specifying an instance variable to the public?

    The main difference between making a field public vs. exposing it through getters/setters 
    is holding control over the property. If you make a field public, it means you provide direct 
    access to the caller. Then, the caller can do anything with your field, either knowingly or 
    unknowingly. For example, one can set a field to a null value, and if you use that field in 
    another method, it may blow up that method with a null pointer exception.

### 18.Does java support nested subprogram?
    yes

### 19.Discuss Abstract Data types in Java.
    In Java abstract data type, we can only know what operations are to be performed and not 
    how to perform them i.e. it does not tell how algorithms are to be implemented or how 
    the data will be organized in the memory. This type is thus called abstract as it does not 
    give the view of implementation.

### 20.Implement Stack in Java.(HW)

    import java.util.ArrayList;

public class StackUsingArrayList<T> {
    private ArrayList<T> stack;

    // Constructor
    public StackUsingArrayList() {
        stack = new ArrayList<>();
    }

    // Push an element onto the stack
    public void push(T value) {
        stack.add(value);
    }

    // Pop an element from the stack
    public T pop() {
        if (isEmpty()) {
            System.out.println("Stack is empty.");
            return null;
        }
        return stack.remove(stack.size() - 1);
    }

    // Peek at the top element without removing it
    public T peek() {
        if (isEmpty()) {
            System.out.println("Stack is empty.");
            return null;
        }
        return stack.get(stack.size() - 1);
    }

    // Check if the stack is empty
    public boolean isEmpty() {
        return stack.isEmpty();
    }

    // Get the size of the stack
    public int size() {
        return stack.size();
    }

    // Main method to test the Stack
    public static void main(String[] args) {
        StackUsingArrayList<Integer> stack = new StackUsingArrayList<>();

        stack.push(10);
        stack.push(20);
        stack.push(30);

        System.out.println("Top element: " + stack.peek()); // Output: 30
        System.out.println("Stack size: " + stack.size());  // Output: 3

        System.out.println("Popped element: " + stack.pop()); // Output: 30
        System.out.println("Top element after pop: " + stack.peek()); // Output: 20
        System.out.println("Stack size after pop: " + stack.size());  // Output: 2

        System.out.println("Is stack empty? " + stack.isEmpty()); // Output: false
    }
    }


# CHAPTER 12

### 1.What is returned by toString method of Object class?
    classname + "@" + hashcode of the object

### 2.All methods in Java :
    toString(),equal(),hashCode(),wait(),notify(),notifyAll(),clone(),get(),finalize()

    




