# Identifiers and types       

## Identifiers      

Identifiers are names of variable, arrays, function, structures, unions and labels.      

## Type      

* `bool`: 1 byte (8 bits) 
* `char`, (`signed char`), `unsigned char`: 1 byte (8 bits) 
* `short` (`signed short`), `unsigned short`: 2 bytes (16 bits) 
* `int` (`signed int`), `unsigned int` : 4 bytes (32 bits) 
* `long` (`signed long`), `unsigned long`: 8 bytes (64 bits) 
* `long long` (`signed long long`), `unsigned long long` : 8 bytes (64 bits) 
* `float`: 4 bytes (32 bits) 
* `double`: 8 bytes (64 bits) 
* `long double`: 16 bytes (80 bits)  (note: 10 bytes stored in 16 byte field)      

## String      

String is sequence of characters.      

## The void type      

A function returns `void`.     

A function has no parameter can accept `void`.      

Pointers to `void`. a memory allocation function `void *malloc( size_t size )` return a pointer to void which can be casted to any type of data.            


      

## Constant variable      

Constant variable      

* `#define identifier value`.     
* `const type identifier = value`.      





## Print      

Format specifiers in `printf` format string.        

* `bool`:  %d, %i 
* `char`: %c 
* `short`: %d, %i 
* `unsigned short`: %u 
* `int`: %d, %i 
* `unsigned int`: %u 
* `long`: %ld, %li 
* `unsigned long`: %lu 
* `long long`: %lld, %lli (see note) 
* `unsigned long long`: %llu (see note) 
* `float`: %f 
* `double`: %f 
* `long double`: %Lf 
* `string`: %s      

## Assignments operator            

We would declare a variable like this `type variable_name`.      

We would use assignments operator `=` to initialize a variable like this `variable_name = value`.      
      
We would initialize a variable in their declaration like this `type variable_name = value`.      



## Arithmetic operators      

Infix binary operators: `+`, `-`, `*`, `/`, `%`.      

Prefix unary operators: `++`, `--`, `+`, `-`.      

Postfix unary operators: `++`, `--`.      

Arithmetic assignment operators: `+=`, `-=`, `*=`, `/=`, `%=`.        

```c
int count = 0; 
int count1 = ++count; // count1 is 1, count is 1 
int count2 = count++; // count2 is 1, count is 2 
count *= count; // count is 4      

```      


## Relational operators      

* equals `==`.      
* not equal `!=`.      
* greater `>`.      
* less `<`.      
* greater or equal `>=`.      
* less or equal '<='.        

## Logical operators        

* logical AND `&&`.                 
* logical OR `||`.      
* logical NOT `!`.      

## Misc Operators        

Conditional operator `?`.       

Returns the size of a variable `sizeof()`.            

Returns the address of a variable `&`.     

Pointer to a variable `*`.      

## Assignment      


Define and initialize the following variable or constant with the appropriate type and value. In some cases, you will use operators to compute the value.     
<ol>
<li>An unsigned integer constant <em>squareOfThree</em> initialized by calculating 
the square of 3</li>
<li>A double precision floating point constant <em>e </em>initialized to Euler's constant 2.718281828459045</li>
<li>A boolean variable<em> isGreaterThan </em>initialized to the logical expression<em> 2.8 </em>&gt; <em>e</em></li>
<li>An integer variable <em>quotient</em> initialized to the ratio of sum 2+4+5 
divided by 3</li>
<li>A short integer variable <em>remainder</em> that is the remainder of 
11 with 3</li>
<li>A double precision variable <em>greaterValue </em>that is 2.8<em></em> if <em>isGreaterThan</em> is true and <em>e if isGreaterThan</em> is false.
</li><li>A single precision floating point constant <em>oneTenth</em> 
initialized to the ratio of 1.0 divided by 10.0</li>
<li>A character <em>hex7A</em> whose value is the hexadecimal constant 7A.</li>
<li>A character constant <em>charZ</em> initialized to 'Z'.</li>
<li>An unsigned short variable <em>numLetters</em> that is the number of letters between 'A' and 'Z' inclusive.</li>
</ol>      
For each variable or constant, provide a printf() statement using the apropriate field specifier that prints its name, its value, and its size in bytes.      





























      



