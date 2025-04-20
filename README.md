Practical No. 1: Write a program to calculate the perimeter and area of a rectangle.
Program:
import java.util.Scanner;
public class Practical1 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 System.out.print("Enter the length of the rectangle: ");
 double l = scanner.nextDouble();
 System.out.print("Enter the breadth of the rectangle: ");
 double b = scanner.nextDouble();
 double area = l * b;
 double perimeter = 2 * (l + b);
 System.out.println("Area of the rectangle: " + area);
 System.out.println("Perimeter of the rectangle: " + perimeter);
 scanner.close();
 }
}





Practical No. 2: Write a menu-driven program to perform the following operations:
i. Calculate the volume of a cylinder.
ii. Find the factorial of the given number.
iii. Check if the number is Armstrong or not.
iv. Exit
Program:
import java.util.Scanner;
public class Practical2 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 int choice;
 do {
 System.out.println("Menu:");
 System.out.println("1. Calculate the volume of a cylinder");
 System.out.println("2. Find the factorial of the given number");
 System.out.println("3. Check if the number is Armstrong or not");
 System.out.println("4. Exit");
 System.out.print("Enter your choice: ");
 choice = scanner.nextInt();
 switch (choice) {
 case 1:
 System.out.print("Enter the radius of the cylinder: ");
 double r = scanner.nextDouble();
 System.out.print("Enter the height of the cylinder: ");
 double h = scanner.nextDouble();
 double volume = Math.PI * r * r * h;
 System.out.println("Volume of the cylinder: " + volume);
 break;
 case 2:
 System.out.print("Enter a number to find its factorial: ");
 int n = scanner.nextInt();
 long factorial = 1;
 for (int i = 1; i <= n; i++) {
 factorial *= i;
 }
 System.out.println("Factorial: " + factorial);
 break;
 case 3:
 System.out.print("Enter a number to check if it's Armstrong: ");
 int num = scanner.nextInt();
 int temp = num, sum = 0;
 int digits = String.valueOf(num).length();
 while (temp > 0) {
 int digit = temp % 10;
 sum += Math.pow(digit, digits);
 temp /= 10;
 }
 if (sum == num) {
 System.out.println(num + " is an Armstrong number");
 } else {
 System.out.println(num + " is not an Armstrong number");
 }
 break;
 case 4:
 System.out.println("Exiting...");
 break;
 default:
 System.out.println("Invalid choice");
 }
 } while (choice != 4);
 scanner.close();
 }
}






Practical No. 3: Write a program to accept the array element and display it in reverse
order.
Program:
import java.util.Scanner;
public class Practical3 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 System.out.print("Enter the number of elements in the array: ");
 int n = scanner.nextInt();
 int[] a = new int[n];
 System.out.println("Enter the elements of the array:");
 for (int i = 0; i < n; i++) {
 a[i] = scanner.nextInt();
 }
 System.out.println("Original array:");
 for (int i = 0; i < n; i++) {
 System.out.print(a[i] + " ");
 }
 System.out.println();
 System.out.println("Reversed array:");
 for (int i = n - 1; i >= 0; i--) {
 System.out.print(a[i] + " ");
 }
 System.out.println();
 scanner.close();
 }
}





