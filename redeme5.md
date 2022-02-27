# packages : 
is a set classes grouped together  and the name of  the package is same folder’s name that  contains this classes.java  gropes files 
 you must decelerate the package = in the first of  the source Java file  and by using import statement you can select the classes that you need from other packages alone without their package but the default package don’t need to declaration   we can add static to imort.

The syntax of package declaration:
1.	Imports  &Package statement  is optional
2.	 The definitions  of interface  or Class  are required.

Ex 1:
Package nameOfPackage;

import java.awt.*;

public class className {…
}

We use * to select all class available in package  
import javax.swing.*;  

We can use  fully name of the class that qualified instead of using import.

ex 2

class ImportTest {
    public static void main(String[] args) {
        javax.swing.JOptionPane.showMessageDialog(null, "Hi")
    }
}
"
 > The common packages in GUI [1]
>- import java.awt.*;	Common GUI >elements.
> - import java.awt.event.*;	The most common GUI event listeners.
> - import javax.swing.*;	More common GUI elements. Note "javax".
 
# The loops
Loops in programming languages is continue in execute set of instruction until specific condition become false

There are four type of loops in java:

## For loop
for (initialize variable ; conduction; step incressing) {
statement1
.
.
 }
In the first  install variable then check the conduction if the conduction true the statements of for loop will execute each time until the conduction be  false 
Ex
for (int i = 0; i < 4; i++) {
    System.out.println( i);
}
The output 
0
1
2
3
And we can use for with arrays to deal with all elements of the array
int[] array = { 1,5,10 };
 for (int item : array) { System.out.println(item); }



## while loop
the while loop still execute the  statements until the conduction  became false
in the first, the while checking the condition if true then execute the statements.
while (conduction) 
{statement1;
.
.
.
}
## Do while

do {
 statement1;
.
.
.
 } 
while (condition);
the first thing execute the statements between { }  of do , regardless the condition un while after that if the condition is true the  statements will continue execute intel the condition became false 

---------
## notes :
ex1 , ex2 and [1] quoted  from reference  1

## references
- [1] https://perso.ensta-paris.fr/~diam/java/online/notes-java/language/10basics/import.html
- [2] https://www.baeldung.com/java-loops 
