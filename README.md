# pattern-matrix
n=int(input("enter the size:"))
matrix=[[0]*n for _ in range(n)]
top,left=0,0
right,bottom=n-1,n-1
num=1
while top<=bottom and left<=right:
    for i in range(left,right+1):
        matrix[top][i]=num
        num+=1
    top+=1
    for i in range(top,bottom+1):
        matrix[i][right]=num
        num+=1
    right-=1
    for i in range(right,left-1,-1):
        matrix[bottom][i]=num
        num+=1
    bottom-=1
    for i in range(bottom,top-1,-1):
        matrix[i][left]=num
        num+=1
    left+=1
for row in matrix:
    for val in row:
        print(f"{val:3}",end=' ')
    print()
OUTPUT:
enter the size: 9
  1   2   3   4   5   6   7   8   9 
 32  33  34  35  36  37  38  39  10 
 31  56  57  58  59  60  61  40  11 
 30  55  72  73  74  75  62  41  12 
 29  54  71  80  81  76  63  42  13 
 28  53  70  79  78  77  64  43  14 
 27  52  69  68  67  66  65  44  15 
 26  51  50  49  48  47  46  45  16 
 25  24  23  22  21  20  19  18  17 
 OUTPUT2:
 enter the size: 4
  1   2   3   4 
 12  13  14   5 
 11  16  15   6 
 10   9   8   7 
 OUTPUT:3
 enter the size: 5
  1   2   3   4   5 
 16  17  18  19   6 
 15  24  25  20   7 
 14  23  22  21   8 
 13  12  11  10   9 
TRAVERSAL:
matrix=[[1,2,3,4],[5,6,7,8],[9,10,11,12],[13,14,15,16]]
row=len(matrix)
cols=len(matrix[0])
top,left=0,0
right,bottom=cols-1,row-1
while top<=bottom and left<=right:
    for i in range(left,right+1):
        print(matrix[top][i],end=' ')
    top+=1
    for i in range(top,bottom+1):
        print(matrix[i][right],end=' ')
    right-=1
    for i in range(right,left-1,-1):
        print(matrix[bottom][i],end=' ')
    bottom-=1
    for i in range(bottom,top-1,-1):
        print(matrix[i][left],end=' ')
    left+=1
OUTPUT:
1 2 3 4 8 12 16 15 14 13 9 5 6 7 11 10 

CHARECTER MATRIX:
n=int(input("enter the size:"))
matrix=[[' ']*n for _ in range(n)]
top,left=0,0
right,bottom=n-1,n-1
num=0
while top<=bottom and left<=right:
    for i in range(left,right+1):
        matrix[top][i]=chr(65 + num % 26)
        num+=1
    top+=1
    for i in range(top,bottom+1):
        matrix[i][right]=chr(65 + num % 26)
        num+=1
    right-=1
    for i in range(right,left-1,-1):
        matrix[bottom][i]=chr(65 + num % 26)
        num+=1
    bottom-=1
    for i in range(bottom,top-1,-1):
        matrix[i][left]=chr(65 + num % 26)
        num+=1
    left+=1
for row in matrix:
    for val in row:
        print(f"{val:3}",end=' ')
    print()
OUTPUT:
enter the size: 5
A   B   C   D   E   
P   Q   R   S   F   
O   X   Y   T   G   
N   W   V   U   H   
M   L   K   J   I   