Practical No. 4: Write a menu-driven program to perform the following operations on a
multidimensional array:
i. Addition.
ii. Multiplication.
iii. Transpose of any matrix.
iv. Exit.
Program:
import java.util.Scanner;
public class Practical4 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 int[][] a = new int[3][3];
 int[][] b = new int[3][3];
 int choice;
 System.out.println("Enter the elements of the first matrix (3x3):");
 for (int i = 0; i < 3; i++) {
 for (int j = 0; j < 3; j++) {
 a[i][j] = scanner.nextInt();
 }
 }
 System.out.println("Enter the elements of the second matrix (3x3):");
 for (int i = 0; i < 3; i++) {
 for (int j = 0; j < 3; j++) {
 b[i][j] = scanner.nextInt();
 }
 }
 do {
 System.out.println("Menu:");
 System.out.println("1. Addition");
 System.out.println("2. Multiplication");
 System.out.println("3. Transpose of the first matrix");
 System.out.println("4. Exit");
 System.out.print("Enter your choice: ");
 choice = scanner.nextInt();
 switch (choice) {
 case 1:
 System.out.println("Sum of the matrices:");
 for (int i = 0; i < 3; i++) {
 for (int j = 0; j < 3; j++) {
 System.out.print((a[i][j] + b[i][j]) + " ");
 }
 System.out.println();
 }
 break;
 case 2:
 System.out.println("Product of the matrices:");
 for (int i = 0; i < 3; i++) {
 for (int j = 0; j < 3; j++) {
 int sum = 0;
 for (int k = 0; k < 3; k++) {
 sum += a[i][k] * b[k][j];
 }
 System.out.print(sum + " ");
 }
 System.out.println();
 }
 break;
 case 3:
 System.out.println("Transpose of the first matrix:");
 for (int i = 0; i < 3; i++) {
 for (int j = 0; j < 3; j++) {
 System.out.print(a[j][i] + " ");
 }
 System.out.println();
 }
 break;
 case 4:
 System.out.println("Exiting...");
 break;
 default:
 System.out.println("Invalid choice");
 }
 } while (choice != 4);
 scanner.close();
 }
}






Practical No. 5: Write a program to accept N names of countries and display them in
descending order.
Program:
import java.util.Scanner;
import java.util.Arrays;
public class Practical5 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 System.out.print("Enter the number of countries: ");
 int n = scanner.nextInt();
 scanner.nextLine(); // Consume the newline character
 String[] countries = new String[n];
 System.out.println("Enter the names of the countries:");
 for (int i = 0; i < n; i++) {
 countries[i] = scanner.nextLine();
 }
 Arrays.sort(countries);
 System.out.println("Countries in descending order:");
 for (int i = n - 1; i >= 0; i--) {
 System.out.println(countries[i]);
 }
 scanner.close();
 }
}






Practical No. 6: Write a menu-driven program to perform the following operations on a 2D
array:
i. Sum of diagonal elements.
ii. Sum of upper diagonal elements.
iii. Sum of lower diagonal elements.
iv. Exit.
Program:
import java.util.Scanner;
public class Practical6 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 int[][] a = new int[3][3];
 int choice;
 System.out.println("Enter the elements of the 2D array (3x3):");
 for (int i = 0; i < 3; i++) {
 for (int j = 0; j < 3; j++) {
 a[i][j] = scanner.nextInt();
 }
 }
 do {
 System.out.println("Menu:");
 System.out.println("1. Sum of diagonal elements");
 System.out.println("2. Sum of upper diagonal elements");
 System.out.println("3. Sum of lower diagonal elements");
 System.out.println("4. Exit");
 System.out.print("Enter your choice: ");
 choice = scanner.nextInt();
 switch (choice) {
 case 1:
 int sum = 0;
 for (int i = 0; i < 3; i++) {
 sum += a[i][i];
 }
 System.out.println("Sum of diagonal elements: " + sum);
 break;
 case 2:
 sum = 0;
 for (int i = 0; i < 3; i++) {
 for (int j = i + 1; j < 3; j++) {
 sum += a[i][j];
 }
 }
 System.out.println("Sum of upper diagonal elements: " + sum);
 break;
 case 3:
 sum = 0;
 for (int i = 0; i < 3; i++) {
 for (int j = 0; j < i; j++) {
 sum += a[i][j];
 }
 }
 System.out.println("Sum of lower diagonal elements: " + sum);
 break;
 case 4:
 System.out.println("Exiting...");
 break;
 default:
 System.out.println("Invalid choice");
 }
 } while (choice != 4);
 scanner.close();
 }
}







