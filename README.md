Download Link: https://assignmentchef.com/product/solved-cs526-homework-assignment-2
<br>
This assignment has two parts. Part 1 is a practice of designing and implementing small <strong><em>recursive</em></strong> methods and Part 2 is an implementation of an application using the stack data structure.




<h1>Part 1 (40 points)</h1>




Create a file named <em>RecursionPractice.java</em> and implement the following two methods within the file.




(1). Write a recursive Java method named <em>recursiveProduct </em>that computes the product of two integers, <em>m</em> and <em>n</em>, using only additions and subtractions, as described below:




<em>recursiveProduct</em> (int <em>m</em>, int <em>n</em>)

Input: integers <em>m</em> and <em>n </em>

returns <em>m</em> * <em>n</em>




Note that <em>m</em> and <em>n</em> could be a negative number, 0, or a positive number. If you invoke the method with <em>m</em> = 10 and <em>n</em> = -20, the expected output is:




Recursive product: 10 times ‐20 is ‐200




(2). Write a recursive Java method named <em>findFixedSumPairs</em> that implements the following requirements:




Given an array of positive integers <em>A</em> and an integer <em>k</em>, the program prints every pair of integers in <em>A</em>, sum of which equals <em>k</em>.




Assume that all integers in <em>A</em> are distinct and they are sorted in the increasing order.




For example, suppose that you have the following main method in your program:







public static void main(String[] args) {




int[] a = {1, 5, 8, 11, 14, 15, 20, 23, 25, 28, 30, 34};

int k;

k = 43;

System.<em>out</em>.println(“k = ” + k);

<em>findFixedSumPairs</em>(a, k);

}




Then, the output of your program should be:




Fixed sum:  k = 43

a = [1, 5, 8, 11, 12, 14, 15, 20, 21, 22, 23, 25, 28, 30, 34, 36]




a[6] = 15, a[12] = 28 a[7] = 20, a[10] = 23

a[8] = 21, a[9] = 22




Note that the <em>findFixedSumPairs</em> itself is not a recursive method. You must write a separate, recursive method with additional parameters, which is invoked within the <em>findFixedSumPairs</em> method. Name this method <em>recursiveFixedSumPairs</em>. You need to determine appropriate input parameters of this method. The Section 5.4 in page 214 of the textbook discusses this issue. You may want to study this section.




An incomplete <em>RecursionPractice.java</em> code is posted on Blackboard. A <em>main</em> method is also written to test the above recursive methods. You need to complete the remaining part of <em>RecursionPractice.java</em>.




<h1>Part 2 (60 points)</h1>




You are required to write a Java program named <em>InfixEvaluation.java</em> that evaluates and produces the value of a given arithmetic expression using a stack data structure. For example, if the given expression is (2 + (5 * 3)), your program must produce 17. As another example, consider the expression ((4 – 2) * ((9 – 3) / 2)). Given this expression, your program must produce 6.




We make the following assumptions about the input expression:




<ul>

 <li>All operands are positive integers.</li>

 <li>Only the following operators are allowed: +, –, *, and /</li>

 <li>Expression is fully parenthesized. In other words, each operator has a pair of “(“ and “)” surrounding its two operands.</li>

</ul>




Your program must read a number of arithmetic expressions from an input file, named <em>infix_expressions.txt</em>, and produce an output. A sample input file is shown below:




( ( 2 + 5 ) * 3 )

( ( ( 3 + 2 ) * 3 ) – ( 6 / 2 ) )

( ( ( 7 – 5 ) * 2 ) / ( 10 – 8 ) )




Each line has one arithmetic expression. Operands, operators, and parentheses are separated by a space(s). So, you can use a space, or spaces, as a delimiter when tokenizing an expression. The expected output for the above input is:




The value of ( ( 2 + 5 ) * 3 ) is 21

The value of ( ( ( 3 + 2 ) * 3 ) – ( 6 / 2 ) ) is 12

The value of ( ( ( 7 – 5 ) * 2 ) / ( 10 – 8 ) ) is 2




Note that a given expression is repeated in the corresponding output. You must write the output on the screen.




A pseudocode is given below. You must implement this pseudocode.




Read an input expression from the input file, tokenize it, and store the tokens in a linear data structure, such as an array. Then, do the following for each expression.




Create two stacks – one for operands and the other for operators




Scan the tokens in the linear data structure from left to right and perform the following:




<ul>

 <li>If a token is an operand, push it to the operand stack.</li>

 <li>If a token is an operator, push it to the operator stack.</li>

 <li>If a token is a right parenthesis, pop two operands from the operand stack and pop an operator from the operator stack and apply it to the operands. The result is pushed back to the operand stack.</li>

 <li>If a token is a left parenthesis, ignore it.</li>

 <li>After all tokens are processed, what is left in the operand stack is the result.</li>

</ul>




Repeat the same process for all expressions in the input file.




We assume that all expressions in the input file are valid (i.e., you don’t need to check for invalid expressions).




For the two stacks, you must use the <strong><em>LinkedStack.java</em></strong> class that is included in the textbook’s source code collection. You may not use Java’s stack class or a stack class defined by somebody else. Note that you must not modify the <strong><em>LinkedStack.java</em></strong> class. Name your program as <em>InfixEvaluation.java</em>.




<h1>Documentation</h1>




No separate documentation is needed. However, you must include sufficient inline comments within your program.




<h1>Deliverables</h1>




You need to submit the following files:




<ul>

 <li><em>java</em></li>

 <li><em>java</em></li>

 <li>All other necessary files, including:</li>

</ul>

o <em>LinkedStack.java</em> o <em>Stack.java</em> o <em>SinglyLinkedList.java</em> o <em>Other files, if any</em>




Combine all files that are necessary to compile and run your program into a single archive file.  Name the archive file <em>LastName_FirstName_hw</em>2<em>.EXT</em>, where <em>EXT</em> is an appropriate file extension, such as <em>zip</em> or <em>rar</em>. Then, upload it to Blackboard.





