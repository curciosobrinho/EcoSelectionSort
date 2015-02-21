# EcoSelectionSort (and brothers)
New sort algorithms derived from selection sort algorithm. Implementation in C (plain C)

I have created 3 algorithms all using the same principles, 2 or more searches in the same for loop.<br>
They are EcoSelectionSort (2 searches inside the loop), EcoTurboSelectionSort (4 searches inside the loop) and EcoPowerSelectionSort (8 searches inside the loop).

The idea is open the mind about the options inside loops.
Why use only 1 value of the array at a time? Why not compare more than one?

I hope that this implementation shows that it is worth to think about it.

# Background reason
We all know that O(n^2) sorting algorithms like insertion or selection sort are not the best options for big arrays.
But selection sort is slower that insertion sort.

The new algotrithms as implemented are faster than insertion sort for arrays with ~500 or more elements.

The above code shows the difference in time  - microseconds - (I know that we must NOT use time to measure, but as they will ALL run with the same array and in the same machine  - your machine - I think we can try)

Just to give you an idea, inside a virtual machine running ubuntu with 2 cores and 2Gb memory, I had the following result:<br>

<br>
Array size = 50000<br>
BubleSort - Time : 8028810 us<br>
SelectionSort - Time : 3431547 us<br>
InsertionSort - Time : 2041612 us<br>
MergeSort -  Time :  12770 us<br>
EcoSelectionSort - Time : 2055795 us<br>
EcoTurboSelectionSort - Time : 1611034 us<br>
EcoPowerSelectionSort - Time : 1487109 us<br>
<br>
* Time is in us (microseconds)<br>

# How to run
If you use clang to compile just:<br>
clang -o sorts sorts.c

Or use your prefered compiler.