Practical No. 7: Write a program to display the 1 to 15 tables.
Program:
public class Practical7 {
 public static void main(String[] args) {
 for (int i = 1; i <= 15; i++) {
 System.out.println("Multiplication table for " + i + ":");
 for (int j = 1; j <= 10; j++) {
 System.out.println(i + " * " + j + " = " + (i * j));
 }
 System.out.println();
 }
 }
}
Output:
Multiplication table for 1:
1 * 1 = 1
1 * 2 = 2
1 * 3 = 3
1 * 4 = 4
1 * 5 = 5
1 * 6 = 6
1 * 7 = 7
1 * 8 = 8
1 * 9 = 9
1 * 10 = 10
Multiplication table for 2:
2 * 1 = 2
2 * 2 = 4
2 * 3 = 6
2 * 4 = 8
2 * 5 = 10
2 * 6 = 12
2 * 7 = 14
2 * 8 = 16
2 * 9 = 18
2 * 10 = 20
... (Output continues for tables 3 to 15)







Practical No. 8: Define an abstract class shape with abstract methods area() and volume().
Write a Java program to calculate the area and volume of Cone and Cylinder.
Program:
import java.util.Scanner;
abstract class Shape {
 abstract double area();
 abstract double volume();
}
class Cone extends Shape {
 double r, h, s; // s is the slant height
 Cone(double r, double h, double s) {
 this.r = r;
 this.h = h;
 this.s = s;
 }
 @Override
 double area() {
 return Math.PI * r * (r + s);
 }
 @Override
 double volume() {
 return (1.0 / 3.0) * Math.PI * r * r * h;
 }
}
class Cylinder extends Shape {
 double r, h;
 Cylinder(double r, double h) {
 this.r = r;
 this.h = h;
 }
 @Override
 double area() {
 return 2 * Math.PI * r * (r + h);
 }
 @Override
 double volume() {
 return Math.PI * r * r * h;
 }
}
public class Practical8 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 System.out.print("Enter the radius of the cone: ");
 double coneRadius = scanner.nextDouble();
 System.out.print("Enter the height of the cone: ");
 double coneHeight = scanner.nextDouble();
 System.out.print("Enter the slant height of the cone: ");
 double coneSlantHeight = scanner.nextDouble();
 Cone cone = new Cone(coneRadius, coneHeight, coneSlantHeight);
 System.out.println("Area of the cone: " + cone.area());
 System.out.println("Volume of the cone: " + cone.volume());
 System.out.print("Enter the radius of the cylinder: ");
 double cylinderRadius = scanner.nextDouble();
 System.out.print("Enter the height of the cylinder: ");
 double cylinderHeight = scanner.nextDouble();
 Cylinder cylinder = new Cylinder(cylinderRadius, cylinderHeight);
 System.out.println("Area of the cylinder: " + cylinder.area());
 System.out.println("Volume of the cylinder: " + cylinder.volume());
 scanner.close();
 }
}
Output:
Enter the radius of the cone: 5
Enter the height of the cone: 12
Enter the slant height of the cone: 13
Area of the cone: 282.7433388230814
Volume of the cone: 314.1592653589793
Enter the radius of the cylinder: 4
Enter the height of the cylinder: 10
Area of the cylinder: 351.8583772020571
Volume of the cylinder: 502.6548245743669









Practical No. 9: Define an Interface shape with an abstract method area(). Write a Java
program to calculate the area of Circle and Sphere (use the final keyword).
Program:
import java.util.Scanner;
interface Shape {
 double area();
}
class Circle implements Shape {
 final double PI = Math.PI;
 double r;
 Circle(double r) {
 this.r = r;
 }
 @Override
 public double area() {
 return PI * r * r;
 }
}
class Sphere implements Shape {
 final double PI = Math.PI;
 double r;
 Sphere(double r) {
 this.r = r;
 }
 @Override
 public double area() {
 return 4 * PI * r * r;
 }
}
public class Practical9 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 System.out.print("Enter the radius of the circle: ");
 double circleRadius = scanner.nextDouble();
 Circle circle = new Circle(circleRadius);
 System.out.println("Area of the circle: " + circle.area());
 System.out.print("Enter the radius of the sphere: ");
 double sphereRadius = scanner.nextDouble();
 Sphere sphere = new Sphere(sphereRadius);
 System.out.println("Area of the sphere: " + sphere.area());
 scanner.close();
 }
}
Output:
Enter the radius of the circle: 7
Area of the circle: 153.93804002589985
Enter the radius of the sphere: 6
Area of the sphere: 452.38934211693025








