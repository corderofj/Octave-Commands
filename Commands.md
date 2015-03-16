# Octave Tutorial
##Key Commands

###Basic Operations:
Help command – prints help on any ‘command’  
Exit – closes Octave
Addpath(‘C:\xxxx’) adds that to the searchpath of Octave


###Comparisons and Evaluations:
==  (EQUALS TO):  Example 1==2 would return a 0 (false)  
~= (NOT EQUALS TO): 1~=2 would return a 1 (true)   
&& (AND):  1&&0 returns a 0 (false – True AND False is false)  
|| (OR): 1||0 returns a 1

###Variables, Matrices and vectors
A = 3 : creates a variable A and assigns value of 3   
A=’text’  
Format long: prints long format in numerical variables  
Format short; prints long format in numerical variables  
A = [1  2; 3  4; 5  6] : Creates a 3X2 Matrix, the ";" tells when to go to the next line  
      |1  2|    
   	  |3  4|    
	    |5  6|    
V = [ 1  2  3] : Creates a 1X3 vector  
V = [1;2;3]: Creates a 3X1 vector (3 rows, 1 column)  
V = 10 : 1 : 20    - This creates a Vector that starts at 10, then increases by 1(second parameter) until it reaches 20(third parameter)  
Ones(2,3)   - Creates a 2X3 matrix with all values = 1  
Zeroes(2,3) - Creates a 2X3 matrix with all values = 0  
Rand(3,3) - Creates a 2X3 matrix with randomly generated numbers between 0 and 1  
Eye(4) – creates a 4X4 identity Matrix  
Magic(5) – Creates a 5X5 magic matrix (all rows and columns and diagonals add up to the same number)  

###Working with Data
Size(A) = returns size of the Matrix A  
Size(A,1) = returns the number of ROWS in matrix A)  
Size(A,2) = returns the number of COLUMNS in matrix A)  
Length(v) = returns the size of the LONGEST dimension of a matrix or vector (use normally in vectors)  

Pwd – returns the current path  
Cd ‘new path’ – changes the current directory to the new path  
Ls – lists all files and directories in the current path  
Load file.dat – loads the file.dat to Octave memory  
Who – shows the variables currently in memory  
Whos – returns the variables with details about them (type of variable, size, bytes)  
Clear – removes all variables  from memory  
Clear variable – removes only that variable from memory  
Save filename.dat Variable  - saves the Variable as a file named filename.dat in a binary format  
Save filename.txt Variable – ascii – saves the Variable as an ASCII text format to disc with the name filename.txt  

###Getting or Assigning Values from Matrices or Vectors
A(3,2) – Returns the content in the 3rd Row and 2nd Column of Matrix A  
A(:, 2) – Rerturns ALL of the Rows (that’s what : means) on the 2nd column  
A([1  3], :) – Returns all of the values in the 1st AND 3rd rows  
A(:,2) = [10;11;12] – Assigns the values 10,11,12 to the 2nd column of Matrix A  
A = [A, [100, 101, 102]] – Will Append one more column at the end of A  
A(:) – Put all of the elements of A into a single vector  
C = [A  B]  - Will concatenate Matrix A and Matrix B together and call it C (A will be on the left followed by B]  
C = [A;B] – Same thing but will put A on top and B on the bottom  

###COMPUTING ON DATA
A*C  - Multiplies Matrix A times Matrix C  
A  .* B  - Multiplies EACH ELEMENT of A (that’s what the “.” Means) times the corresponding element of B  
-	The “.” Can be used before any arithmetic sign (/, +, -, ^)  
Abs(x) – Returns absolute value of x   
A’  - Returns the TRANSPONSE of A  
Max(A) – returns the maximum value of matrix A – just one value of the maximum  
Max (A,[],1) – Takes the COLUMN WISE maximum – will return as many values as columns in the matrix  
Max(A,[],2) – Takes the ROW WISE maximum – will return as many values as rows… first the max of the first row, then the max of the second row, etc  c
[val, ind] = max(A) returns the max value of A in val and its index in the matrix in ind  
Find (A>=7) – returns the index (row,column) on the elements of matrix A that are greater or equal to 7  

Sum(A) – sums all elements of a  
Sum(A,1) – Sums each COLUMN of A and return as many values as Columns  
Sum(A,2) – Sums each ROW of A  

Prod(a) – multiplies all elements of a  
Floor(a) – rounds down all elements of a  
Ceil(a) – rounds up  
Pinv(A) - returns the invert matrix of A  

###PLOTTING DATA
Plot(x,y) – does a plot of variables x and y  
Hold on – will hold any current plot and add new plots on top instead of replacing them  
Xlabel(‘label of x’) – Adds label to the x dimension (same for Y)  
Legend(‘legendA’, ‘legendB’) – Adds 2 legends to the active plot  
Title(‘MyTitle)  
Print –dpng myplot.png will save the current plot as a png file called myplot.png (type help to see which other formats are available)  
Close – eliminates the current plot window  
Figure(1); plot(x,y) – creates one windown with a plot, if you do a figure(2); plot(x,y) creates a second separate window for that other plot  
Subplot(1,2,1) – divides de plot window into a 1x2 grid and access the first element (subplot(1,2,2) accesses the second element)  
Axis([x1  x2  y1  y2]) changes the axis values for the current plot to go from x1 to x2 and from y1 to y2  
Imagesc(A) – visualizes a Matrix with color blocks  
Colorbar/Colormap  adds legends to previous command  

###CONTROL STATEMENTS
FOR  
    For I = 1:10,  
         Instructions…   
   End;  

WHILE
  I=1;   
     While I <= 5,  
     V(I) = 100;  
     I = i+1  
End;  

IF  
I=1  
While True,  
   V(i) =9000;  
   I=i+1;  
   If i==6,  
       Break;  
   End;  
End;  

V(1) = 2;  
If v(1)==1,  
    disp(‘The value is one’);  
elseif v(1) == 2,  
   disp(‘The value is two’);  
else  
  disp(‘The value is not 1 nor 2.’);  
end;  

###FUNCTIONS
Recomentadion – use wordpad instead of notepad  

Create a file with the name of the function and “.m” (ie function.m)  

Function y = squarethisnumber(x) 
   Y = x^2   

the above function take the parameter x and returns the value y  

Can also define functions to return multiple numbers:  

Function [y1, y2] = squareANDcubethis number(x)  
   Y1 = x^2  
   Y2 = x^3  






