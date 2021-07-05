## Level 9=>10

`strings` prints all printable characters, which means that this can help us filter out all the printable characters.

`grep -E "=+` will help us find all the lines that have 1 or more than 1 = in them!

So we will pipe the result of `strings` to `grep`!

`strings data.txt | grep -E '=+'`

we will see all the desired lines, now you can easily detect which is your password!

password: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