Practical No. 10: Write a program for multilevel inheritance such that the country is
inherited from the continent. The state is inherited from the country. Display the place,
state, country, and continent.
Program:
import java.util.Scanner;
class Continent {
 String continentName;
 Continent(String continentName) {
 this.continentName = continentName;
 }
 void displayContinent() {
 System.out.println("Continent: " + continentName);
 }
}
class Country extends Continent {
 String countryName;
 Country(String continentName, String countryName) {
 super(continentName);
 this.countryName = countryName;
 }
 void displayCountry() {
 super.displayContinent();
 System.out.println("Country: " + countryName);
 }
}
class State extends Country {
 String stateName;
 State(String continentName, String countryName, String stateName) {
 super(continentName, countryName);
 this.stateName = stateName;
 }
 void displayState() {
 super.displayCountry();
 System.out.println("State: " + stateName);
 }
}
class Place extends State {
 String placeName;
 Place(String continentName, String countryName, String stateName, String placeName) {
 super(continentName, countryName, stateName);
 this.placeName = placeName;
 }
 void displayPlaceDetails() {
 super.displayState();
 System.out.println("Place: " + placeName);
 }
}
public class Practical10 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 System.out.print("Enter the continent: ");
 String continent = scanner.nextLine();
 System.out.print("Enter the country: ");
 String country = scanner.nextLine();
 System.out.print("Enter the state: ");
 String state = scanner.nextLine();
 System.out.print("Enter the place: ");
 String place = scanner.nextLine();
 Place myPlace = new Place(continent, country, state, place);
 myPlace.displayPlaceDetails();
 scanner.close();
 }
}
Output:
Enter the continent: Asia
Enter the country: India
Enter the state: Maharashtra
Enter the place: Mumbai
Continent: Asia
Country: India
State: Maharashtra
Place: Mumbai











Practical No. 11: Write a program that implements a multi-thread application that has
three threads. First thread generate random number every 1 second and if the value is
even, second thread computes the square of number and prints. If the value is odd, then
third thread will print the value of cube of the number.
Program:
import java.util.Random;
class NumberGenerator extends Thread {
 @Override
 public void run() {
 Random random = new Random();
 for (int i = 0; i < 10; i++) {
 int n = random.nextInt(100);
 System.out.println("Generated Number: " + n);
 if (n % 2 == 0) {
 new SquareCalculator(n).start();
 } else {
 new CubeCalculator(n).start();
 }
 try {
 Thread.sleep(1000); // Sleep for 1 second
 } catch (InterruptedException e) {
 System.out.println("Generator thread interrupted.");
 }
 }
 }
}
class SquareCalculator extends Thread {
 int n;
 SquareCalculator(int n) {
 this.n = n;
 }
 @Override
 public void run() {
 System.out.println("Square of " + n + " is: " + (n * n));
 }
}
class CubeCalculator extends Thread {
 int n;
 CubeCalculator(int n) {
 this.n = n;
 }
 @Override
 public void run() {
 System.out.println("Cube of " + n + " is: " + (n * n * n));
 }
}
public class Practical11 {
 public static void main(String[] args) {
 NumberGenerator generator = new NumberGenerator();
 generator.start();
 }
}
Output:
Generated Number: 45
Cube of 45 is: 91125
Generated Number: 22
Square of 22 is: 484
Generated Number: 81
Cube of 81 is: 531441
Generated Number: 16
Square of 16 is: 256
Generated Number: 7
Cube of 7 is: 343
Generated Number: 92
Square of 92 is: 8464
Generated Number: 63
Cube of 63 is: 250047
Generated Number: 30
Square of 30 is: 900
Generated Number: 59
Cube of 59 is: 205379
Generated Number: 4
Square of 4 is: 16











