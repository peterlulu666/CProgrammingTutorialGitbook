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

We would declare the enum like this `enum identifier(opt) {enumerator-list}`.     

```c     
typedef enum { Sun, Mon, Tue, Wed, Thu, Fri, Sat } DayOfWeek;      

```      

This makes DayOfWeek a type, similar to int. As with any type, we can declare variables of that type.      

```c     
int main(){
    DayOfWeek homeWorkDueDay = Tue;
    printf("%d ", homeWorkDueDay);

}      

```        






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

1. Create an Animal enum for the animals listed above in that order, and add Animal_kinds at the end of the enum as the number of kinds of Animals.
2. Create a Zoo typedef as an array of unsigned int representing the counts for each kind of Animal in the Zoo's collection.
3. Write a function void makeZoo(Zoo aZoo) that initializes the Zoo to have no Animals in its collection.
4. Write a function unsigned int addAnimal(Zoo aZoo, Animal anAnimal) that adds an Animal to the Zoo and returns the current count for that Animal.
5. Write a function const char* getAnimalName(Animal anAnimal) that returns the name of the Animal. Declare a local array static const char *animalNames[], initialized with the literal strings for the Animal names using the Animal enumeration value as an index into the animalNames array. The function can return the string because the animalNames is a static array of literal strings.
6. Write a function void printZoo(const Zoo aZoo) that prints an inventory of the animals in the Zoo. The output is one animal per line with the count in a blank-padded field of 3 digits (%3u), followed by a tab character ('\t') followed by the name of the animal.The function uses getAnimalNames() to get the Animal names.
7. Write a int main(void) function that creates a Zoo and calls makeZoo() to initialize it. Then it calls addAnimal() to add a number of each Animal to the Zoo corresponding to the enumeration value of the Animal. For each Animal added, it prints the Animal name and the new count using this format: "Added %s count: %u\n" Finally it uses printZoo() to print animals in the Zoo and their counts.        


<br/>      











## Programming      

{% github_embed "https://github.com/peterlulu666/CProgrammingTutorial/blob/master/zoo.c" %}{% endgithub_embed %}        



































