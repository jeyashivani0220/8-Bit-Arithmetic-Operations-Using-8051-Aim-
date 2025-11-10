# 8-Bit-Arithmetic-Operations-Using-8051

## Aim:
To perform 8-bit arithmetic operations such as addition, subtraction, multiplication, and division using the 8051 microcontroller.

## Apparatus Required:

•	Laptop with Keil uVision software

## Algorithm:![mpmc exp5a-1](https://github.com/user-attachments/assets/79ecc70a-0489-491e-a2e1-ec92a6b4d5fd)


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
MOV A, #00H    
MOV A, 00H     
; Load first number from memory
 ; Add second number
 ; Store result in memory
 ; Clear A (use # for immediate data)
 ; <-- invalid (removing this)
 MOV 41H, #00H  ; Initialize carry storage as 0
 JNC SKIP_CARRY ; Jump if no carry
 MOV 41H, #01H  ; Store carry as 1 if CY = 1
 SKIP_CARRY: NOP
 END;
```


## Output:
![mpmc exp5a-2](https://github.com/user-attachments/assets/f81225e9-f6f5-4d2d-b7f9-cc5eede19947)
![mpmc exp5a-3](https://github.com/user-attachments/assets/cf0c1aa9-dbd0-4791-b018-abfca4abedd4)

   
## For Subtraction:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Subtract B from A.
4.	Store the result in memory location 40H.

## Program:
```
 ORG 0000H;
 MOV A, 30H;
 SUBB A,31H;
 MOV 40H,A;
 JNC NEXT;
 MOV 41H,#01H;
 SJMP END_PROGRAM;
 NEXT:MOV 41H,#00H;
 END_PROGRAM:NOP
END;
```


## Output:
![mpmc exp5b-1](https://github.com/user-attachments/assets/7bc91273-98a0-4750-8d49-69ddf645571d)
![mpmc exp5b-2](https://github.com/user-attachments/assets/7289125e-d6fb-43a7-bc4e-beac7b482286)


## For Multiplication:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Multiply A and B.
4.	Store the lower byte of the result in memory location 40H.
5.	Store the higher byte of the result in memory location 41H.

## Program:
```
 MOV A,30H;
 MOV B, 31H;
 MUL AB;
 MOV 40H,A;
MOV 41H,B;
 END;
```


## Output:
![mpmc exp5c-1](https://github.com/user-attachments/assets/0ac614f9-c7c4-4503-9349-70ef2ae546b3)
![mpmc exp5c-2](https://github.com/user-attachments/assets/dcda2f7e-dbe1-4381-a44c-50aa1c995e1e)


## For Division:
1.	Load the dividend from memory location 30H into register A.
2.	Load the divisor from memory location 31H into register B.
3.	Divide A by B.
4.	Store the quotient in memory location 40H.
5.	Store the remainder in memory location 41H.


## Program:
```
 ORG 0000H;
 MOV A,30H;
 MOV B,31H;
 DIV AB;
 MOV 40H,A;
 MOV 41H,B;
 END;
```



## Output:

![mpmc exp5d-1](https://github.com/user-attachments/assets/355a20bc-bc81-424b-8164-634c0a3e72c7)
![mpmc exp5d-2](https://github.com/user-attachments/assets/678c552f-9928-482d-85b9-337769a88307)


## Result:
The 8-bit arithmetic operations using the 8051 microcontroller have been successfully executed and verified using Keil software.

