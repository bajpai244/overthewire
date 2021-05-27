#Level 4->5

## So what's special here?

Nothing, we just have to find files that contain Human readable files.

## TL;DR

1. Change Directory to inhere
`cd inhere`
2. Read file-type of of all files
`file ./*`
3. Look for the file with ASCII text as output and get the password
`cat ./-file07`

password: koReBOKuIDDepwhWk7jZC0RTdopnAYKh

## Cool! So how did we did that?

*data* means that the files store data and on inscpection we can see that it is not human readable.

*ASCII text* is a format that can read properly so the data must be inside that file.


