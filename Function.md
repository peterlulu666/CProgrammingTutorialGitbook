# Function      

## Function      

Reusability.     

Understandable.     

Productivity.      

# C function      

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
// Function Declaration        
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





        





       





























