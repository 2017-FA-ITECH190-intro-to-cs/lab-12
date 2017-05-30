# Introduction to Computer Science - Fall 2017

## Lab 12 - And the correct answer is...

### Representing the data that we use

**32-bit 2s Complement Integer Coding:** Signed integers are typically stored in 32 bits (4 consecutive bytes) in 2s complement form. If the leftmost bit is 1, the integer is negative. Zero is represented by all 0 bits and all other 32-bit combinations that start with 0 represent positive integers. The 2s complement representation for a postive integer is just the binary equivalent of the value with enough leading zeros to fill all 32 bits. For example, 13<sub>10</sub> = 1101<sub>2</sub> and so the 32-bit 2s complement represetnation for 13<sub>10</sub> is

`0000 0000 0000 0000 0000 0000 0000 1101`

A 2s complement number is negated by creating the number's 1s complement (each 0 becomes 1 and each 1 becomes 0) and then add 1 to the result using binary addition. Here's the negation of the 2s complement form of 13<sub>10</sub> to get the representation for -13<sub>10</sub> in 2s complement form:

<pre>
 1111 1111 1111 1111 1111 1111 1111 0010 = 1s complement of 13 (base 10)
+0000 0000 0000 0000 0000 0000 0000 0001
----------------------------------------
 1111 1111 1111 1111 1111 1111 1111 0011 = -13 (base 10)
</pre>

Usually, 32 bits at a time is difficult for humans to process, so we often write long strings of bits using hexadecimal. The conversion is easy. Start at the right hand side, grab chunks of four bits and look up the corresponding hexadecimal character in the following table.

| Bit String | Hex | Bit String | Hex |
|------------|-----|------------|-----|
| 0000       | 0   | 1000       | 8   |
| 0001       | 1   | 1001       | 9   |
| 0010       | 2   | 1010       | A   |
| 0011       | 3   | 1011       | B   |
| 0100       | 4   | 1100       | C   |
| 0101       | 5   | 1101       | D   |
| 0110       | 6   | 1110       | E   |
| 0111       | 7   | 1111       | F   |

So, if we perform this on the 32-bit representation of 13<sub>10</sub>, we get 0000000D. And the 2s complement representation of -13<sub>10</sub> would be FFFFFFF3.

### ASCII Coding for Characters

In the ASCII coding scheme, each character is uniquely represented by a single byte (8 bits) that is called the ASCII code for the character. Since a character string is a sequences of characters, a string can be represented by consecutive byte representations for its characters. For example, the string "Bemidji" is stored in consecutive bytes of memory as:

0100 0010 0110 0101 0110 1101 0110 1101 0110 0100 0110 1010 0110 1001

To see this, let's first convert the binary to hexadecimal using the table above.

42 65 60 69 64 6A 69

Next, we look them up in any [ASCII table](http://www.asciitable.com/) and verify that each hexadecimal code corresponds to the correct letter. **Be sure to use the hex column.**

### Representing Colors

Colors are typically represented using 24 bits. The first eight bits are dedicated to the color Red. The second eight bits are dedicated to the color Green. The last eight bits are dedicated to the color Blue. Sometimes this is called the RGB color scheme. Each of the eight bit chunks is interpreted as an unsigned integer that indicates the intensity of the given color. Since there are 8 bits, there are 256 different possible intensities for each color (0 to 255).

Let's consider the color

011011110010100111111111

It is fairly common to express the eight bits as two hexadecimal dgitis, each representing four bits. As before, this is much easier for humans to wrap their brains around. So in the hexadecimal scheme, this color is:

6F29FF

A reasonable question to ask is what color is this? You can begin to guess. The intensity of red is just under half the possible intensity (6F/FF). There is just a little bit of green in the color (29/FF) and the maximum possible amount of blue (FF/FF). So, a bluish purple seems a pretty good guess. There are lots of ways to verify the answer. This [web page](http://itech190.erickuha.com/representation/color.html) offers a no frills way of finding out. Try it.

### The Assignment

All of the instructions for the lab assignment are included in the document included in this repository. You will have to either clone the repo to your computer or download the `.odt` file directly from the repository and open it with LibreOffice or Microsoft Word in order to edit it.

Once you have completed the assignment, save it and push the repository back to your master branch for grading.