Practical No. 12: Write a Java program to read in students' names from the user, store
them into the ArrayList collection. The program should not allow duplicate names. Display
the names in ascending order.1
Program:
import java.util.ArrayList;
import java.util.Collections;
import java.util.HashSet;
import java.util.Scanner;
import java.util.Set;
public class Practical12 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 Set<String> nameSet = new HashSet<>();
 ArrayList<String> nameList = new ArrayList<>();
 System.out.print("Enter the number of students: ");
 int n = scanner.nextInt();
 scanner.nextLine(); // Consume newline
 System.out.println("Enter the names of the students:");
 for (int i = 0; i < n; i++) {
 String name = scanner.nextLine();
 if (nameSet.add(name)) {
 nameList.add(name);
 } else {
 System.out.println("Duplicate name: " + name + " - Not added.");
 }
 }
 Collections.sort(nameList);
 System.out.println("Students' names in ascending order:");
 for (String studentName : nameList) {
 System.out.println(studentName);
 }
 scanner.close();
 }
}
Output:
Enter the number of students: 5
Enter the names of the students:
Alice
Bob
Charlie
Bob
David
Duplicate name: Bob - Not added.
Students' names in ascending order:
Alice
Bob
Charlie
David










Practical No. 13: Write a Java program to accept n employee names from the user, store
them into the LinkedList class, and display them by using a. Iterator Interface. b.
ListIterator Interface.
Program:
import java.util.LinkedList;
import java.util.Iterator;
import java.util.ListIterator;
import java.util.Scanner;
public class Practical13 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 LinkedList<String> employeeNames = new LinkedList<>();
 System.out.print("Enter the number of employees: ");
 int n = scanner.nextInt();
 scanner.nextLine(); // Consume newline
 System.out.println("Enter the names of the employees:");
 for (int i = 0; i < n; i++) {
 employeeNames.add(scanner.nextLine());
 }
 System.out.println("\nDisplaying names using Iterator:");
 Iterator<String> iterator = employeeNames.iterator();
 while (iterator.hasNext()) {
 System.out.println(iterator.next());
 }
 System.out.println("\nDisplaying names using ListIterator (forward):");
 ListIterator<String> listIteratorForward = employeeNames.listIterator();
 while (listIteratorForward.hasNext()) {
 System.out.println(listIteratorForward.next());
 }
 System.out.println("\nDisplaying names using ListIterator (backward):");
 ListIterator<String> listIteratorBackward =
employeeNames.listIterator(employeeNames.size());
 while (listIteratorBackward.hasPrevious()) {
 System.out.println(listIteratorBackward.previous());
 }
 scanner.close();
 }
}
Output:
Enter the number of employees: 3
Enter the names of the employees:
John Doe
Jane Smith
Peter Jones
Displaying names using Iterator:
John Doe
Jane Smith
Peter Jones
Displaying names using ListIterator (forward):
John Doe
Jane Smith
Peter Jones
Displaying names using ListIterator (backward):
Peter Jones
Jane Smith
John Doe











Practical No. 14: Write a Java program to accept the details of 'n' employees (Ename,
salary) from the user, store them into the Hash table, and display the Employee names2
having the maximum salary.
Program:
import java.util.Hashtable;
import java.util.Scanner;
import java.util.Map.Entry;
public class Practical14 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 Hashtable<String, Double> employeeDetails = new Hashtable<>();
 System.out.print("Enter the number of employees: ");
 int n = scanner.nextInt();
 scanner.nextLine(); // Consume newline
 System.out.println("Enter the employee details (name and salary):");
 for (int i = 0; i < n; i++) {
 System.out.print("Enter employee name: ");
 String name = scanner.nextLine();
 System.out.print("Enter employee salary: ");
 double salary = scanner.nextDouble();
 scanner.nextLine(); // Consume newline
 employeeDetails.put(name, salary);
 }
 double maxSalary = 0;
 for (double salary : employeeDetails.values()) {
 if (salary > maxSalary) {
 maxSalary = salary;
 }
 }
 System.out.println("\nEmployees with the maximum salary:");
 for (Entry<String, Double> entry : employeeDetails.entrySet()) {
 if (entry.getValue() == maxSalary) {
 System.out.println(entry.getKey());
 }
 }
 scanner.close();
 }
}
Output:
Enter the number of employees: 3
Enter the employee details (name and salary):
Enter employee name: John Doe
Enter employee salary: 50000
Enter employee name: Jane Smith
Enter employee salary: 60000
Enter employee name: Peter Jones
Enter employee salary: 60000
Employees with the maximum salary:
Jane Smith
Peter Jones













