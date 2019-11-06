# Function      

## Function      

Reusability.     

Understandable.     

Productivity.      

# C function      

Each function definition has the general form.      

<pre>
<code class="language-c">
// Documentation        
/**
* Description of function.
* @param param1 description of param1 
* …
* @param paramN description of paramN 
* @return description of return value 
*/ 
// Function definition        
return-type function-name (type1 param1, … , typeN paramN) { 
    // Function Body        
    statement-1; 
    …
    statement-M; 
    // Return statement returns return-value to caller        
    return return-value;     
}      

</code>    
</pre>      

We would declare a function, call a function in main() and define a function like this       

```c      
#include <stdio.h>
 
/* function declaration */
int max(int num1, int num2);
 
int main () {

   /* local variable definition */
   int a = 100;
   int b = 200;
   int ret;
 
   /* calling a function to get max value */
   ret = max(a, b);
 
   printf( "Max value is : %d\n", ret );
 
   return 0;
}
 
/* function returning the max between two numbers */
int max(int num1, int num2) {

   /* local variable declaration */
   int result;
 
   if (num1 > num2)
      result = num1;
   else
      result = num2;
 
   return result; 
}        

```        






## scope      

* Scope      
    - Visibility of variable.      
* Local scope      
    - Variables declared within a function block are known only to that function.                   
* Global scope      
    - Variables declared outside the function are unknown to the function.     


The `static` qualifier.      

```c
/** @file cfile1.c */ 
/** This function is visible only within this file*/ 
static void function1(void) { 
    …
} 
/** This function is visible everywhere in the global scope */ 
void function2(void) { 
    function1();      

}

```       

```c        
/** @file cfile2.c 
*/ 
/** This variable is visible only within this file*/ 
static int variable1; 
/** This variable is visible everywhere in the global scope */ 
int variable2;        

```      





        





       





























