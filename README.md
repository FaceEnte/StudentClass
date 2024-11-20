# Student Class

This exercise involves writing a Java program to create a `Student` class that encapsulates the properties and behaviors of a student. The class will include constructors for initializing student objects, methods for printing student information, and a static counter to track the number of student instances created.

## Objective

Create a Java program that:

- Defines a `Student` class with instance variables for the student's name, last name, and age.
- Implements constructors to initialize the student objects.
- Provides methods to print student information and set the student's age.
- Extends the class to include a static counter that tracks the number of `Student` instances created.

## Steps to Complete

1. **Create a New Java Project**

    - Open your Java IDE (e.g., IntelliJ IDEA, Eclipse).
    - Create a new Java project named `StudentClass`.

2. **Create the Student Class**

    - Inside the project, create a new class named `Student`.
    - Declare the following instance variables:
        - `String name`
        - `String lastName`
        - `int age`

3. **Implement Constructors**

    - Implement two constructors:
        - A constructor with three parameters (name, last name, age) that initializes all instance variables.
        - A constructor with two parameters (name, last name) that initializes the name and last name and sets age to a default value (e.g., 18).

4. **Add Methods**

    - Implement the following methods in the `Student` class:
        - `printStudentInfo()`: This method should print the student's information in the format: "John Smith is 22 years old."
        - `setAge(int age)`: This method should set the age of the student.

5. **Create the StudentTest Class**

    - Create another class named `StudentTest` that contains the `main` method.
    - In the `main` method:
        - Create two `Student` objects using both constructors.
        - Use the `setAge` method to set the age for the student created without age.
        - Print the information for both students.

### Example Program

User   Interaction

The program's output may look like this:

```
John Smith is 22 years old.
Jim Foo is 23 years old.
```

### Example Implementation

```java
public class Student {
    private String name;
    private String lastName;
    private int age;
    private static int studentCounter = 0;

    // Full constructor
    public Student(String name, String lastName, int age) {
        this.name = name;
        this.lastName = lastName;
        this.age = age;
        studentCounter++;
    }

    // Partial constructor
    public Student(String name, String lastName) {
        this.name = name;
        this.lastName = lastName;
        this.age = 18; // Default age
        studentCounter++;
    }

    public void printStudentInfo() {
        System.out.println(name + " " + lastName + " is " + age + " years old.");
    }

    public void setAge(int age) {
        this.age = age;
    }

    public static int getCounter() {
        return studentCounter;
    }
}

public class StudentTest {
    public static void main(String[] args) {
        Student student1 = new Student("John", "Smith", 22);
        Student student2 = new Student("Jim", "Foo");
        student2.setAge(23);

        student1.printStudentInfo();
        student2.printStudentInfo();

        System.out.println("Total students created: " + Student.getCounter());
    }
}
```

## Hints

- Use the constructor to initialize instance variables when creating a new `Student`.
- Use the `printStudentInfo()` method to display student information.
- Use the static method `getCounter()` to retrieve the total number of `Student` instances created.

## Notes

- Ensure that the class name matches your file name if you use a different name.
- Test the program with various inputs to ensure accuracy.
- Document your code with comments to explain the functionality.

Happy coding! 🎉