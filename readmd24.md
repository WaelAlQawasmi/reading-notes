# Arrays and ArrayLists 
Arrays and ArrayLists
# Arrays
- you can't chang the nuber of valur of array after insall it after buils it
## building
- int[]array=new int[7];
- char[]array={'j','a','v','a'};
## Multi-dimensional array creation
- int[][]array=new int[2][2];
- int[][]array={{1,2},{2,3}};

## Traverse the elements of an Array
-  to acces to spesific index in array -> arr[index]
- to traverse the elements of an array use 
>for( dataType elemant __:__ arr){  }
 ## Arrays methods
 > Arrays.__function name__;
 ### function name
 - asList();
 - binarySearch(array, item);
 -compare(array 1, array 2)
 - toString(array)

 #  ArrayList
The ArrayList class is a resizable array, which can be found in the __java.util package.__

The difference between a built-in array and an ArrayList in Java, is that the size of an array cannot be modified (if you want to add or remove elements to/from an array, you have to create a new one). While elements can be added and removed from an ArrayList whenever you want. The syntax is also slightly different:

## building
- ArrayList<String> cars = new ArrayList<String>();
- ArrayList<Integer> cars = new ArrayList<Integer>();

## methodes
 > arrayListName.__methode name__;
 - add(item); // cars.add("item");
  - get(index); // cars.get(0);
  - set(index, value); //cars.set(0, "Opel");
  - remove(index); // cars.remove(0);
  - clear(); // cars.clear();
  - size(); // cars.size();
  - indexOf(index); // cars.indexOf(2);
  > Collections.sort(myNumbers);  // Sort myNumbers

  > arrayListName.stream().mapToInt(x->x).max()
  - arrayListName.stream().mapToInt(x->x).average()

  ## Traverse the elements of an ArrayList
-  to acces to spesific index in ArrayList -> ArrayList.get(index);
- to traverse the elements of an array use 
>for( dataType elemant __:__ arr){  }
> Iterator iterator= arrayListName.iterator();
- iterator.hasNext()
- iterator.next()






 
