# ICS3203-CAT2-Assembly-Kithinji_Faith_Kathomi_151674
# Assembly Program - Control Flow, Logic, and Modular Tasks

This repository contains assembly programs showcasing the use of Control Flow and Conditional Logic, Array Manipulation with Looping and Reversal, Modular Program with Subroutines for Factorial Calculation, and Data Monitoring and Control Using Port-Based Simulation. Each program demonstrates a unique concept and its implementation using assembly language.

---

## 1. Control Flow and Conditional Logic

### Task Overview:
Classify a user-input number as **POSITIVE**, **NEGATIVE**, or **ZERO** by leveraging **branching logic** and conditional jumps.

### Steps:
1. Accept user input.
2. Compare the input using conditional jumps (`je`, `jg`, `jl`).
3. Branch to the appropriate label to display the classification.

### Key Concepts:
- **Conditional Jumps**: Instructions like `je`, `jg`, and `jl` guide the program's flow based on specific conditions.
- **Unconditional Jumps**: Ensures the program skips to subsequent operations after completing a classification.

### Implementation Notes:
- **`je` (Jump if Equal)**: Verifies if the number is zero.
- **`jg` (Jump if Greater)**: Determines if the number is positive.
- **`jl` (Jump if Less)**: Checks if the number is negative.

### Challenges:
- The main challenge here is to ensure that the correct jump instruction is used based on the input number's value. This requires accurate comparison and control of flow.

---

## 2. Array Manipulation with Looping and Reversal

### Task Overview:
Reverse an array of 5 integers **in place** and output the result. This operation does not use additional memory for a second array.

### Steps:
1. Input an array of integers.
2. Use a **loop** to swap elements symmetrically (e.g., first with last).
3. Output the reversed array.

### Key Concepts:
- **In-Place Reversal**: Reverses the array directly within its original memory.
- **Looping**: Iterates through half the array to minimize operations and achieve reversal efficiently.

### Implementation Notes:
- Swapping is performed by iterating only through the first half of the array.
- This method is memory-efficient as no additional storage is allocated for the reversed array.

### Challenges:
- Manipulating arrays without additional space can be tricky. The loop needs to handle the swap logic while avoiding overwriting values prematurely.
  
---

## 3. Modular Programming with Subroutines for Factorial Calculation

### Task Overview:
Calculate the factorial of a user-provided number using a modular approach via subroutines.

### Steps:
1. Accept a number as input.
2. Call a **subroutine** to compute the factorial.
3. Print the result.

### Key Concepts:
- **Subroutines**: Encapsulate reusable logic into a separate, callable block of code.
- **Stack Management**: Save and restore register states to maintain program flow integrity.

### Implementation Notes:
- The subroutine uses a loop and registers for iterative multiplication.
- Registers are saved to the stack before computation and restored after to avoid overwriting important values.

### Challenges:
- Subroutine handling can be tricky, especially when saving and restoring registers. Care must be taken to ensure that the main program's state is not overwritten by subroutine execution.

---

## 4. Data Monitoring and Control via Port-Based Simulation

### Task Overview:
Simulate a control system by reading a **sensor value** (e.g., water level) from memory and performing appropriate actions like turning on a motor or triggering an alarm.

### Steps:
1. Read a "sensor value" from a simulated memory location.
2. Execute conditional checks:
   - Trigger an alarm if the value exceeds a threshold.
   - Stop the motor if the value is moderate.
3. Perform actions by setting or clearing specific bits.

### Key Concepts:
- **Memory-Based Input/Output**: Simulates real-world sensor and actuator interaction through memory operations.
- **Control Actions**: Use bit manipulation to simulate outputs like motor activation or alarm triggering.

### Implementation Notes:
- Conditional checks guide the program to decide the appropriate control action.
- The simulation uses predefined memory addresses to mimic hardware input/output.

### Challenges:
- Simulating control systems with assembly can be complex due to the need to manage memory and simulate real-time hardware interaction using conditional checks.
 
---

## Documentation Guidelines

Each program includes detailed comments explaining:
1. The purpose of **jumps** and their role in controlling logic flow.
2. The use of loops for array manipulation and efficient data handling.
3. Subroutine logic for modular programming and stack management.
4. Simulated input/output mechanisms for control system tasks.

---

## How to Run:
1. Assemble the code using the assembler for your platform (e.g., `nasm`).
   -    for conditional logic and control flow program - task 1:
   ```
   nasm -f elf64 control_flow.asm -o control_flow.o

   ```
   
   -    for second program for array manipulation:
   ```
   nasm -f elf64 array_reverse.asm -o array_reverse.o

   ```
   
   -    for third program for factorial calculation
   ```
   nasm -f elf64 factorial.asm -o factorial.o

   ```
   
   -    for fourth program for data monitoring
   ```
   nasm -f elf64 port_control.asm -o port_control.o


   ```
   
3. Link the object files to create an executable.

 -   for the first task:
     
    ```
    ld -o control_flow control_flow.o
    ```

   -   for the second task:
      
    ```
    ld -o array_reverse array_reverse.o
    ```

   -   for the third task:

      
    ```
    ld -o factorial factorial.o

    ```
 -   for the fourth task:
      
    ```
    ld -o port_control port_control.o

    ```

5. Run the program in a terminal, and provide the required inputs as prompted.

   -   for the first task:
     
   ```
   ./control_flow
   ```

   -   for the second task:
     
   ```
   ./array_reverse

   ```

   -   for the third task:
   
   ```
   ./factorial
   ```

   -   for the fourth task:
     
   ```
   ./port_control
   ```
   
