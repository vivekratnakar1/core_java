>> a lambda expression is a short, concise way to represent an anonymous function (a function without a name).
      >> Introduced in Java 8, lambdas allow you to treat functionality as a method argument or pass a block of code around as if it were

 The Syntax
java
// Syntax variations
() -> System.out.println("Hello World")           // No parameters, single statement
(x) -> x * x                                      // One parameter, returns an expression
(a, b) -> a + b                                   // Multiple parameters
(a, b) -> {                                       // Multiple lines of code (requires braces & explicit return)
    int sum = a + b;
    return sum;
}


. The Core Rule: Functional Interfaces :--  A lambda expression cannot exist in isolation.
A lambda expression cannot exist in isolation. It must implement a Functional Interface. 

The Functional Interface:
java
@FunctionalInterface // Optional annotation to safeguard the rule
interface MathOperation {
    int operate(int a, int b);
}

Before Java 8 (Anonymous Inner Class):
java
// Verbose, requires a lot of structural code just to say "add"
MathOperation addition = new MathOperation() {
    @Override
    public int operate(int a, int b) {
        return a + b;
    }
};


With Java 8+ (Lambda Expression):
java
// Highly readable and ultra-compact
MathOperation addition = (a, b) -> a + b; 
