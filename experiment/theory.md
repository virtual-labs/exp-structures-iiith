In C programming, arrays are useful when you need to store many values of the same type. However, many real-world records contain different kinds of data that belong together. A student record, for example, may include a name, roll number, gender, course, and marks. These values are related, but they are not all of the same type. C structures are designed for exactly this situation.

A structure is a user-defined data type that groups variables of different data types under one name. This makes programs easier to organize, read, and maintain. Instead of handling each related value separately, you can treat the whole record as one unit.

For example, a student record can be defined as:

```

struct student_record {
    char name[100];
    int rollnumber;
    char gender;
    char stream[100];
    float marks;
};
```

This definition creates a structure type named `student_record`. You can then declare variables of this type:

```

struct student_record student1;
struct student_record student2;
```

If you need to handle many students, you can also create an array of structures:

```
struct student_record students[100];
```

To access members of a structure, use the dot (`.`) operator:

```

strcpy(student1.name, "Abc");
student1.rollnumber = 24;
student1.gender = 'm';
strcpy(student1.stream, "Computer Science");
student1.marks = 84.5;
```

Structures are stored as a group of related fields in memory. When one structure variable is assigned to another, all the members are copied together. For example, `student2 = student1;` copies the complete record from `student1` to `student2`.

#### Why structures are useful

Structures are better than arrays when a single logical entity has multiple pieces of information of different types. Arrays store repeated items of the same type, while structures store related items of different types. For that reason, structures are commonly used for records such as students, employees, products, and bank accounts.

#### Nested and typedef structures

Structures can also be nested inside other structures. This is helpful when a record has sub-parts, such as an address inside a student record. In C, the `typedef` keyword is often used to give a shorter and cleaner name to a structure type.

#### Example of practical use

Suppose you want to store and update student details in a program. A structure allows you to pass the full record to a function, update selected fields, and return the updated data in a clear and controlled way. This is why structures are a key part of Computer Programming labs: they help model real-world data logically and efficiently.

Structures are powerful because they let you build custom data types that match the problem you are solving, making your programs easier to write, debug, and extend.