Practical No. 15: Write a Java program to accept the employee name from the user and
check whether it is valid or not. If it is not valid, then throw the user-defined exception
"Name is invalid" otherwise display it.
Program:
import java.util.Scanner;
class NameInvalidException extends Exception {
 NameInvalidException(String message) {
 super(message);
 }
}
public class Practical15 {
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
 System.out.print("Enter employee name: ");
 String name = scanner.nextLine();
 try {
 if (!name.matches("^[a-zA-Z\\s]+$")) { // Simple validation: only letters and spaces
allowed
 throw new NameInvalidException("Name is invalid");
 }
 System.out.println("Employee name: " + name);
 } catch (NameInvalidException e) {
 System.out.println("Exception: " + e.getMessage());
 }
 scanner.close();
 }
}
Output:
Enter employee name: John123
Exception: Name is invalid
Enter employee name: John Doe
Employee name: John Doe
Practical No. 16: Write a multithreading program in Java to display all vowels from a
given string.(use thread class)
Program:
public class Practical16 {
 public static void main(String[] args) {
 String inputString = "Hello Everyone, How are you?";
 VowelThread vowelThread = new VowelThread(inputString);
 vowelThread.start();
 }
}
class VowelThread extends Thread {
 String text;
 VowelThread(String text) {
 this.text = text;
 }
 @Override
 public void run() {
 System.out.print("Vowels in the string: ");
 for (int i = 0; i < text.length(); i++) {
 char ch = text.charAt(i);
 if (isVowel(ch)) {
 System.out.print(ch + " ");
 }
 }
 }
 boolean isVowel(char ch) {
 ch = Character.toLowerCase(ch);
 return ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u';
 }
}
Output:
Vowels in the string: e E e o e o a e ou



















Practical No. 17: Write a program in Java that will show the life cycle (creation, sleep, and
dead) of a thread. Program should print randomly the name of thread and value of sleep
time. The name of the thread should be hard coded through constructor. The sleep time of
a thread will be a random integer in the range of 0 to 4999.
Program:
import java.util.Random;
public class Practical17 {
 public static void main(String[] args) {
 MyThread thread1 = new MyThread("Thread-1");
 MyThread thread2 = new MyThread("Thread-2");
 MyThread thread3 = new MyThread("Thread-3");
 thread1.start();
 thread2.start();
 thread3.start();
 }
}
class MyThread extends Thread {
 MyThread(String name) {
 super(name);
 }
 @Override
 public void run() {
 Random random = new Random();
 int sleepTime = random.nextInt(5000); // 0 to 4999 milliseconds
 System.out.println(getName() + " - Created");
 try {
 Thread.sleep(sleepTime);
 System.out.println(getName() + " - Slept for " + sleepTime + " ms");
 } catch (InterruptedException e) {
 System.out.println(getName() + " - Interrupted");
 }
 System.out.println(getName() + " - Dead");
 }
}
Output:
Thread-2 - Created
Thread-3 - Created
Thread-1 - Created
Thread-3 - Slept for 1914 ms
Thread-3 - Dead
Thread-2 - Slept for 3267 ms
Thread-2 - Dead
Thread-1 - Slept for 4125 ms
Thread-1 - Dead













