# Lab 04 - SOP/POS and KMaps

In this lab, you’ve learned how to apply KMaps, Sum Of Products and Products of
sums to simplify digital logic equations. Then, you’ve proven out that they work
using an implemented design on your Basys3 boards.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Lab Summary

I this lab, we played around with KMaps. We found the SOP and POS of a function using values from the truth table and inserting the values into a KMap. Using the KMap we used either positive or negative logic depending on whether we are solving for SOP or POS.Both SOP and POS gave us an optimized for of the equation. We also saw how using the canonical expression (for POS/SOP) is much less efficient. It has a lot more terms and it isn't the optimzed version. Then, we used Verilog and coded in our functions and saw that all three version of the function (POS, SOP, canonical) all yield the same results within  the truth table, which meant that all three functions were equivalent to each other. 

## Lab Questions

### Why are the groups of 1’s (or 0’s) that we select in the KMap able to go across edges?
It is because the first and last rows and columns only change by 1 bit so they are tecnically next to eachother. That means that the map wraps around which lets valid groups cross edges. Another way to think about the KMaps is that the table can be wrapped around to create a cylinder. With a cylinder the two edges will be touching each other. 

### Why are the names Sum of Products and Products of Sums?
They are named after boolean expression structure. Sum of Products (SOP) means you OR together a bunch of AND terms. For Product of Sums (POS), it's basically the same idea but it follows negative logic and you OR together all the terms in each group and with each group you AND them together. Both SOP and POS results in a optimized function. 

### Open the test.v file – how are we able to check that the signals match using XOR?
XOR is 0 when 2 signals are the same and 1 when they are different. So you use XOR to check if 2 signals result in 0, which would be a match, or 1, which means mismatch.

