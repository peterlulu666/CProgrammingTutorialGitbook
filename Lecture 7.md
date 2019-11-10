# Lecture 7      



## Pointers to Arrays and Strings      


This lecture looks at the relationship between pointers and arrays. Arrays are a natural use for pointers because they reprresent contigously allocated blocks of memory that are often addressed sequentially. As we will see, the sequential access pattern makes it attractive to use pointers rather than array indexing operations to access data. Using pointers avoids an additional set of address arithmetic calculations that must be performed each time.

We will also look at how arrays are passed to functions, and how the C compiler translates C operations written in terms of arrays into equivalent pointer operations on the arrays. In this way, C arrays are actually passed to functions by reference because it is the address of the array that is being passed by value.

Finally, we will look at how the C string functions use pointers to implement more string operations, including ones we have already seen and new ones that provide more advance operations.        



## Lecture      

{% urlembed %}
assets/Lecture7.pdf
{% endurlembed %}      















