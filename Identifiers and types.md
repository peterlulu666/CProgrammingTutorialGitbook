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
* `const identifier = value`.      





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

## Conditional operator        

Conditional operator `?`.      

      



