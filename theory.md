Arrays are used to store large sets of data and manipulate them but the disadvantage is that all the elements stored in an array are to be of the same data type. When we need a collection of different data items of different data types, such as integer, float etc., we can use a structure. Structure can be seen as datatype composed of different datatypes. For example, suppose you want to store information about students enrolling in a university. Then, you may naturally want to store information like Student Name, Roll Number, Gender, Batch, etc. Ofcourse, you can create separate arrays for storing each of these quantities, but notice that for each student this diverse data is highly related. So, using a structre to pack these data entries into a single variables would be a good choice. In this case we can define the structure as,

```
            struct student_record{
            char Name[100];
            int Roll;
            char gender;
            char Stream[100];
            };
```       

This definition will practically create a new datatype students_record having a 2 character arrays, one integer and one character. So, in the main function one can define variables of this new compound datatype as,

```
            student_record student1, student2;
```          

You can even define an array of structure variables like,

```
            students_record students[100];
```       

Now, the individual elements of a structure variable can be addressed by the dot(.) operator. For example, the variable student1 can initialized using the following statements:

```
            strcpy(student1.Name,"Abc");
            student1.Roll=24;
            student1.gender='m';
            strcpy(student1.Stream,"Computer Science");
```          

An interesting thing to note is that the memory allocation for the whole structure is done contigously. So, size of one variable of type student_record is 100+4+1+100=205 bytes. And, if r1 and r2 are two variables of the structure struct_record, then writing r1=r2 is equivalent to copying the data in 205 bytes corresponding to r2 and copying them into r1.
