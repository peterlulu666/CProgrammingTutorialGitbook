# Memory allocation and management      

## `malloc` and `calloc`     

```c      
#include <stdlib.h>
#include <string.h>
#include <stdio.h>

int main() {
    char name[100];
    strcpy(name, "Allen");
    printf("%s\n", name);
    
    char *sentence;
    // Dynamic memory allocation 
    sentence = malloc(200 * sizeof(char));
    // Initialize allocated memory     
    strcpy(sentence, "Allen is a computer science student");
    // Print string       
    printf("%s\n", sentence);
    
    char *paragraph;
    // Dynamic memory allocation      
    paragraph = calloc(200, sizeof(char));
    // Initialize allocated memory      
    strcpy(paragraph, "Kevin is a computer science student.");
    // Print string       
    printf("%s\n", paragraph);      

    return 0;
}            

```      

## `strlen`       

```c        
#include <stdlib.h>
#include <string.h>
#include <stdio.h>

int main() {
    char *sentence;
    // Dynamic memory allocation
    sentence = malloc(strlen("Computer science student. "));
    // Initialize allocated memory
    strcpy(sentence, "student");
    // Print string        
    printf("%s\n", sentence);      

    return 0;
}

```      

## `strdup`      

```c        
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
    char *words;
    // Initialize string            
    words = strdup("Allen is a computer science student. ");           
    // Print string      
    printf("%s\n", words);
  
    return 0;      

}      

```                    

## `realloc` and `free`        

```c        
#include <stdlib.h>
#include <string.h>
#include <stdio.h>

int main() {
    char name[100];
    strcpy(name, "Allen");
    printf("%s\n", name);
    
    char *sentence;
    // Dynamic memory allocation 
    sentence = malloc(200 * sizeof(char));
    // Initialize allocated memory        
    strcpy(sentence, "Allen is a computer science student. ");
    // Print string        
    printf("%s\n", sentence);
    
    char *paragraph;
    // Dynamic memory allocation      
    paragraph = calloc(100, sizeof(char));
    // Initialize allocated memory      
    strcpy(paragraph, "Kevin is a computer science student. ");
    // Print string        
    printf("%s\n", paragraph);      

    // Increase the size of an allocated memory        
    paragraph = realloc(paragraph, 200 * sizeof(char));
    // Concatenate to extended memory            
    strcat(paragraph, "Kevin is a programmer. ");       
    // Print string      
    printf("%s\n", paragraph);
    // Release memory        
    free(paragraph);      

    return 0;
}            

```  

## `realloc` `strlen` and `free`                

```c        
#include <stdlib.h>
#include <stdio.h>
#include <string.h>

int main() {
    char *words;
    // Memory allocation
    words = malloc(strlen("Computer science student. "));
    // Initialize memory      
    strcpy(words, "student ");
    // Print string      
    printf("%s\n", words);
    // Increase the size of allocated memory        
    words = realloc(words, strlen("Programming "));      
    // Concatenate to extended memory      
    strcat(words, "Programming");
    // Print string     
    printf("%s\n", words);                            
    // Release memory      
    free(words);            

    return 0;
}        

```        







        





        















