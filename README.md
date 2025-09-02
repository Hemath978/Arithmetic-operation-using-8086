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
|           ![WhatsApp Image 2025-09-01 at 23 28 25_1cb910c3](https://github.com/user-attachments/assets/40ea9aad-b172-4f5f-b62d-b5ffc5985c8b)|            ![WhatsApp Image 2025-09-01 at 23 28 25_b811ca90](https://github.com/user-attachments/assets/83b6d161-1a61-45e0-89c1-f5d2fbc6e440)|

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 22 35 15_70a9b978](https://github.com/user-attachments/assets/277652bf-f648-4af6-91db-095e5d7475f9)

---

## OUTPUT IMAGE FROM MASM SOFTWARE

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
|            ![WhatsApp Image 2025-09-01 at 23 19 14_da5e48fa](https://github.com/user-attachments/assets/79244b30-6c5e-4aa7-a0d8-05b6f48ebd41)|           ![WhatsApp Image 2025-09-01 at 23 19 15_127aacd9](https://github.com/user-attachments/assets/1939fe81-6248-4773-aad8-2cbe76279183)|

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 22 35 16_361f713d](https://github.com/user-attachments/assets/975d9528-2646-462f-9687-76ea0558823f)

---


## OUTPUT SCREEN FROM MASM SOFTWARE

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
|            ![WhatsApp Image 2025-09-01 at 23 28 11_2349f85b](https://github.com/user-attachments/assets/84e75e45-2e14-47a6-80b1-76d14cbdc902)|           ![WhatsApp Image 2025-09-01 at 23 28 11_2752ddff](https://github.com/user-attachments/assets/8edbf192-ed5e-4af7-af5d-85c5e3d50f31)|

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 22 35 16_117c9fb4](https://github.com/user-attachments/assets/9919768c-1c0f-4546-afdb-36d87c88b87f)

---

## OUTPUT SCREEN FROM MASM SOFTWARE

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
|      ![WhatsApp Image 2025-09-01 at 23 21 10_1662fa82](https://github.com/user-attachments/assets/e345ee17-1857-4406-bfd6-89af3a4366fd)| ![WhatsApp Image 2025-09-01 at 23 21 11_37a19459](https://github.com/user-attachments/assets/313c49b3-6079-4ad1-8cdc-b2ef082f092b)|

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 22 35 15_99659ffa](https://github.com/user-attachments/assets/3ab1c66f-3bac-45a6-9ce4-56d3a06619fd)

---
## OUTPUT FROM MASM SOFTWARE
## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
