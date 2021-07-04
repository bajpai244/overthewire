## Level 6-> Level 7

So, here three things are given to us:

1. The file size is 33bytes
2. The file is owned by user bandit7
3. The file is owned by group bandit 6

## The Hack.

SSH into the machine:

```
ssh bandit6@bandit.labs.overthewire.org -p 2220
password : DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```

Now, using the `groups` command will let us know that we belong to group bandit6, whic means that all the permissions provided to group bandit6 can be availed by us. 

So, let first move to the **root directory**:

`cd /`

Now, we will use find command.

`find ./ -size 33c -user bandit7 -group bandit6`

There are certain directories, which we can't open, **so all the errors written to stderr will become visible to us.**

To remove all the errors from our output, we will redirect all of them to null device. which is located at **/dev/null.**

So our command becomes:

`find ./ -size 33c -user bandit7 -group bandit6 2>/dev/null`

**2**, is the number given to stderr during redirection

Now, it will log a file path which matches this criteria.

Let's pipe output of our find command to xargs and then use it to run our cat command on the file path. 

`find ./ -size 33c -user bandit7 -group bandit6 2>/dev/null | xargs cat`

This will print the content of the file.

We could also have used `-exec` of `find` command.

Passsword for the next level: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
