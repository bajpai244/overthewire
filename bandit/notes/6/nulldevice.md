# What is a null device?

So, since we know that all devices in linux are available on /dev directory.

Linux, provides us a lot of virtual devices for programming purposes, /dev/null is one of them.

If you will try to read something from it then, you will read `NULL`.

**If you will write something to it, then it will be dumped and will be forgetten**.

- So you can use it to dump output that you don't want.

## Use it to dump erros

a lot of commands that perform a operation recurssively, get a lot of errors, example can find, grep etc.

You can dump all stderr to /dev/null.

`find / -size 44c -user user8 2>/dev/null`

Here, 2 is the file descriptor for stderr and we are saying that redirect all stderr to stdin of /dev/null, which we will basically dump all errors that will be encounteredduring this command.

## Use it to dump all output.

Sometime we just want to execute a command and don't care about it's stderr and stout logs.

We can do this in that case `command 1>/dev/null 2>&1`

So we are redirecting all stdout to null device, and we are redirecting all stderr to stdout, which indirectly means that we are again redirecting all the stderr to null device too.
