In C programming, arrays are useful for storing and working with many values of the same type, such as a list of numbers or characters. However, sometimes you need to keep together different types of information that belong to a single entity. For example, a student's record might include their name (text), roll number (number), gender (character), and stream (text).

To handle such cases, C provides structures. A structure is a user-defined data type that allows you to group variables of different types under one name. This makes it easier to organize and manage related data.

For example, to store information about students, you can define a structure like this:

```
struct student_record {
    char name[100];
    int rollnumber;
    char gender;
    char stream[100];
};
```

This creates a new data type called `student_record` that contains a name, roll number, gender, and stream. You can then create variables of this type:

```
struct student_record student1, student2;
```

Or, if you want to store records for many students, you can create an array of structures:

```
struct student_record students[100];
```

To access or set the values inside a structure, use the dot (`.`) operator. For example:

```
strcpy(student1.name, "Abc");
student1.rollnumber = 24;
student1.gender = 'm';
strcpy(student1.stream, "Computer Science");
```

All the data for a structure is stored together in memory. If you copy one structure variable to another (e.g., `student2 = student1;`), all the fields are copied at once.

Structures are powerful because they let you create complex data types that match real-world information, making your programs easier to write and understand.
