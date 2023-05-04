Download Link: https://assignmentchef.com/product/solved-cs590-homework2-recurrences-and-sorting-2
<br>
<strong>Part 2: Radix-sort on strings </strong>

The class random generator has been updated (<em>random_generator.h</em> and <em>random generator.cpp</em>) by a member function which generates random strings of up to a given length with characters between “a” and “z”.

<ul>

 <li><em>char* random_string(int max, int&amp; m)</em></li>

</ul>

The function picks a string length <em>m</em> at random in between 1 and <em>max</em> (<em>1&lt;=m&lt;= max</em>). The length <em>m</em> of the random string is stored in the second parameter. The function then allocates <em>m + 1 </em>characters. The first <em>m </em>characters (<em>0……m-1</em>) are chosen at random in between the characters “a”

and “z”. The <em>m</em>-th character is set to 0 in order to mark the end of the string.




A string in C is represented by an array of characters (e.g. <em>char *st</em>). Each character is an ASCII representation of a specific integer value. The character “a” is a representation of the value 97 according to the ASCII table. The individual characters of the array/string can therefore be viewed as a digit.




<ol>

 <li>Implement an insertion sort algorithm for strings that sorts a given array of strings according to the character at position <em>d</em>. It is necessary to include the length of each string (<em>array A len</em>) as it is unclear whether or not the digit<em> d</em> A non-existing digit <em>d</em> is interpreted as a 0 in the sorting process. Add a parameter <em>int d </em>and <em>int* A_len</em> to the algorithm arguments and modify the given insertion sort algorithm accordingly. This algorithm should be implemented in the method below:</li>

</ol>

void insertion_sort_digit(char** A, int* A_len, int l, int r, int d)

Notes:

<ul>

 <li>Do not copy the characters itself, but only the pointer to the string/array of characters instead.</li>

 <li>Do not fill the strings with 0’s to make them of equal size.</li>

 <li>Do not compute the length of a string with <em>strlen</em>. Use the int array <em>A_len</em></li>

 <li>If you move a string within the array of strings then you must update the array containing the length of the strings accordingly.</li>

</ul>




<ol start="2">

 <li>Use this modified insertion sort algorithm to implement radix sort for an array of strings. Measure the runtime performance for <strong>arrays of random</strong> <strong>strings 5 times for every combination of array size n = 2500; 5000; 7500; 10000 and length of the random strings m = 25; 35; 45</strong>. Discuss your results. (You might have to adjust the value for <em>n</em> dependent on your computers speed, but allow each test to take up to a couple of minutes). This algorithm should be implemented in the method below:</li>

</ol>

void radix_sort_is(char** A, int* A_len, int n, int m)




<ol start="3">

 <li>Develop a <strong>counting sort</strong> algorithm for strings that sorts a given array of strings according to the character at position<em> d</em>. As for the insertion sort on digit <em>d</em>, a non-existing digit <em>d</em> is treated as a 0 throughout the counting sort. This algorithm should be implemented in the method below:</li>

</ol>

void counting_sort_digit(char** A, int* A_len, char** B, int* B_len, int n, int d)




Notes:

<ul>

 <li>Do not copy the characters itself, but only the pointer to the string/array of characters, instead.</li>

 <li>Do not fill the strings with 0’s to make them of equal size.</li>

 <li>Do not compute the length of a string with <em>strlen</em>. Use the int array <em>A_len</em></li>

 <li>When moving the string into its correct position you also have to move the length of the string into its correct position.</li>

 <li>You can use <em>int C[256]</em> to store the counters/positions.</li>

</ul>

<ol start="4">

 <li>Use this new counting sort algorithm to implement radix sort for an array of strings. Measure the runtime performance for <strong>arrays of random strings 5 times for every combination of array size n = 50000; 100000; 500000; 750000 and length of the random strings m = 25; 35; 45</strong>. Discuss your results. (You might have to adjust the value for <em>n</em> dependent on your computers speed, but allow each test to take up to a couple of minutes). This algorithm should be implemented in the method below:</li>

</ol>

void radix_sort_cs(char** A, int* A_len, int n, int m)