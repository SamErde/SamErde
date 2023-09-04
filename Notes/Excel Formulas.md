# Count the number of "." within a cell by getting the lenght of the cell with all "." removed and subtracting that number from the original lenth of the cell:  
`=LEN(A1)-LEN(SUBSTITUTE(A1,".",""))`

# Position of the 2nd "." within a cell:  
`=FIND("~",SUBSTITUTE(A1,".","~",2),1)`

# Position of the 3rd "." within a cell:  
`=FIND("~",SUBSTITUTE(A1,".","~",3),1)`

# Final formula to get the last two octets of the IP address:  
```=IF(LEN(A1)-LEN(SUBSTITUTE(A1,".",""))>1,MID(A1,(FIND("~",SUBSTITUTE(A1,".","~",(LEN(A1)-LEN(SUBSTITUTE(A1,".",""))-1)))+1),LEN(A1)),A1)```