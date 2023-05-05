Download Link: https://assignmentchef.com/product/solved-cso201-lab1-simple-c
<br>
<h1>Counting and Replacing Vowels</h1>

Write a C function int countVowels(char *str)

You may assume that str points to a legal C string. For this problem the only vowels are ’a’, ’A’, ’e’, ’E’, ’i’, ’I’, ’o’, ’O’, ’u’, and ’U’. The int returned by countVowels() is the total number of vowels found in the string (pointed to by) str. In addition, countVowels() modifies str, specifically it removes every vowel.

Example: if originally str =”<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="23424140107663">[email protected]</a>”, countVowels(str) returns 2 and, after the call, str=”<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="1371702053">[email protected]</a>”.

<h1>2           Ordering Strings by Length</h1>

Consider a string char *str. If you wanted a function f() to change a character in str to another character and return an int you would declare int f(char *str)

However, in this problem you are to write a function f() that is to change not characters, but strings themselves.. Hence the caller must write f(&amp;str) and the declaration becomes int f(char **str)

Write a C function int reorder(char **s1, char **s2, char **s3)

If all the strings are of equal length, reorder() leaves all three strings unchanged, returns 3, and prints “All 3 are equal length.”

If exactly two of the strings are equal in length, reorder() leaves all three strings unchanged, returns 2, and prints “Two are equal length.”

If all three strings are different in length, reorder() returns 1, sets s1 to the longest string, sets s2 to the middle length string, and sets s3 to the shortest string, and prints “all three are unequal length.” Feel free to use the strlen() library function.

<h1>3           Upper and Lower Case</h1>

Write a C main() program int main(int argc, char *argv[]) This program has two optional command line argument, “-d” (indicating duplicate) and “-u” (indicating uppercase). As we did in class these may be combined in several ways (search for “pink and yellow” in the lecture notes). Your program reads characters with getchar() and, for each character read (call it C), the program prints corresponding character(s) using putchar().

<ol>

 <li>If there are no optional arguments, C is printed unchanged.</li>

 <li>If the duplicate option is present C is printed twice.iii. If C is alphabetic and the uppercase option is present C is printed in upper case.</li>

 <li>If both options are present, C is printed twice and, if C is a letter, both copies are printed in uppercase.</li>

</ol>

Feel free to use the toupper() library function.

<em>Lab 1—Simple C                                                     Computer Systems Organization 201 2020-21 Spring                                                Page </em>2

<h1>4           Prime Numbers</h1>

<strong>4.1 </strong>isPrime() <strong>(10 Points)</strong>

Write a C function int isPrime(int n)

isPrime(n) returns 1 if n is prime and returns 0 otherwise. You may assume n is an integer greater than 1.

<strong>4.2          A C main Program to Test isPrime() (15 Points)</strong>

int main(int argc, char *argv[])

This program first checks that argc==3. If it is not, the program prints an error message and terminates. You may assume that argv[1] and argv[2] are characters containing only digits. Have atoi() convert argv[1] and argv[2] to integers called arg1 and arg2. Confirm that arg1 <em>&lt;</em>= arg2 (print an error message if this is not so). Finally, for all n, arg1 <em>&lt;</em>= <em>n&lt;</em>= arg2, call isPrime(n) and print whether <em>n </em>is prime.

<h1>5           Three Command-line Arguments</h1>

Write a C main program that accepts three (non-optional) command-line arguments (not counting the command name itself). Call the first argument str, call the second except and call the third dup. Each argument is a string, i.e., a pointer to a char. Your program does all the following.

<ol>

 <li>Checks that every character C in str is a lower-case letter. If a character is not a lower-case letter, then C is “illegal” and you print an error message and terminate the run immediately.</li>

 <li>Assuming C is legal, check if it also appears in the except</li>

 <li>If C does appear in except, skip it (i.e., print nothing for this character) and proceed to the next character in str.</li>

 <li>If C does <strong>not </strong>appear in except, check if it appears in dup.</li>

 <li>If C does <strong>not </strong>appear in either except or dup, print C using putchar().</li>

 <li>If C appears in dup but not in except, print C twice using putchar().</li>

</ol>