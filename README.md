# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
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
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     1200 : 12           |      1204 : 24           |
1201 : 34  |  1205 : 68
1202 : 12   | 1206 : 00
1203 : 34    |1207 : C4

#### Manual Calculations
![1](https://github.com/user-attachments/assets/36510d27-3d47-4de8-99b6-772153cb95e5)



## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/1a13b188-3a2b-42ff-a328-c7bde3e6844a" />

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|               1200 : 12          |      1204 : 00                    |
1201 : 34 | 1205 : 00
1202 : 12 | 1206 : 00
1203 : 34 | 1207 : C4
#### Manual Calculations

![2](https://github.com/user-attachments/assets/58b85873-2ebf-47e9-873c-080650d3f259)



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (11)" src="https://github.com/user-attachments/assets/d288ce37-5fd6-42a1-ae7e-ef62b2624741" />

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
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
```

#### Output Table
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200 : 12                |       1204 : 44                   |
1201 : 34 | 1205 : 51
1202 : 12 | 1206 : 97
1203 : 34 | 1207 : 0A
#### Manual Calculations

![3](https://github.com/user-attachments/assets/d0541466-35ce-4979-be6a-67fa415ddeda)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (14)" src="https://github.com/user-attachments/assets/f7b1282f-8f22-4986-9554-c0c7ff03a565" />

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
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
```

#### Output Table
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200 : 12                  |              1204 : 01            |
1201 : 34 | 1205 : 00
1202 : 12 | 1206 : 00
1203 : 34 | 1207 : 00
#### Manual Calculations

![4](https://github.com/user-attachments/assets/3aea83ad-287d-4dbf-b8f0-fd53e1d22df6)

## OUTPUT FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (16)" src="https://github.com/user-attachments/assets/cec1376a-2e9f-46c7-8ddc-45450e88c53b" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
