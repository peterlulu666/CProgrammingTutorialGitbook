# Arrays      

## Array     

Array is a collection of variables of the same type.      

Array index.     

Declare array `array type array name [array size]` `int arr [6]`.      

Declare and initialize array `array type array name [array size] = {array element}` `int arr [6] = {1, 2, 3, 4, 5, 6}` `int arr [] = {1, 2, 3, 4, 5, 6}`.              

## 2D array      

Declare 2D array `array type array name [number of rows][number of columns]` `int arr [3][3]`.     

Declare and initialize 2D array `array type array name [number of rows][number of columns] = {array element}`.                      

```        
int array [3][3] = {{1, 2, 3}, 
                    {4, 5, 6}, 
                    {7, 8, 9}};     


int array [][3] = {{1, 2, 3}, 
                    {4, 5, 6}, 
                    {7, 8, 9}};        

```      

> **[info] 2D array**      
> * When declaring a 2D array, the number of columns is required.      

## 3D array        

Declare and initialize 3D array `array type array name [number of rows][number of columns][index of element] = {array element}`.      

```        
int array [3][3][3] = {{10, 20, 30}, {40, 50, 60}, {70, 80, 90}},     
                      {{15, 25, 35}, {45, 55, 65}, {75, 85, 95}},      
                      {{16, 26, 36}, {46, 56, 66}, {76, 86, 96}};      

```        





## String      

Initialize string      

```        
char hello[ 6]  = { 'H', 'e', 'l', 'l', 'o', '\ 0'}; 
char hello[ ] = { 'H', 'e', 'l', 'l', 'o', '\ 0'}; 
char hello[ ]  = "Hello";  // compiler supplies '\0'        

```      



## Assignment      



DUE DATE: Wed, 19 Sept by 11:59:59pm
Include all the specified functions in a file "assignment-3.c". Include a main program that calls the functions with test data and prints the results returned by the functions. Label the output so someone else can understand it. You must provide a documentation block for each function describing its purpose, parameters, and return values as appropriate. Check your file in to the CCIS GitHub repository 2017FACS5001SV/assignment-3-ccisID that was created by your instructor for your ccisID.

### Problem 1
Write a function void initArray(unsigned int n, int array[], int value) that initializes all n elements of the input array to the specified value. Test the function in the main() function by calling it with arrays of size 0, 1, and one or two other small sizes, and printing the array on return. Be sure to label the output so someone reading it can verify the result.

Here are some examples for int arrays a0 of lenght 0, a1 of length 1, etc.

initArray(0, a0, 25)  result: { }
initArray(1, a1, 42)  result: { 42 }
initArray(3, a3, 88)  result: { 88, 88, 88 }
initArray(6, a6, 14)  result: { 14, 14, 14, 14, 14, 14 }
### Problem 2
Write a function int wordCount(char str[]) that counts the number of words in the input string and return the count as the function result. A word is a sequence of characters that does not contain a space character (' '). The final word will end with the '\0' end of string character. Use local counters, and a loop to implement this function. (Hint: what is the reliationship between the number of spaces and the number of words if just one space separates words?)

Test this function by passing it test strings and verifying that function returns the expected word count. Here are several examples for you to use in testing:

* ""  length: 0, word count: 0
* "the"  length: 3, word count: 1
* "two words"  length: 9, word count: 2
* "the quick brown fox"  length: 19, word count: 4      


Although it is not required, consider how to make your function work corectly if there could multiple spaces before and afterwords.      







<br/>
     





## Programming      

{% github_embed "https://github.com/peterlulu666/CProgrammingTutorial/blob/master/assignment-3.c" %}{% endgithub_embed %}      














































        

























