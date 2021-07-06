# Level 11 => 12

We will be using `tr` command to solve this.

tr commands take two sets of sequences and maps characters from set 1 to set 2.

Basically tr stands for translate.

So the command we will use the following command to retrieve the password.

`cat data.txt | tr "[A-Za-z]" "[N-ZA-Mn-za-m]"`

so what it means is that a => n, b=>o and so on!

**[n-za-m]** means the sequence [n,o...z,a,b...m]
**[N-ZA-Mn-za-m] means the sequence [N,O...,Z,A,B...M,n,o...z,a,b...m]**

So it will shift every character by 13 characters, this type of encryption is known as **ROT13.**

password: 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
