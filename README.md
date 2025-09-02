Arithmetic-operation-using-8086
8086 Assembly Language Programs for Arithmetic Operations
AIM
To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

APPARATUS REQUIRED
Personal Computer with MASM Software
1. ADDITION
Algorithm
Initialize memory location in HL register.
Store 1st data.
Increment HL to enter 2nd data.
Move 2nd number to accumulator.
Decrement HL.
Add value in memory with accumulator.
Store result.
Stop.
FLOW CHART
image
Program
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
Output Table
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
WhatsApp Image 2025-09-01 at 23 28 25_1cb910c3	WhatsApp Image 2025-09-01 at 23 28 25_b811ca90
Manual Calculations
WhatsApp Image 2025-09-01 at 22 35 15_70a9b978

OUTPUT IMAGE FROM MASM SOFTWARE
2. SUBTRACTION
Algorithm
Initialize memory and store 1st data.
Increment to get 2nd data.
Move 2nd data to accumulator.
Subtract memory content.
Store result.
FLOWCHART
image
Program
Output Table
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
WhatsApp Image 2025-09-01 at 23 19 14_da5e48fa	WhatsApp Image 2025-09-01 at 23 19 15_127aacd9
Manual Calculations
WhatsApp Image 2025-09-01 at 22 35 16_361f713d

OUTPUT SCREEN FROM MASM SOFTWARE
3. MULTIPLICATION
Algorithm
Initialize memory and store operands.
Move operands to registers.
Multiply.
Store result.
##FLOWCHART

image
Program
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
Output Table
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
WhatsApp Image 2025-09-01 at 23 28 11_2349f85b	WhatsApp Image 2025-09-01 at 23 28 11_2752ddff
Manual Calculations
WhatsApp Image 2025-09-01 at 22 35 16_117c9fb4

OUTPUT SCREEN FROM MASM SOFTWARE
4. DIVISION
Algorithm
Load memory location of operands.

Perform division.

Store result.

FLOWCHART
image
Program
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
Output Table
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
WhatsApp Image 2025-09-01 at 23 21 10_1662fa82	WhatsApp Image 2025-09-01 at 23 21 11_37a19459
Manual Calculations
WhatsApp Image 2025-09-01 at 22 35 15_99659ffa

OUTPUT FROM MASM SOFTWARE
RESULT
Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
