# Level 1 -> 2

## What is special here?

So here we have a file with name `-`, and the password for the next level is storedin it.

password is `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`

## TL;DR

Use the following command to the get password:
`cat ./-`

## Explaination

So , in Unix Like Systems we _stdin, stdout and stderr_ are called as files.

They have file descriptors 0,1,2 ( File descriptors help us to reference them )

Now `cat -` redirects the output of _stdin to stdout_.

	- So whatever we type will be sent from our stdin, cat command will print it to our stdout;
	- We can input until we send the EOF ( End of File ) command, ctrl+d
	
## How does the shell actually prints?

	( Still have to research more on this topic, I am not sure that it exactly works like that  )

Shell watches for changes in our stdout file, BTW stdout is a stream from our keyboard.

As soon as there are changes it prints it to the screen.




