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




## Assignment      



DUE DATE: Mon, 24 Sept by 11:59:59pm
Coming soon.
Tic Tac Toe Game
You will implement several functions in a Tic Tac Toe game. I have already implemented the main that will call the functions you have to write. The board will be stored in a 2 dimensional 3x3 array of char.

Implement the following functions:

initBoard(char board[3][3]) – This function initializes the 3x3 board array to space characters representing unmarked positions.
displayBoard(char board[3][3]) – This displays the tic-tac-toe board with vertical and horizontal grid lines formed with dashes and vertical bars, using the characters in the 3x3 board array.
-------------
| X | O |   |
-------------
|   | O |   |
-------------
| O | X | X |
-------------
markTheBoard(char board[3][3], char mark, int position) – This function marks the board based on the position (1-9) and marker character passed in.
hasWon(char board[3][3], char mark) – Returns true if the marker character of the player passed in as won the game by examining the values in the 3x3 board array.
isTie(char board[3][3]) – Tells if the board is currently a tie.
You will use the code in your repository, which is under 2018FACS5001SV/assignment-4-CCIS_ID.      

<br/>      











## Programming      

{% github_embed "https://github.com/peterlulu666/CProgrammingTutorial/blob/master/assignment-4.c" %}{% endgithub_embed %}      















































