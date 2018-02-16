# Registers

#### General Purpose 

 Register       | Description   | 
| ------------- |:-------------:| 
| EAX    | Accumulator Register - Used for Arithmatic operations | 
| EBX      | Base Register  - No specific use   | 
| ECX  | Counter Register   - Often used as function parameter or loop counter  |
| EDX      | Data Register  - Used as function parameter or for storing local variable values  | 
| ESI  | Source Index - Often used as a pointer  |
| EDI      | Destination Index      | 
| EBP  | Base Pointer   - Frame pointer   |
| ESP      | Stack Pointer      | 

#### Segment Registers

| Register | Description |
| --- | --- |
| SS | Stack Segment, Pointer to the stack |
| CS | Code Segment, Pointer to the code |
| DS | Data Segment, Pointer to the data |
| ES | Extra Segment, Pointer to extra data |
| FS | F Segment, Pointer to more extra data |
| GS | G Segment, Pointer to still more extra data |

#### EFLAGS Register

| ID | Name | Description |
| --- | --- | --- |
| CF | Carry Flag | Set if the last arithmetic operation carried (addition) or borrowed (subtraction) a bit beyond the size of the register. This is then checked when the operation is followed with an add-with-carry or subtract-with-borrow to deal with values too large for just one register to contain |
| PF | Parity Flag | Set if the number of set bits in the least significant byte is a multiple of 2 |
| AF | Adjust Flag | Carry of Binary Code Decimal (BCD) numbers arithmetic operations |
| ZF | Zero Flag | Set if the result of an operation is Zero (0) |
| SF | Sign Flag | Set if the result of an operation is negative |
| TF | Trap Flag | Set if step by step debugging |
| IF | Interruption Flag | Set if interrupts are enabled |
| DF | Direction Flag | Stream direction. If set, string operations will decrement their pointer rather than incrementing it, reading memory backwards |
| OF | Overflow Flag | Set if signed arithmetic operations result in a value too large for the register to contain |
| IOPL | I/O Privilege Level field (2 bits) | I/O Privilege Level of the current process |
| NT | Nested Task flag | Controls chaining of interrupts. Set if the current process is linked to the next process |
| RF | Resume Flag | Response to debug exceptions |
| VM | Virtual-8086 Mode | Set if in 8086 compatibility mode |
| AC | Alignment Check | Set if alignment checking of memory references is done |
| VIF | Virtual Interrupt Flag | Virtual image of IF |
| VIP | Virtual Interrupt Pending flag | Set if an interrupt is pending |
| ID | Identification Flag | Support for CPUID instruction if can be set |

#### Instruction Pointer

The **EIP** register contains the address of the next instruction to be executed.

---