Practical No. 18: Write a Java program that will display the name and priority of the
current thread. Change the name of thread to MyThread and priority to 2. Display the
details of thread.
Program:
public class Practical18 {
 public static void main(String[] args) {
 Thread currentThread = Thread.currentThread();
 System.out.println("Original Thread Details:");
 System.out.println("Name: " + currentThread.getName());
 System.out.println("Priority: " + currentThread.getPriority());
 currentThread.setName("MyThread");
 currentThread.setPriority(2);
 System.out.println("\nModified Thread Details:");
 System.out.println("Name: " + currentThread.getName());
 System.out.println("Priority: " + currentThread.getPriority());
 }
}
Output:
Original Thread Details:
Name: main
Priority: 5
Modified Thread Details:
Name: MyThread
Priority: 2










Practical No. 19: Write a Java program using multithreading to execute the threads
sequentially (use synchronized method)
Program:
public class Practical19 {
 public static void main(String[] args) {
 SharedResource resource = new SharedResource();
 MyThread1 thread1 = new MyThread1(resource, "Thread-1");
 MyThread1 thread2 = new MyThread1(resource, "Thread-2");
 MyThread1 thread3 = new MyThread1(resource, "Thread-3");
 thread1.start();
 thread2.start();
 thread3.start();
 }
}
class SharedResource {
 // Synchronized method to ensure sequential access
 public synchronized void display(String threadName) {
 for (int i = 1; i <= 5; i++) {
 System.out.println("Thread: " + threadName + " - Count: " + i);
 try {
 Thread.sleep(500);
 } catch (InterruptedException e) {
 System.out.println("Thread interrupted");
 }
 }
 }
}
class MyThread1 extends Thread {
 SharedResource resource;
 MyThread1(SharedResource resource, String name) {
 super(name);
 this.resource = resource;
 }
 @Override
 public void run() {
 resource.display(getName());
 }
}
Output:
Thread: Thread-1 - Count: 1
Thread: Thread-1 - Count: 2
Thread: Thread-1 - Count: 3
Thread: Thread-1 - Count: 4
Thread: Thread-1 - Count: 5
Thread: Thread-2 - Count: 1
Thread: Thread-2 - Count: 2
Thread: Thread-2 - Count: 3
Thread: Thread-2 - Count: 4
Thread: Thread-2 - Count: 5
Thread: Thread-3 - Count: 1
Thread: Thread-3 - Count: 2
Thread: Thread-3 - Count: 3
Thread: Thread-3 - Count: 4
Thread: Thread-3 - Count: 5












Practical No. 20: Write a Multithreading program in Java to display all the alphabets from
A to Z after 3 seconds.
Program:
public class Practical20 {
 public static void main(String[] args) {
 AlphabetThread alphabetThread = new AlphabetThread();
 alphabetThread.start();
 }
}
class AlphabetThread extends Thread {
 @Override
 public void run() {
 try {
 Thread.sleep(3000); // Sleep for 3 seconds
 } catch (InterruptedException e) {
 System.out.println("Thread interrupted");
 }
 for (char c = 'A'; c <= 'Z'; c++) {
 System.out.print(c + " ");
 }
 }
}
Output:
(After a 3-second delay)
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z










Practical No. 21: Write a servlet program which counts how many times a user has visited
a web page. If user is visiting the page for the first time, display a welcome message. If the
user is revisiting the page, display the number of times visited. (Use Cookie)
Program:
sevlet.java file :-
import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;
public class HitCountServlet extends HttpServlet {
 public void doGet(HttpServletRequest req, HttpServletResponse res)
 throws ServletException, IOException {
 res.setContentType("text/html");
 PrintWriter out = res.getWriter();
 int count = 1;
 Cookie c[] = req.getCookies();
 if (c == null) {
 Cookie newCookie = new Cookie("count", "1");
 res.addCookie(newCookie);
 out.print("<h1>Welcome Servlet</h1>");
 } else {
 count = Integer.parseInt(c[0].getValue()) + 1;
 c[0].setValue(Integer.toString(count));
 res.addCookie(c[0]);
 }
 out.print("Hit Count:" + count);
 }
}
web.xml file :-
<servlet>
 <servlet-name>HitCount</servlet-name>
 <servlet-class>HitCountServlet</servlet-class>
