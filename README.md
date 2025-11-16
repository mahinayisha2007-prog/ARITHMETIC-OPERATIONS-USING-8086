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
|     2000:34	           |           2000:55        |
|     2001:12             |           2005:55        |
|     2002:21	           |           2006:00        |
|     2003:43	           |                          |

#### Manual Calculations

![WhatsApp Image 2025-11-16 at 12 42 05_d111362e](https://github.com/user-attachments/assets/23bd6155-e28e-4856-b5da-df927195cfda)

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="662" height="433" alt="511747842-95d543b1-96bd-4ea1-ba8d-ce1c2916e440" src="https://github.com/user-attachments/assets/c461d24d-8ed1-4cde-b707-750362f80e4d" />

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
|       2000:45	        |       2000:04            |
|       2001:A4	        |       2005:72            |
|       2002:41	        |       2006:00            |
|       2003:32	        |                          |

#### Manual Calculations

![WhatsApp Image 2025-11-16 at 12 43 24_0b045a35](https://github.com/user-attachments/assets/5f39ab8a-38de-49de-9777-2c2e22349d72)


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="635" height="426" alt="511748078-611cbcfc-d7b7-4e9b-88a7-4b0452ce6c41" src="https://github.com/user-attachments/assets/48ad58d3-7810-4788-aa49-c9609e1fa41d" />

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
|      2000:22	        |        2000:A8           |
|      2001:21            |	     2005:CC           |
|      2002:14	        |        2006:57           |
|      2003:21	        |        2007:02           |

#### Manual Calculations

![WhatsApp Image 2025-11-16 at 12 43 23_bf4b7362](https://github.com/user-attachments/assets/20d23874-6bd2-42c1-aa80-7cbda884a1c6)


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="627" height="444" alt="511748205-7d043222-f2f6-4717-aa83-ed01eeffc8a5" src="https://github.com/user-attachments/assets/dbdbc7a5-f381-428f-ab3a-1c041e474ff2" />

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
|       2000:33	        |        2000:03           |
|       2001:33           |        2005:00           | 
|       2002:11	        |        2006:00           |
|       2003:11	        |        2007:00           |


#### Manual Calculations

![WhatsApp Image 2025-11-16 at 12 43 23_a54aa3e5](https://github.com/user-attachments/assets/38308f31-213e-4325-ad3b-9a282345ebb1)

## OUTPUT FROM MASM SOFTWARE

<img width="645" height="430" alt="511748660-22976632-35c1-4271-894f-d7114d029635" src="https://github.com/user-attachments/assets/785a8acc-1514-420b-b070-d4cfa365b7e6" />

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

