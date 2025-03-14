# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.


To test the sorting algorithm, I would use reverse-sorted lists (for worst case runtimes) and run linearly larger lists through the algorithm and compare their runtimes. For example, I would run a reverse-sorted array of length 100, then of 200, then 300, etc. I would compare the runtimes to see if they increase linearly. If the runtime differences are negligaile, I can work with factors of thousands or ten-thousands for the input sizes. I would similarly compare their run times for being linear. If an input of size n has a runtime of around t, I would expect an input size of 10n to have a runtime of around 10t. I may start out with larger input sizes to reach the asymptotic complexity of the runtime of the sorting algorithm. 

I believe that X is incorrect. To even process (read) each element of an array would take n time. For this algorithm to only take n time, each element must be sorted to where it needs to go after only being "read" once. It must only make a finite (not n) amount of operations/comparisons to know exactly where to place this item, and thus not being able to check the rest of the array. This also would assume this sort is in place, as creating a temporary array to store these values in would add another n time. 

“I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.” - Natalie Sleight
