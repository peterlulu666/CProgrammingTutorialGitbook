# Pointers to Arrays and Strings        

## Pointers to Arrays      

We would use pointer to access array element.      

     

                   



```c      
    int arr[] = {1, 2, 3, 4, 5, 6};
    int *arrptr = arr;
    for (int i = 0; i < sizeof(arr) / sizeof(arr[0]); ++i) {
        arrptr = arr + i;
        printf("%d ", *arrptr);


    }     

```      

> **[info] Pointers to Arrays**
> * The pointer `arrptr` points to the location of the first array element.      

* The `arr` is the address of the first array element. The `arr + i` is the address of the ith array element.      

* The `*arrptr` is the content of array element. The `arrptr = arr + 0` is the array element in index 0. The `arrptr = arr + i` is the element in index i.      


> 
     

```c      
    int *arrayPointer = arr;
    for (int i = 0; i < sizeof(arr) / sizeof(arr[0]); ++i) {
        printf("%d ", *arrayPointer++);


    }      

```        

> **[info] Pointers to Arrays**
> * This would be more efficient.      
>       






## Pointers to strings      

The `atoi()` function.      

```c     
/** This function returns an int representing
 * the integer value of the string.
 *
 * @param str the input string
 * @param the integer represented by the string
 * @return the integer value for the input string
 */
int atoiTest(const char *str) {
    while (isspace(*str)) {
        str++;
    }
    bool negtive = false;
    if (*str == '-') {
        negtive = true;
        str++;
    }
    int result = 0;
    for (; isdigit(*str); ++str) {
        int digit = *str - '0';
        result = (10 * result) + digit;
    }
    if (negtive) {
        return -result;
    }
    return result;
}      

```      






















