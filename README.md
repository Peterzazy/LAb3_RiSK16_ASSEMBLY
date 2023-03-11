# LAb3_RiSK16_ASSEMBLY
-)Code for 8 instructions idea  : 
This code implements four tests to check if one number is less than, greater than, less than or equal to, or greater than or equal to another number.
The code starts by initializing eight registers (R1 through R8) with different values for testing. Then, for each test case, it loads the values of a and b into the appropriate registers (R4 and R5, respectively).
To perform the "less than" test, the code uses the NAND (not-and) instruction to compute the bitwise negation of the logical AND of a and b. If a is less than b, then a & b will not be equal to b, 
so the result of the NAND operation will not be zero, causing the code to branch to the 
"incorrect result" label and set R1 to 1. If a is greater than or equal to b, 
then a & b will be equal to b, so the result of the NAND operation will be zero, causing the code to continue to the HALT instruction.

The "greater than" test is similar to the "less than" test, but the operands to the NAND operation are swapped, so the result of the test is inverted.
The "less than or equal to" test is also similar to the "less than" test, but the operands to the NAND operation are swapped, so the result of the test is inverted.
The "greater than or equal to" test is also similar to the "greater than" test, but the operands to the NAND operation are swapped, so the result of the test is inverted.
Overall, the code is checking if a is less than, greater than, less than or equal to, or greater than or equal to b, and setting R1 to 1 if the test fails.

-)Code for operators with Special IS1



-) Q3 Special IS1
Initialize reg3 and reg4 to 0 using the MOVI instruction.
Initialize a counter reg5 to 1. This counter will be used to shift the value in reg2 left and double the value in reg1.
Enter a loop. Inside the loop, shift the value in reg2 left by the number of bits stored in reg5 using the SHL instruction, and then clear all but the least significant bit using the AND instruction.
If the least significant bit of reg6 is 0, skip to the NEXT instruction.
If the least significant bit of reg6 is 1, add the value in reg1 to reg3 using the ADD instruction.
If the counter reg5 has reached its maximum value of 15, exit the loop and go to the DONE instruction.
If the counter reg5 has not reached its maximum value of 15, double the value in reg1 using the SHL instruction, increment the counter reg5 using the ADDI instruction, and jump back to the LOOP instruction using the JALR instruction.
When the loop is finished, the result will be stored in reg3 and reg4. The least significant byte of the result will be in reg3, and the most significant byte will be in reg4. The HALT instruction stops the program.

-) Q3 special IS2 with MUL
This code loads 0 into the upper 16 bits of R3, 
multiplies the contents of R1 and R2 using the MUL instruction, and then stores the lower 16 bits of the result in R3 and the upper 16 bits in R4 using SW instructions. This code is more efficient than the previous version as it only uses three instructions to perform the multiplication and storage of the result.
