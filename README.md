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
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
<img width="1271" height="723" alt="image" src="https://github.com/user-attachments/assets/a7d65d3f-003b-4004-b9ce-b10972e76c80" />


#### Manual Calculations

<img width="1163" height="560" alt="image" src="https://github.com/user-attachments/assets/97e3abf7-87cd-4714-9609-12dde4618820" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="1054" height="831" alt="image" src="https://github.com/user-attachments/assets/612493f7-3073-4ca8-99ef-6a914fa23773" />

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

<img width="1127" height="774" alt="image" src="https://github.com/user-attachments/assets/631a70f9-28b2-4096-95cf-af9be50f4750" />


#### Manual Calculations

<img width="1163" height="560" alt="image" src="https://github.com/user-attachments/assets/d617e4ec-4db7-4c77-a7da-96dbde3dbc47" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="958" height="666" alt="image" src="https://github.com/user-attachments/assets/56e71c89-a8f1-4aa0-be36-d2a25223cd75" />

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

<img width="1189" height="844" alt="image" src="https://github.com/user-attachments/assets/032d4875-2f76-482c-8d1a-44b70daad009" />

#### Manual Calculations

<img width="1600" height="712" alt="image" src="https://github.com/user-attachments/assets/2fea066f-bb70-4d60-ae18-2f305fd5e14d" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1600" height="810" alt="image" src="https://github.com/user-attachments/assets/d99561dc-31e6-404a-98d5-49c445bb75da" />

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

<img width="1115" height="805" alt="image" src="https://github.com/user-attachments/assets/9a6ef66d-fcc5-42fa-bb94-7d35f47e7d57" />


#### Manual Calculations

<img width="742" height="508" alt="image" src="https://github.com/user-attachments/assets/540c5fac-942c-40c2-9216-6e61f177b2db" />

---
## OUTPUT FROM MASM SOFTWARE

<img width="1038" height="786" alt="image" src="https://github.com/user-attachments/assets/3242eff3-0b3f-412f-8567-7702781d9c1e" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

