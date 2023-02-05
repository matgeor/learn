---
layout: page
title: Instructions
description: >-
    Follow these carefully, to start with Octave.
---

# Instructions
{:.no_toc}

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Starting 

1. Access / open terminal
	1. press `Ctl` + `Alt` + `T`  

2. Invoke octave
	1. input `octave` in the terminal opened above.
	
	We we will get Octave CLI (command line interface). We can enter all our commands via the CLI we just opened. One can start going ahead with the commands given below. 
		
3. Commands

	1. `a = 1`
	2. `b = 3`
	3. `a*b`
	5. `a/b`
	6. `a+b`
	7. `a-b`

4. Accessing previous commands
	1. Press up and arrow and see what happens.
	

5. Check a and A ?
	1. Issue `a` . The value of `a` is shown. Try inputing `A`.

6. Named variables
	1. Obvious from above activities.
	2. Issue `a = 2`. Check `whos`.
	3. Numerics or strings possible, for the same variable.

8. Built in functions :

	1. `cos` Cosine of an angle (in radians)
	2. `sin` Sine of an angle (in radians)
	3. `tan` Tangent of an angle (in radians)
	4. `exp` Exponential function 
	5. `log` Natural logarithm (ln x)
	6. `atan` Inverse tangent
	7. `sqrt` Square root
	8. `abs` Absolute value

	example : Try `exp(1)` and `abs(3+4i)`.

9. Numbers, Vectors and Matrices

	1. Octave is designed to manipulate matrices (m x n). 
	2. Single row or column matrices are known as vectors (m x 1 or n x 1). 
	3. Numbers are 1 x 1 matrices.
	4. A list of numbers separated by spaces or commas, inside square brackets, defines a row vector.
	5. Numbers separated by semicolons (or carriage returns), define a column vector.
	4. examples:
 		1. `A = [1 2 3]`
 		2. `A = [1 2 3; 4 5 6]`
 		3. `A'`
 		4. `A*A'`
 		5. `X = [1:10]` ?
 		6. `X = [1:2:10]`
10. Vector creation

	1. `zeros(M,N)` Create an M by N matrix where every element is zero.
	2. `ones(M,N)` Create an M by N matrix where every element is one.
	3. `eye(M)` Create the M by M identity matrix.
	4. `rand(M)` Create an M by M matrix with random elements.
	5. `diag(X)` Create a diagonal matrix with vector X on the main diagonal.
	6. `linspace(x1,x2,N)` Create a row vector of N elements, evenly spaced between x1 and x2.

11. Matrix operations
	1. Make a 2x2 matrix (say `h`)
	2. Try, `h+h`, `2h - h`, `h*h` etc.

12. Componentwise operations
	1. `a=[1,2,3]`
	2. `b=[3,4,5]`
	3. `a*b` (did it work? Why not?)
	4. `a.*b`
	5. `b = b'`
	6. `a*b`
	7. `a.*b` (Can you explain the output?)
	

13. Saving and loading workspace
	1. issue `whos`
	2. issue `save ws` (ws is the name given to save the workspace parameters.)
	3. issue `exit` (You will get out of Octave environment.)
	4. issue `octave`
	5. issue `whos` (There will be no variables listed)
	6. issue `load ws` (We whould have the workspace we saved earlier, restored now.)
	7. issue `whos` (Confirmatory test).

14. Multiply selected elements of a 10 element matrix, usage of *for* loop.
	
	Issue the following in order:
	1. `A =[1:20]` (creation of a row vector)
	2. `for i = 15:20` (*for* loop begins. choosing i values for which the particular action needs to executed)
	3. `A(i)=2*A(i)`  (defining the action)
	4. `end` (*for* loop ends)
	
	The output is expected to be self explanatory. Any doubts, feel free to ask.

15. Suppression of output
	1. Issue, `A =[1:20]`
	2. Issue `A =[1:20];` (note the semicolon)
	3. The semicolon suppresses the output.
	
	
	
## Plotting
	
16. Basic steps.

	In order to make a 2D plot, we need two row (or column) vectors. These are defined in steps 1 and 2 below. 

	1. `x = [1,2,3,4,5,6,7,8,9]`
	2. `y = [1,2,3,4,5,6,7,8,9]`
	3. `plot(x,y)` (we will get a line inclined at 45 degrees wrt both axis)
	4. `plot(x,y,'r-x')` (red line and red x marks)
	5. `plot(x,y,'r-o')` (red line and red o marks)
	6. `plot(x,y,'b-o')` (blue line and blue o marks)
	7. `plot(x,y,'bo')` (scattered blue o marks)
	8. `plot(x,y,'rx')` (scattered red x marks)
	9.  Repeat : step 7 and then, `hold on` and then step 8 (both plots will appear together)
	10. `hold off` removes previous `hold on` .
	
17. More on plots

	1. Repeat : step 7 and then, `hold on` and then step 8 
	2. `xlabel('abc')` (*abc* is an arbitrary label. Can be any string)
	3. `ylabel('def')`
	4. `title('tt')`
	5. `legend('tt', 'rr')`
	
	
## Octave Scripts

1. Scripting: preparation and usage of .m files

	We can speed up calculations which are repeated by scripting. The steps to make a script are described below:
	
	1. Open a blank text file. One may use any text editor. My favourite is Gedit.
	2. Type in the steps as we would do in Octave CLI.
	3. Save the file (in the same directory in which you are working) , as *test-script.m* . The .m part is very important.
	4. Issue the command `test-script` (without the *.m*). All the steps will be executed in order.

2. Practice

	1. 	Make an Octave script file, which plots *sin(x)* and *sin(2x)* on the same plot, for arbitrary values of *x*.


## The Simple Pendulum

This is an experiment which is done, routinely by XII science students. The goal is to measure *g* at the location, by measuring time periods of pendula with varying lengths. The experimental data gathered by a students is given below. 

1. Make a *l-T* and *l-T^2* graph as well as estimate *g* using the data provided.

2. *g* may be found using the formula 
```math g=(4pi^2)l/T^2```	

	|l (cm)|T (s)|
	|------|-----|
	| 5    | 4.4 |
	| 10   | 6.4 |
	| 15   | 7.7 |
	| 20   | 9.0 |
	| 25   | 10.0|
	| 30   | 11.0|
	| 35   | 11.7|
	| 40   | 12.6|
	| 45   | 13.6|
	| 50   | 14.2|	

 
	
## References : 

The above material is made with the aid of the following references.
	
1. [Prof. Yaniv Plan's](https://www.yanivplan.com/) notes, which are based on [P G Long's book](http://www-mdp.eng.cam.ac.uk/web/CD/engapps/octave/octavetut.pdf) .
2. [Octave](https://octave.org/) website. 
