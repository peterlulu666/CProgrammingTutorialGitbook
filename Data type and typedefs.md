# Data type and typedefs      

## C programming language data type      

`bool`, `char`, `short`, `int`, `long`, `float`, and `double`.      



## Define      

**References** provide indirect access to values of another data type.        
**Sequences** are indexable homogeneous collections of another data type.        
**Aliases** provide an alternate name for another data type.        
**Enumerations** explicitly identify collections of discrete values that comprise data types.
**Aggregations** are heterogeneous combinations of other data types.        







## typedef      

A typedef is an alias for an existing data type. It does not create a new type in any sense; it merely adds a new name for some existing type.      












We would declare the typedef like this `typedef existing-type new-type`.      

```c      
typedef int Length;
Length len, maxlen;
Length *lengths[];


typedef char *String;
String p, lineptr[MAXLINES], alloc(int)
int strcmp(String, String);
p = (String) malloc(100);            

```      

> **[info] Primative Data Types**
> * Parameterize a program against portability problems.
> * Provide better documentation for a program.     
>  
 












## Enum      

An enum is an enumerated type that specifies a fixed set of choices.      

We would use `enum` to avoid "magic number" which is a numeric constant that appears in your code without explanation.               

We would declare the enum like this `enum identifier(opt) {enumerator-list}`.     

```c     
typedef enum { Sun, Mon, Tue, Wed, Thu, Fri, Sat } DayOfWeek;      
// This is the same as         
// const int Sun = 0;              
```      

This makes DayOfWeek a type, similar to int. As with any type, we can declare variables of that type.      

```c     
int main(){
    DayOfWeek homeWorkDueDay = Tue;
    printf("%d ", homeWorkDueDay);

}      

```        


### Playing card      
















## Struct      

Struct is an aggregation of heterogeneous types that represent a record.      


## Assignment      



DUE DATE: Fri, 29 Sept before 11:59:59pm
A zoo is a collection of animals. We can represent animals using an enum Animal whose identifiers are the animal names. For this assignment, our zoo has the following kinds of animal in its collection:

* anteater
* bear
* cheetah
* elephant
* giraffe
* lion
* monkey
* rhinoceros
* tiger
* zebra     

We can represent a Zoo as a typedef for an array of Animal whose elements count the number of each Animal in its collection. The value of each Animal can be used as an index into the Zoo array.

Write a C program "zoo.c" that creates and manages a zoo.
    

<ol>
            <li>
            Create an <strong>Animal</strong> enum for the 
            animals listed above in that order, and add 
            <em>Animal_kinds</em> at the end of the enum as
            the number of kinds of <strong>Animal</strong>s.
            </li>
            <li>
            Create a <strong>Zoo</strong> typedef as an array
            of <strong>unsigned
            int</strong> representing the counts for each 
             kind of <strong>Animal</strong> in the
            <strong>Zoo</strong>'s collection.
            </li>
            <li>
            Write a function 
            <em>void makeZoo(<strong>Zoo</strong> aZoo)</em>
            that initializes the Zoo to have no 
            <strong>Animal</strong>s in its collection.
            </li>
            <li>
            Write a function <em><strong>unsigned int</strong>
            addAnimal(<strong>Zoo</strong> aZoo, 
            <strong>Animal</strong> anAnimal)</em> that
            adds an <strong>Animal</strong> to the 
            <strong>Zoo</strong> and returns the current
            count for that <strong>Animal</strong>.
            </li>
            <li>
            Write a function 
            <em><strong>const char*</strong> 
            getAnimalName(<strong>Animal</strong> anAnimal)</em> 
            that returns the name of the 
            <strong>Animal</strong>. Declare a
            local array <em>static const 
            <strong>char *</strong>animalNames[]</em>, 
            initialized with the
            literal strings for the <strong>Animal</strong> 
            names using the <strong>Animal</strong> 
            enumeration value 
            as an index into the <em>animalNames</em>
            array. The function can return the string 
            because the <em>animalNames</em> is a static 
            array of literal strings.
            </li>
            <li>
            Write a function 
            <em><strong>void</strong> 
            printZoo(const <strong>Zoo</strong> aZoo)</em>
            that prints an inventory of the animals in the
            <strong>Zoo</strong>. The output is one animal 
            per line with the
            count in a blank-padded field of 3 digits (%3u),
            followed by a tab character ('\t') followed by
            the name of the animal.The function uses
            <em>getAnimalNames()</em> to get the 
            <strong>Animal</strong> names.
            </li>
            <li>
            Write a
            <em><strong>int</strong> 
            main(<strong>void</strong>)</em>
            function that creates a <strong>Zoo</strong>
            and calls <em>makeZoo()</em> to initialize it.
            Then it calls <em>addAnimal()</em> to add a number
            of each <strong>Animal</strong> to the 
            <strong>Zoo</strong> corresponding to the
            enumeration value of the <strong>Animal</strong>. 
            For each <strong>Animal</strong> added, it prints
            the <strong>Animal</strong> name and the new count
            using this format:
            "Added %s count: %u\n" Finally it uses 
            <em>printZoo()</em> to print animals in the 
            <strong>Zoo</strong> and their counts.
            </li>
            </ol>     


<br/>








## Programming      

{% github_embed "https://github.com/peterlulu666/CProgrammingTutorial/blob/master/zoo.c" %}{% endgithub_embed %}        



