</servlet>
<servlet-mapping>
 <servlet-name>HitCount</servlet-name>
 <url-pattern>/hit</url-pattern>
</servlet-mapping>
Output:








Practical No. 22: Write a JSP script to accept username, store it into the session, compare it
with password in another jsp file, if username matches with password then display
appropriate message in html file.
Program:
user.html file :-
<form method='post' action='user.jsp'>
 User Name:<input type='text' name='un'><br>
 <input type='submit'><input type='reset'>
</form>
user.jsp file :-
<%
 String un = request.getParameter("un");
 session.setAttribute("user",un);
 response.sendRedirect("pass.html");
%>
pass.html file :-
<form method='post' action='pass.jsp'>
Password:<input type='password' name='pass'><br>
<input type='submit'><input type='reset'>
</form>
pass.jsp file :-
<%
 String pass = request.getParameter("pass");
 String un = session.getAttribute("user").toString();
 if(un.equals(pass))
 response.sendRedirect("success.html");
 else
 response.sendRedirect("fail.html");
%>
success.html file:-
<body bgcolor='green'>
<h1>Login Successful.</h1>
</body>
fail.html file:-
<body bgcolor='red'>
<h1>Login Failed.</h1>
</body>
Output:
If user name password are not same:-






  
Practical No. 23: Write a JSP program to accept user name in a TextBox and greet the user
according to the time on server machine.
Program:
greet.html file:-
<form method='post' action='greet.jsp'>
User Name:<input type='text' name='uname'>
<input type='submit'>
</form>
greet.jsp file:-
<%@page import="java.util.*"%>
<%
 String uname = request.getParameter("uname");
 Date d = new Date();
 if(d.getHours()<11){
%>
Good morning
<%
 }
 else if(d.getHours()<17){
%>
Good afternoon
<%
 }
 else{
%>
Good evening
<%
 }
%>
<%=" "+uname%>
Output:








  
Practical No. 24: Create a JSP page to accept a number from an user and display it in
words: Example: 123 – One Two Three. The output should be in red color.
Program:
number.html file:-
<form method='post' action='number.jsp'>
Number:<input type='text' name='no'><br>
<input type='submit'><input type='reset'>
</form>
number.jsp file:-
<font color='blue'>
<%
 String words[]={"Zero","One","Two","Three","Four","Five",
 "Six","Seven","Eight","Nine"};
 String s = request.getParameter("no");
 for(int i=0;i<s.length();i++){
 out.print(words[s.charAt(i)-'0']+" ");
 }
%>
</font>
Output:





   
Practical No. 25: Write a JSP program to check whether given number is Armstrong or
not. (Use Include directive).
Program:
armstrong.html file:-
<form method='post' action='check.jsp'>
Enter Number:<input type='text' name='no'><br><br>
<input type='submit'><input type='reset'>
</form>
check.jsp file:-
<%!
 public boolean isArmstrong(int n){
 int s=0,n1=n;
 while(n!=0){
 int r = n%10;
 s+=r*r*r;
 n/=10;
 }
 return s==n1;
 }
%>
armstrong.jsp.file:-
<%!
 public boolean isArmstrong(int n){
 int s=0,n1=n;
 while(n!=0){
 int r = n%10;
 s+=r*r*r;
 n/=10;
 }
 return s==n1;
 }
%>
Output:








  
Practical No. 26: Write a JSP script to accept username, store it into the session, compare it
with password in another jsp file, if username matches with password then display
appropriate message in html file.
Program:
age.html file:-
<form method='post' action='age_check.jsp'>
Enter Vote Name:<input type='text' name='name'><br>
Enter Voter Age:<input type='text' name='age'><br><br>
<input type='submit'><input type='reset'>
</form>
age_check.jsp file:-
<%
 String name = request.getParameter("name");
 int age = Integer.parseInt(request.getParameter("age"));
 if(age>=18)
 out.print(name+" you are eligible for voting");
 else
 out.print(name+" you are not eligible for voting");
%>
Output:
