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
|   1200:12               |   1204: 24               |
|   1201:34               |   1205: 68               |
|   1202:12               |   1206: 00               |
|   1203:34               |   1207: C4               |
#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-08-24 at 15 23 28_92d4fbd3](https://github.com/user-attachments/assets/0b2debe6-a7c1-40fc-93b8-375129c70307)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="425" alt="Screenshot 2025-08-20 205032" src="https://github.com/user-attachments/assets/934b067c-763e-4bc8-b9d2-a3c2e435a4b2" />

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
|  1200:12                |   1204:00                |
|  1201:34                |   1205:00                |
|  1202:12                |   1205:83                |
|  1203:34                |   1206:C4                |
#### Manual Calculations

(Add your calculation here)

![WhatsApp Image 2025-08-24 at 15 32 57_bcac144c](https://github.com/user-attachments/assets/5342826f-b0fd-414a-badc-7d219396dafd)



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="654" height="426" alt="Screenshot 2025-08-23 205239" src="https://github.com/user-attachments/assets/15eceb53-c7e2-400d-b116-f9ceb5f42dc3" />

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
|  1200:12                |   1204:44                |
|  1201:34                |   1205:51                |
|  1202:12                |   1205:97                |
|  1203:34                |   1206:0A                |
#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-08-24 at 15 37 58_52762ac3](https://github.com/user-attachments/assets/13a12b3a-47bf-41eb-a359-6f59e2f9de20)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="642" height="421" alt="Screenshot 2025-08-20 160315" src="https://github.com/user-attachments/assets/dd150db0-5ddf-4253-bcfa-754a1ec537ad" />

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
|  1200:12                |   1204:01                |
|  1201:34                |   1205:00                |
|  1202:12                |   1205:00               |
|  1203:34                |   1206:00                |

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-08-24 at 15 45 42_8cbb01ac](https://github.com/user-attachments/assets/b60f5758-124d-410e-a486-15e89c7d40ea)

---
## OUTPUT FROM MASM SOFTWARE
<img width="641" height="425" alt="image" src="https://github.com/user-attachments/assets/2e9411e7-81e3-4bb9-9f63-7047c5d4b26d" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
