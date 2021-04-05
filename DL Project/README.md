Our project is based on solving the problem of String Matching. In today's world, when data is required everywhere, everyone inputs their data. But often while inputting the data, people use different short forms or spellings or even sometimes there are double entries. Since its a lot of manual labour work to sit and check all these errors and bring into one format, our project solves this error. This problem is faced in almost all the corporate and other offices. Therefore there is a huge need to overcome this. 

In our project, we have used the Fuzzy Wuzzy logic to overcome this problem.

Fuzzy Wuzzy Logic -

Fuzzywuzzy is a python library that uses Levenshtein Distance to calculate the differences between sequences and patterns that was developed and also open-sourced by SeatGeek.
Levenshtein Distance calculates distance between two strings.

Example 
Gaurav & Saurav 
Distance will be 1 
Because of G & S 


Kitten & Sitting has distance of 3 

kitten → sitten (substitution of "s" for "k")

sitten → sittin (substitution of "i" for "e")

sittin → sitting (insertion of "g" at the end).



The Levenshtein distance has several simple upper and lower bounds. These include:

It is at least the difference of the sizes of the two strings.

It is at most the length of the longer string.

It is zero if and only if the strings are equal.

If the strings are the same size, the Hamming distance is an upper bound on the Levenshtein distance. The Hamming distance is the number of positions at which the corresponding symbols in the two strings are different.
The Levenshtein distance between two strings is no greater than the sum of their Levenshtein distances from a third string (triangle inequality).


Fuzz Ratio  simple comparison between two strings 

It works strictly example (‘Data Science’, ‘Data Science') it will give 100  match 


Fuzz partial ratio in this if partial matches are correct it gives output (Gaurav , Gaurav#) it will give 100 % still 

But again in second scenario ( Hello Kapoor, Hello Vidhi Kapoor ) will give less accuracy because new token has been introduced 


Fuzz Token sort ratio in this it takes token into consideration

fuzz.token_sort_ratio(DL Project, Project DL) score 100 

fuzz.token_sort_ratio(DL Project, Project Project DL) 88 

fuzz.token_set_ratio (DL Project, Project Project DL) 100 


Therefore fuzzy wuzzy logic suits the best for our project.

How our project works:

Takes a dataset as input (excel file)

Gives the required output that satisfies the string in the Flask as well as saves the output in the excel file. 






