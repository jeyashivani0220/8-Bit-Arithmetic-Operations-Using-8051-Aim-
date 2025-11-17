# 8-Bit-Arithmetic-Operations-Using-8051

## Aim:
To perform 8-bit arithmetic operations such as addition, subtraction, multiplication, and division using the 8051 microcontroller.

## Apparatus Required:

•	Laptop with Keil uVision software

## Algorithm:

## For Addition:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Add the contents of registers A and B.
4.	Store the result in memory location 40H.
5.	Store the carry (if any) in 41H.

## Program:
```
ORG 0000H
MOV A, 30H     
ADD A, 31H    
MOV 40H, A 
JNC NEXT 
MOV 41H, #01H
SJMP END_PROGRAM
NEXT: MOV 41H, #00H
END_PROGRAM: NOP
END
```

## Output:
<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/21bd48e1-38fc-4fa5-bba8-b0fff7e33055" />
<img width="1919" height="1139" alt="image" src="https://github.com/user-attachments/assets/d622d80a-fe0b-4292-8f8c-cf06123d0a6a" />

   
## For Subtraction:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Subtract B from A.
4.	Store the result in memory location 40H.

## Program:
```
ORG 0000H
MOV A, 30H
SUBB A, 31H
MOV 40H, A
JNC NEXT
MOV 41H, #01H
SJMP END_PROGRAM
NEXT: MOV 41H, #00H
END_PROGRAM: NOP
END
```

## Output:
<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/bcf68f1b-5c78-4ddf-bfb8-a2de0a3a0cc9" />
<img width="1919" height="1139" alt="image" src="https://github.com/user-attachments/assets/91b3f022-16ae-4f61-be52-6a5edb94d1f2" />

## For Multiplication:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Multiply A and B.
4.	Store the lower byte of the result in memory location 40H.
5.	Store the higher byte of the result in memory location 41H.

## Program:
```
ORG 0000H
MOV A, 30H 
MOV B, 31H
MUL AB
MOV 40H, A 
MOV 41H, B
END
```

## Output:
<img width="1918" height="1137" alt="image" src="https://github.com/user-attachments/assets/399c4ab6-c58c-41ca-a293-d010b2e46d9e" />
<img width="1919" height="1137" alt="image" src="https://github.com/user-attachments/assets/79e572cb-7e8f-4180-84af-7fd950c09ac2" />


## For Division:
1.	Load the dividend from memory location 30H into register A.
2.	Load the divisor from memory location 31H into register B.
3.	Divide A by B.
4.	Store the quotient in memory location 40H.
5.	Store the remainder in memory location 41H.


## Program:
```
ORG 0000H
MOV A, 30H
MOV B, 31H
DIV AB
MOV 40H, A
MOV 41H, B 
END
```

## Output:
<img width="1918" height="1135" alt="image" src="https://github.com/user-attachments/assets/25c5eb00-1681-48b9-b245-547c304078b8" />
<img width="1915" height="1135" alt="image" src="https://github.com/user-attachments/assets/45cab786-1956-418a-9309-c3464fc44812" />


## Result:
The 8-bit arithmetic operations using the 8051 microcontroller have been successfully executed and verified using Keil software.

