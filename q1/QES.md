# Q.E.S. - 80

##Problem
![seq](http://compete.sctf.io/problems/2015q1/seq.png "seq")


##Solution

So this question provided minimal clues to figure out what to do. The two main spots to look at are in the name and file name of the picture. The name QES reversed is seq, and the picture is named seq. From that we can infer that it stands for sequence and the table is a sequence. However using https://oeis.org/ a sequence database, the numbers don't fit any known sequences. We have to assume that it is multiple sequences fit together then. From here, one could do a few things:

One could recognize the fibonacchi numbers interspread in the table. We check where these numbers are, and it is much more obvious in the later two rows as in the first one there exists four 1's and not all of those are in the fib. sequence. We see its every third number thats part of the sequence. From there, it makes sense that there are two other sequences in the table. The table is split into 1/3 fib and 2/3 other numbers. It's logical to assume they are even so each sequence occupies 1/3 of the table. Also, no other sequence will match the remaining numbers. After plugging in every third number again to the databse, we can figure out the two other seqences. These are the lucas numbers and the pentagonal numbers. 

We can also just imagine it being two sequences put together, but when we input every other number into the database nothing shows up. We try it being three sequences together and there we find there are sequences that match it. These are the fibonacci numbers, the lucas numbers, and the pentagonal numbers.

![coloredSeq](http://s16.postimg.org/pwvjc7g5x/QES.png "coloredSeq")

The flag is just the rest of the grid.

    13  29  70  21  47  92  34
    76  117 55  123 145 89  199
    176 144 322 210 233 521 247

##Flag

>13297021479234761175512314589199176144322210233521247
