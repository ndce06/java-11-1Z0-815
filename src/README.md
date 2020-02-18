## JAVA 11 - 1Z0-815

Course - https://cognizant.udemy.com/course/oracle-java-11-programmer-exam-1z0815/

1. File name should have zero or one public class
2. public class and file name should be match

## Main Method - Valid

- public and static modifiers are both required.
- return type always void.
- kewords public and staticin any order - public static void main(String[] args) {} - static public void main(String[] args) {}
- Other modifiers are allowed - final, strictfp, synchronized in any order - public final static void main(String[] args) {} - public final strictfp static void main(String[] args) {} - public final strictfp synchronized static void main(String[] args) {} - public final static synchronized strictfp void main(String[] args) {}
- The parameter of main method can be valid array syntax - public static void main(String[] args) {} - public static void main(String args[]) {} - public static void main(String []args) {} - public static void main(String... args) {} - public static void main(String...args) {} // no space
- The parameter of main method can be declared final. - public static void main(final String[] args) {}
- public static void main(String[] args) throws Exception {}

## import Statements

- import garden.vegetable.VineVegetable; (High precedence)
  import garden.vegetable.\*;

- import static java.lang.Math.PI;
  import static java.lang.Math.\*;

- import static a.e.StaticImport.APP_NAME;
  System.out.println("App Name = " + APP_NAME); // complile
  System.out.println("App Name = " + StaticImport.APP_NAME); // complile error

- import static a.e.StaticImport.APP_NAME;
  import a.e.StaticImport.\*;
  System.out.println("App Name = " + APP_NAME); // complile
  System.out.println("App Name = " + StaticImport.APP_NAME); // complile

- Only one package can be defined in a .java source file.
- The package statement must be first line of code.
- No package statement makes the class, or type you define

* What to look for - multiple package statement - package statement not the first line of code - import statement not in correct order

## Primitive Data Types

byte - 8 bits
char - 16 bits
short - 16 bits
int - 32 bits
long - 64 bits
float - 32 bits
double - 64 bits
boolean - 1 bit

- primitive data types cannot be null - int i8 = null;
  expect it's instance or static variable of class.

## Invalid - literals

byte b8 = 0b*00000001; // cannot have underscore directly after 0b
char c8 = 0x_007F; // cannot have underscore directly after 0x
int i8 = 10000*; // underscore cannot be at end of literal
long d8 = 10000_L; // underscore cannot be prior to suffix (L/l, f/F, d/D)
float f8 = \_100.000; // underscore cannot be at start of literal
double l8 = 1.00000_e10; // underscore cannot prefix exponential in literal

## Declare and initialize Variables - Things to Remember

- Literals with decimal default to double, not float.
- Doubles and floats do not overflow, since they are approximated.
- Local variable privmitives are not initilalized.
- Class static and instance members are initialized.
- null is not a valid value for a primitive data type.
