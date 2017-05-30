# Introduction to Computer Science - Fall 2017

## Lab 12 - And the correct answer is...

### Representing the data that we use

**32-bit 2s Complement Integer Coding:** Signed integers are typically stored in 32 bits (4 consecutive bytes) in 2s complement form. If the leftmost bit is 1, the integer is negative. Zero is represented by all 0 bits and all other 32-bit combinations that start with 0 represent positive integers. The 2s complement representation for a postive integer is just the binary equivalent of the value with enough leading zeros to fill all 32 bits. For example, 13<sub>10</sub> = 1101<sub>2</sub> and so the 32-bit 2s complement represetnation for 13<sub>10</sub> is

00000000000000000000000000001101

A 2s complement number is negated by creating the number's 1s complement (each 0 becomes 1 and each 1 becomes 0) and then add 1 to the result using binary addition. Here's the negation of the 2s complement form of 13<sub>10</sub> to get the representation for -13<sub>10</sub> in 2s complement form:



<table>
    <tr>
        <th><br></th>
        <th>1111  1111 1111 1111 1111 1111 1111 0010<br></th>
    </tr>
    <tr>
        <td>+</td>
        <td>0000 0000 0000 0000 0000 0000 0000 0001<br></td>
    </tr>
    <tr>
        <td colspan="2"><hr></td>
    </tr>
    <tr>
        <td></td>
        <td>1111 1111 1111 1111 1111 1111 1111 0011 <br></td>
    </tr>
</table>
