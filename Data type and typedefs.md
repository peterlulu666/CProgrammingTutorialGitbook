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

{% github_embed "https://github.com/peterlulu666/CProgrammingTutorial/blob/master/PlayingCard.c" %}{% endgithub_embed %}        





















## Struct      

Array is the collection of the same type data. Likewise, struct is the collection of the different type data.          

Struct is an aggregation of heterogeneous types that represent a record.      

```c        
#include <stdio.h>
#include <string.h>

// Define struct
struct Books{
    char title[100];
    char author[100];
    char subject[100];
    int book_id;

};

int main(){
    // Declare struct
    struct Books book1;
    struct Books book2;
    // Assign struct      
    strcpy(book1.author, "Allen");
    strcpy(book1.title, "C Programming");
    strcpy(book1.subject, "Computer");
    book1.book_id = 123456;
    // Access struct        
    printf("%s\n", book1.title);
    printf("%d", book1.book_id);     

    return 0;

}      

```      

```c      
#include <stdio.h>
#include <string.h>

// define struct
struct Books {
    char title[100];
    char author[100];
    char subject[100];
    int book_id;

};

// struct as function parameter
void printBook(struct Books books) {
    printf("%s\n", books.title);
    printf("%d\n", books.book_id);

}

int main(){
    // declare struct
    struct Books book_one;
    struct Books book_two;
    // assign struct
    strcpy(book_one.title, "Programming");
    book_one.book_id = 123456;
    strcpy(book_one.subject, "Computer");
    // call the printBook function     
    printBook(book_one);        
    return 0;

}
      
```      













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


## Assignment    

<div id="btab-5" class="t_div assignment ui-tabs-panel ui-widget-content ui-corner-bottom" aria-labelledby="ui-id-7" role="tabpanel" aria-hidden="false" style="display: block;">
                <ul class="assign_info">
                    <li>
                    DUE DATE: <span class="due_date">Wed, 3 Oct before 11:59:59pm</span><br>
                    </li>
                </ul>

                <p>
                This problem is similar to the example shown on slides 21-24 of Lecture 3. Write a program "assignment-6.c" that creates and manages geometric shapes.
                </p>
                <ol>
                <li>
                Define and typedef a struct <strong>Point</strong> that contains two double variables
                <em>x</em> and <em>y</em>. An instance of <em>Point</em> represents a point in
                Cartsian space.
                </li>
                <li>
                Define and typedef a struct <strong>Circle</strong> that contains
                a double variable <em>radius</em> and a <em>Point</em> variable <em>center</em>.
                </li>
                <li>
                Define and typedef a struct <strong>Rectangle</strong> that contains
                a <strong>Point</strong> variable <em>origin</em> that is the top left corner of
                the rectangle, and two double variables <em>width</em> and
                <em>height</em>.
                </li>
                <li>
                Create a function <em>distanceofPoints()</em> that takes const pointers to two
                <strong>Point</strong> structs, and computes the distance between them. The distance between
                two points is the square root of the square of the x distances plus the square
                of the y distances for the two points. The function returns a double. </li>
                <li>
                Create a function <em>intersectsCircles()</em> that takes const pointers to two
                <strong>Circle</strong> structs <em>circle1</em> and <em>circle2</em>and returns true
                if the two circles intersect and false otherwise. Two circles
                intersect if the distance between their centers is less than the sum
                of the two radii (if they are equal, the two circles touch but do not
                intersect. </li>
                <li>
                Create a function <em>getBoundingBox()</em> that takes a const pointer to a in input
                parameter <strong>Circle</strong>, <em>circle</em> and a pointer to a <strong>Rectangle</strong>
                result parameter <em>boundingBox</em>. The function sets the fields of
                <strong>Rectangle</strong> to the bounding box that encloses the circle. The function
                returns the <strong>Rectangle</strong> result parameter pointer.
                </li>
                <li>
                Create a main program that tests the
                <em>intersectsCircles()</em> function using the following cases:
                <ul>
                <li>
                circle1 at 0,0 radius 10, and circle2 at 21,0, radius 10: do not intersect
                </li>
                <li>
                circle1 at 0,0 radius 10, and circle3 at 20, 0, radius 10: do not intersect
                </li>
                <li></li>
                circle1 at 0,0 radius 10, and circle4 at 19,0, radius 10: intersect
                </ul>
                </li>
                <li>
                Also in the main program, test the <em>getBoundingBox()</em> function by
                declaring an uninitialized <em>Rectangle</em> <em>boundingBox</em> and
                calling the <em>getBoundingBox()</em> function for <em>circle1</em>,
                <em>circle2</em>, <em>circle3</em>, and <em>circle4</em>. Print the origin,
                width, and height of the <em>boundingBox</em> for each circle.
                </li>
                </ol>
            </div>     




## Programming    


{% github_embed "https://github.com/peterlulu666/CProgrammingTutorial/blob/master/assignment-6.c" %}{% endgithub_embed %} 































