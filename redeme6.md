# Type System in java
There is two types  system in java primitives like int and reference like interger
If  the primitive tupe to be ref one is called , and the other called unboxing
Integer wael = 7; //  called autoboxing 
int wael = new Integer(wael); // called unboxing
 to determine what the object will be used besed on the performance of application that we need to achive , and available memory and the what values we handle.

> 	boolean – 1 bit
> 	byte – 8 bits
> 	short, char – 16 bits
> 	int, float – 32 bits
> 	long, double – 64 bits

> 	Boolean – 128 bits
> 	Byte – 128 bits
> 	Short, Character – 128 bits
> 	Integer, Float – 128 bits
> 	Long, Double – 192 bits
[2]

the performance of  the code in Java is so important issue
it depends on the device on which the code execute on it,
on the perform  that the compiler could perform certain optimizations, the stste of VM  and the process of other operations in OS.
We use JMH to measure the performance.

Default Values
0 in the primitive types is the Default values and null in wrapper classes is the default

Usage 
We prefer to use primitive types due to is faster and use less memory than wrapper classes but java specification does not allow you to use of primitive type in generics parameterized types, in the collections of java or the Reflection API.
# Exception
>  What Is an Exception?
>  Definition: An exception is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions.[1]

If an error happens within a method, an object is created by the method and sent to the runtime system. This object is called an exception object, it has info about this error, like the error type and the state of the app when the error happens, throwing an exception is an exception object Created handing it to the runtime system.

The Catch or Specify Requirement
we can enclose exceptions  If  the code throws on it  by:
•	catches the exception by a try statement. The try provides an exception handler .
•	by specifies method.
Type of exceptions:
-	checked exception we can hendel it by conditions and we can use try and catch.
-	exception is the error : this external the application but we cant handle it by try and catch
-	runtime exception. that is  internal to the app.


How to Throw Exceptions
-throw Statement
 Ex:  throw new EmptyStackException();

Throwable Class and Its Subclasses

 Throwable  with   Error and Exception.
Error Class
When Java virtual machine   have  hard .

# Scanning
the scanner selects and separates tokens and we must  use the USA Setting 
example at scanning[3]
> import java.io.FileReader; 
>import java.io.BufferedReader;
>import java.io.IOException;
>import java.util.Scanner;
>import java.util.Locale;

>public class ScanSum {
    >public static void main(String[] args) throws IOException {

> Scanner s = null;
    >    double sum = 0;

>    try {
     >      s = new Scanner(new > ufferedReader(new FileReader("usnumbers.txt")));
          >   s.useLocale(Locale.US);

>    while (s.hasNext()) {
 >                if (s.hasNextDouble()) {
                    sum += s.nextDouble();
 >                } else {
  >                   s.next();
  >               }   
            }
   >      } finally {
     >        s.close();
      >   }

 >    System.out.println(sum);
   >  }
> }

## Notes
[1] quoted  from reference [A]
[2]quoted  from reference [B]
[3] Example quoted  from reference [C]

## refranses:
- [A] https://perso.ensta-paris.fr/~diam/java/online/notes-java/language/10basics/import.html
- [B]https://www.baeldung.com/java-primitives-vs-objects
- [C] https://docs.oracle.com/javase/tutorial/essential/io/scanning.html
- [D] https://docs.oracle.com/javase/tutorial/essential/exceptions/throwing.html





