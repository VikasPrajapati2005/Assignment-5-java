# Assignment-5-java
Demonstrate inheritance using a base Person class and subclasses Teacher, Student.
// Base class
class Person {
    String name;
    int age;

    // Constructor
    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Method to display person details
    void displayInfo() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

// Subclass: Student
class Student extends Person {
    String studentId;

    Student(String name, int age, String studentId) {
        super(name, age); // Call the constructor of Person
        this.studentId = studentId;
    }

    void displayInfo() {
        super.displayInfo(); // Call displayInfo from Person
        System.out.println("Student ID: " + studentId);
    }
}

// Subclass: Teacher
class Teacher extends Person {
    String subject;

    Teacher(String name, int age, String subject) {
        super(name, age);
        this.subject = subject;
    }

    void displayInfo() {
        super.displayInfo();
        System.out.println("Subject: " + subject);
    }
}

// Main class to test inheritance
public class InheritanceDemo {
    public static void main(String[] args) {
        Student student = new Student("Alice", 20, "S1234");
        Teacher teacher = new Teacher("Mr. Smith", 45, "Mathematics");

        System.out.println("Student Info:");
        student.displayInfo();

        System.out.println("\nTeacher Info:");
        teacher.displayInfo();
    }
}
