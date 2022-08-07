# Java String
In Java
, string is basically an object that represents sequence of char values. An array
of characters works same as Java string.
-How to create a string object?
There are two ways to create String object:

1.By string literal
> String s="java";

2.By new keyword
> String s2= new String("java");


> char[]arr={'j','a','v','a'};

 > String s3=new String(arr);

__so S1,S2,S3 is same__

## Java String class methods
### ValueOf 
to convert the char array to String
>char[]arr={'j','a','v','a'};

 >String word=String.ValueOf(arr);
###  charAt()
The Java String class charAt() method returns a char value at the given index number.
>String name="javatpoint";
> 
>char ch=name.charAt(4);//returns the char value at the 4th index (t)

### compareTo() 
it compare each character
>if s1 > s2, it returns positive number  
>if s1 < s2, it returns negative number  
>if s1 == s2, it returns 0  

>String s1="hello";  
String s2="hello";  
String s3="meklo";  
String s4="hemlo";  
String s5="flag";  
System.out.println(s1.compareTo(s2));//0 because both are equal  
System.out.println(s1.compareTo(s3));//-5 because "h" is 5 times lower than "m"  

### contains() 
method searches the sequence of characters in this string.
It returns true if the sequence of char values is found in this string otherwise returns false.
> String name="what do you know about me";  
System.out.println(name.contains("do you know"));  // true
  
>System.out.println(name.contains("hello"));  //false

### equalsIgnoreCase()
method compares the two given strings on the basis of the content of the string irrespective of the case (lower and upper) of the string.
>String s2="javatpoint";  
>String s3="JAVATPOINT";  
>String s4="python";  
System.out.println(s3.equalsIgnoreCase(s2));//true because content and case both are same  
System.out.println(s3.equalsIgnoreCase(s4));//false because content is not same  

### [format()](https://www.javatpoint.com/java-string-format) 

In java, String format() method returns a formatted string using the given locale, 
specified format string, and arguments
>
        // Concatenation of two strings
        String s = String.format("My Company name is %s", str);
  
        // Output is given upto 8 decimal places
        String str2 = String.format("My answer is %.8f", 47.65734);
  
        // Here answer is supposed to be %15.8f" and
        // "47.65734000" there are 15 spaces
        String str3 = String.format("My answer is %15.8f",
                                    47.65734);

>%d	 
input-> integer (incl. byte, short, int, long, bigint)
optput-> Decimal Integer

>%n	 
input-> 	none
optput-> Platform-specific line separator.

>%s 
input-> any type
output-> String value 
>%f
> %.5f to make the number take 5 dismal number
input->floating point
output-> decimal number

### prinf() & format()
- print formatted  the java change the %x with value in the formatted you need
- x
  - s -> string 
    - if you want to print with number of spaces before the string %(NumberOfSpaces)S
    - System.out.printf("%3s", "hi");      //  -->  "   hi"
    - if you want to print with number of spaces after the string %(-NumberOfSpaces)S
    - System.out.printf("%-3s koo", "hi");      //  -->  "hi   koo"

  - f -> float
     - if you need three places(خانات)  and  one decimal places(الخانات العشرية) %3.1f
     - System.out.printf("Hello World %03.1f",222.2222);
     - output -> 222.1
     -     long n = 461012;
     -  System.out.format("%d%n", n);      //  -->  "461012"
     -  System.out.format("%08d%n", n);    //  -->  "00461012"
      - System.out.format("%+8d%n", n);    //  -->  " +461012"
     -  System.out.format("%,8d%n", n);    // -->  " 461,012"
     -  System.out.format("%+,8d%n%n", n); //  -->  "+461,012"

  - d -> integer
    - if you need two decimal places(الخانات العشرية) %
  - c ->character
    - System.out.printf("%c+%c",'A','B'); //A+B


### indexOf(int ch)
> int index1=s1.indexOf("is");//returns the index of is substring 

###   substring(x,y)
        String substr2 = s1.substring(5,10); // Starts from 5 and goes to 10
### replace()
> String s1="javatpoint is a very good website"; 
> String replaceString=s1.replace('a','e');//replaces all occurrences of 'a' to 'e'  

>String s1="my name is khan my name is java";  
String replaceString=s1.replace("is","was");//replaces all occurrences of "is" to "was"  

### trim()
method eliminates leading and trailing spaces

### startsWith()
> System.out.println(s1.startsWith("java string"));   // true  

### endsWith()
> System.out.println(s1.endsWith("point"));  // false

## ref
[java-string](https://www.javatpoint.com/java-string-charat)
