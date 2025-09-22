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
<img width="707" height="820" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


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
|     2000 = 34           |       2004 = 68          |
|     2001 = 12           |       2005 = 24          |
|     2002 = 34           |
|     2003 = 12           |


#### Manual Calculations

![WhatsApp Image 2025-09-22 at 08 47 23_752deccf](https://github.com/user-attachments/assets/20a8af02-c897-463d-80be-45702d39d48a)

---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="690" height="449" alt="image" src="https://github.com/user-attachments/assets/00995b89-875e-411e-a93d-4171d0637d9e" />


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
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
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
|     2000 = 69           |       2004 = C5          |
|     2001 = 24           |       2005 = 0D          |
|     2002 = A4           |
|     2003 = 16           |

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 08 47 24_c2f70f83](https://github.com/user-attachments/assets/32bd0c0e-ad0c-428d-ae33-538b4b48a6b3)


---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="683" height="472" alt="image" src="https://github.com/user-attachments/assets/376d0bfb-64e2-4856-aeb5-f2efd313aa30" />


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
|     2000 = 34           |       2004 = 90          |
|     2001 = 12           |       2005 = 5A          |
|     2002 = 12           |       2006 = 4B          |
|     2003 = 34           |       2007 = 01          |

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 08 47 24_29b4e7a7](https://github.com/user-attachments/assets/f9d62b64-5017-4d2d-a2a1-e3ff5f1f3864)


---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="739" height="464" alt="image" src="https://github.com/user-attachments/assets/5c399780-a54d-4757-b251-940955d9dc6f" />


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
|     2000 = 36           |       2004 = 01          |
|     2001 = 12           |       2005 = 00          |
|     2002 = 36           |       2006 = 02          |
|     2003 = 12           |

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 08 47 25_48bb4189](https://github.com/user-attachments/assets/35691812-172f-4260-bcc5-5b83cc67eb46)

---
## OUTPUT FROM MASM SOFTWARE

<img width="754" height="493" alt="image" src="https://github.com/user-attachments/assets/ff666829-5c7e-44bd-a2d5-c0d8b0392b23" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

