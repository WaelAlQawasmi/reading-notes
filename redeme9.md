## Interface 

 An interface in Java is similar to a class and its collection of abstract methods and could have methods  (default/ static and)  and nested types but the body of this method should exist only default or static methods and all of the interface’s methods must be defined in the class.
Interface construction is like a class.  But interface contains class implements behaviors.





### Declarant Interfaces:
 > EX1

public interface interfaceName {


   // method signatures, constant declarations if any
   
   // An enum with values RIGHT, LEFT
   int turn(Direction direction,
            double radius,
            double startSpeed,
            double endSpeed);
   int changeLanes(Direction direction,
                   double startSpeed,
                   double endSpeed);
   int signalTurn(Direction direction,
                  boolean signalOn);
   int getRadarFront(double distanceToCar,
                     double speedOfCar);
   int getRadarRear(double distanceToCar,
                    double speedOfCar);
         ......
   // more method signatures
}

There no braces in method signatures in interface and it end with a semicolon
If you  want to use interface  you must write class implements the interface
 >EX2 

public class OperateBMW760i implements OperateCar {

    // the OperateCar method signatures, with implementation --
    // for example:
    public int signalTurn(Direction direction, boolean signalOn) {
       // code to turn BMW's LEFT turn indicator lights on
       // code to turn BMW's LEFT turn indicator lights off
       // code to turn BMW's RIGHT turn indicator lights on
       // code to turn BMW's RIGHT turn indicator lights off
    }

    // other members, as needed -- for example, helper classes not 
    // visible to clients of the interface
}


## Inheritance


>[A]Definitions: A class that is derived from another class is called a subclass (also a derived class, extended class, or child class). The class from which the subclass is derived is called a superclass (also a base class or a parent class).

>EX3
>public class Bicycle {
        
   > // the Bicycle class has three fields
   > public int cadence;
   > public int gear;
   > public int speed;
        
   > // the Bicycle class has one constructor
   > public Bicycle(int startCadence, int >startSpeed, int startGear) {
  >      gear = startGear;
  >      cadence = startCadence;
  >      speed = startSpeed;
  >  }
        
    // the Bicycle class has four methods
    public void setCadence(int newValue) {
        cadence = newValue;
    }
        
    public void setGear(int newValue) {
        gear = newValue;
    }
        
    public void applyBrake(int decrement) {
        speed -= decrement;
    }
        
    public void speedUp(int increment) {
        speed += increment;
    }
        
}

 >EX4
public class MountainBike extends Bicycle {
        
    // the MountainBike subclass adds one field
    public int seatHeight;

    // the MountainBike subclass has one constructor
    public MountainBike(int startHeight,
                        int startCadence,
                        int startSpeed,
                        int startGear) {
        super(startCadence, startSpeed, startGear);
        seatHeight = startHeight;
    }   
        
    // the MountainBike subclass adds one method
    public void setHeight(int newValue) {
        seatHeight = newValue;
    }   
}





Notes :
EX1&2 quoted FROM [1]
EX3&4 and [A] quoted FROM [2]

: references

1-[1](https://docs.oracle.com/javase/tutorial/java/IandI/createinterface.html)

2-[2](https://docs.oracle.com/javase/tutorial/java/IandI/subclasses.html)

3-[3](https://www.tutorialspoint.com/java/java_interfaces.htm)








