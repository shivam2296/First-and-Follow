# First-and-Follow
A C++ program to find the First and Follow of a given grammar
 
   Author: Shivam Prasad (prasadshivam2296@gmail.com)
   
   Date:   19th March 2018
   
   Description: This program finds the first and follow of a given grammar.
  
   Usage: First and Follow are used in the LL(1) Predictive Parser
  
  
   Input: 
   
           The first line corresponds to the number of test grammars.
           Each grammar has a number of non terminals.
           It assumes that the nonterminals are named A,B,C,D... and the productions are separated by spaces. 
           See input.txt and output.txt for more on this.
  
   Output: 
          
          Finds the first and follow of each nonterminal and saves it in an output file output.txt
          
   Sample run:
          
          Enter the number of grammars: 4

          Enter number of nonterminals: 4
          Enter the productions for NT A: 3 BDC DbC Ca
          Enter the productions for NT B: 2 da CD
          Enter the productions for NT C: 2 g ~
          Enter the productions for NT D: 2 h ~
          
          1)
          FIRST TABLE: 
	             A-> a b d g h ~ 
	             B-> d g h ~ 
	             C-> g ~ 
	             D-> h ~ 
          FOLLOW TABLE: 
	             A-> $ 
	             B-> $ g h 
	             C-> $ a g h 
	             D-> $ b g h
              
          Enter number of nonterminals: 6
          Enter the productions for NT A: 1 BCDEF
          Enter the productions for NT B: 2 a ~
          Enter the productions for NT C:2 b ~
          Enter the productions for NT D:1 c
          Enter the productions for NT E:2 d ~
          Enter the productions for NT F:2 e ~

          2)
          FIRST TABLE: 
	             A-> a b c 
             	B-> a ~ 
             	C-> b ~ 
             	D-> c 
             	E-> d ~ 
             	F-> e ~ 
           FOLLOW TABLE: 
	             A-> $ 
	             B-> b c 
	             C-> c 
	             D-> $ d e 
	             E-> $ e 
	             F-> $ 
              
          Enter number of nonterminals: 5
          Enter the productions for NT A: 1 CB
          Enter the productions for NT B: 2 +CB ~
          Enter the productions for NT C: 1 ED
          Enter the productions for NT D: 2 *ED ~
          Enter the productions for NT E: 2 i (A)
         
         3)
         FIRST TABLE: 
	            A-> ( i 
	            B-> + ~ 
	            C-> ( i 
	            D-> * ~ 
	            E-> ( i 
         FOLLOW TABLE: 
	            A-> $ ) 
	            B-> $ ) 
	            C-> $ ) + 
	            D-> $ ) + 
	            E-> $ ) * + 

          Enter number of nonterminals: 3
          Enter the productions for NT A: 2 Bb Cd
          Enter the productions for NT B: 2 aB ~ 
          Enter the productions for NT C: 2 cC ~
  
          4)
           FIRST TABLE: 
	             A-> a b c d 
	             B-> a ~ 
	             C-> c ~ 
           FOLLOW TABLE: 
	             A-> $ 
	             B-> b 
	C-> d 
