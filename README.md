# Practica-3-arquitectura-de-computadoras
Practica de arquitectura 3. Se agregan diccionario de opcode para facilitar agregar instrucciones

| OPCODE | INSTRUCTION | DESCRIPTION |
| --- | --- | --- |
| 0000 | SENDTOACC | Send the value of the accumulator to a register |
        |XX|XX|XX| REGISTER CONNECTED TO A|REGISTER CONNECTED TO ACC|REGISTER THAT SAVES THE RESULT|
| 0001 | NOTA | Negate the value of the register |
        |RX|RX|RX| REGISTER CONNECTED TO A|REGISTER CONNECTED TO ACC|REGISTER THAT SAVES THE RESULT|
| 0010 | COMP2 | Convert the value of the register to two's complement |
        |RX|RX|RX| REGISTER CONNECTED TO A|REGISTER CONNECTED TO ACC|REGISTER THAT SAVES THE RESULT|
| 0011 | AND | Perform a bitwise AND operation between the accumulator and the register |
        |RX|RX|RX| REGISTER CONNECTED TO A|REGISTER CONNECTED TO ACC|REGISTER THAT SAVES THE RESULT|
| 0100 | OR | Perform a bitwise OR operation between the accumulator and the register |
        |RX|RX|RX| REGISTER CONNECTED TO A|REGISTER CONNECTED TO ACC|REGISTER THAT SAVES THE RESULT|
| 0101 | LSR | Shift the value of the register one bit to the right |
        |RX|RX|RX| REGISTER CONNECTED TO A|REGISTER CONNECTED TO ACC|REGISTER THAT SAVES THE RESULT|
| 0110 | LSL | Shift the value of the register one bit to the left |
        |RX|RX|RX| REGISTER CONNECTED TO A|REGISTER CONNECTED TO ACC|REGISTER THAT SAVES THE RESULT|
| 0111 | ADD | Add the value of the register to the accumulator |
        |RX|RX|RX| REGISTER CONNECTED TO A|REGISTER CONNECTED TO ACC|REGISTER THAT SAVES THE RESULT|
| 1000 | SUB | Subtract the value of the register from the accumulator |
        |RX|RX|RX| REGISTER CONNECTED TO A|REGISTER CONNECTED TO ACC|REGISTER THAT SAVES THE RESULT|
| 1001 | MUL | Multiply the value of the register by the accumulator |
        |RX|RX|RX| REGISTER CONNECTED TO A|REGISTER CONNECTED TO ACC|REGISTER THAT SAVES THE RESULT|
| 1010 | DIVIDE | Divide the value of the accumulator by the register |
        |RX|RX|RX| REGISTER CONNECTED TO A|REGISTER CONNECTED TO ACC|REGISTER THAT SAVES THE RESULT|
| 1011 | LOAD | Load the value of the a memory in a specific register |
        |XX|RX|XXXXXXXX| REGISTER CONNECTED TO A|REGISTER CONNECTED TO ACC|REGISTER THAT SAVES THE RESULT|

| 1100 | JUMPS | Jump to the address specified by the register |
       |0000   |JMP|Jump to the address specified by the register|
         |0001   |JALR|Jump with return|
            |0010   |BNZ| Jump if the accumulator is not zero|
               |0011   |BS| Jump if the value is negative|
                    |0100  |BNC|Jump if the carry flag is not set|
                        |0101  |BNV|Jump if the overflow flag is not set|
                            |0110 |RET |Return from of a subroutine|
                                |0111 |LEDS|Augment 1 in leds and show in the FPGA|
                                    |1000   |LEADSCLEAR|

                  
| 1101 | SENDDISPLAY | Send the value of the accumulator to the display |
| 1110 | COMPARER | Compare the value of the accumulator with the value of the register |

| 1111 | ENDPROG | Stop the execution of the program |


