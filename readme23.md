## Java.util.Random 
> Random random = new Random();
>  System.out.println(random.nextInt(10)); //4
System.out.println(random.nextBoolean()); //true
System.out.println(random.nextDouble()); //0.19674934340402916
System.out.println(random.nextFloat()); // 0.7372021
System.out.println(random.nextGaussian()); //1.4877581394085997
>  System.out.println(random.nextLong());  // 158739962004803677
> System.out.println(random.nextInt()); // -1344764816

## Java.lang.Math
>  int Absi = Math.abs(Vali);
>  Math.PI;
> Math.sqrt(y)
> Math.pow(x, y)


## Decision Statements
- if / if else
- switch case
![switch](https://i.ytimg.com/vi/wcwWlasmLWs/maxresdefault.jpg)

## Looping Statements
- for 
- while
- do while
![do while](https://media.geeksforgeeks.org/wp-content/uploads/20191118154342/do-while-Loop-GeeksforGeeks2.jpg)

## Exception Handling
Exceptions can be caught using a combination of the try and catch keywords.
A try/catch block is placed around the code that might generate an exception.
> try {
//some code
>} catch (Exception e) {
//some code to handle errors
}

### throw
The throw keyword allows you to manually generate exceptions from your methods.
Some of the numerous available exception types include the IndexOutOfBoundsException, IllegalArgumentException, ArithmeticException, and so on.
>  static int div(int a, int b) throws ArithmeticException {

>if(b == 0) {

> throw new ArithmeticException("Division by Zero");
} else {
return a / b;
}
}


>try {
//some code
} catch (ExceptionType1 e1) {
//Catch block
} catch (ExceptionType2 e2) {
//Catch block
} catch (ExceptionType3 e3) {
//Catch block
}


## Arrays and ArrayLists 




