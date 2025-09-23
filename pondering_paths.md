# Pondering Paths

## The Root
Using absolute paths to invoke a program

### Solve
**Flag:** `pwn.college{MGqmCvcAM6ROrA_B-wL-i5nbTuB.QX4cTO0wSNyEzNzEzW}`

Enter the absolute path to invoke the pwn file as asked in the challenge

```bash
~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{MGqmCvcAM6ROrA_B-wL-i5nbTuB.QX4cTO0wSNyEzNzEzW}
```

### New Learnings
Absolute paths, invoking programs using absolute paths



## Program and absolute paths
invoking a file using its absolute path

### Solve
**Flag:** `pwn.college{wiXjppjwr8fp7Kp-AE-W0p0hhA-.QX1QTN0wSNyEzNzEzW}`

Enter the absolute path to invoke the run which lies in the cahllenge directory file as asked in the challenge

```bash
~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{wiXjppjwr8fp7Kp-AE-W0p0hhA-.QX1QTN0wSNyEzNzEzW}
```

### New Learnings
involing files nested in directories



## Position thy self
changing current directory to reach required directory to invoke the flag

### Solve
**Flag:** `pwn.college{cwNbWjs8MbDSE6ddQn3ZNrlJAxy.QX2QTN0wSNyEzNzEzW}`

Change current working directory to reach the correct directory to invoke the flag

```bash
~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc/fontconfig directory.

~$ cd /usr/share/doc/fontconfig

/usr/share/doc/fontconfig$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{cwNbWjs8MbDSE6ddQn3ZNrlJAxy.QX2QTN0wSNyEzNzEzW}
```

### New Learnings
changing directories and invoking the flag from a particular directory



## Position elsewhere
changing current directory to reach required directory to invoke the flag

### Solve
**Flag:** `pwn.college{8H29J-t9f8etjWj3HPNPQ8IAM1_.QX3QTN0wSNyEzNzEzW}`

Change current working directory to reach the correct directory to invoke the flag

```bash
~$ /challenge/run
Incorrect...
You are not currently in the /proc/138 directory.
Please use the `cd` utility to change directory appropriately.

~$ cd /proc/138

/proc/138$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{8H29J-t9f8etjWj3HPNPQ8IAM1_.QX3QTN0wSNyEzNzEzW}
```

### New Learnings
changing directories and invoking the flag from a particular directory




## Position yet elsewhere
changing current directory to reach required directory to invoke the flag

### Solve
**Flag:** `pwn.college{4AT4P0jNKkvupFXRCnUoTrSmhLh.QX4QTN0wSNyEzNzEzW}`

Change current working directory to reach the correct directory to invoke the flag

```bash
~$ /challenge/run
Incorrect...
You are not currently in the /sys directory.
Please use the `cd` utility to change directory appropriately.

~$ cd /sys

/sys$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{4AT4P0jNKkvupFXRCnUoTrSmhLh.QX4QTN0wSNyEzNzEzW}
```

### New Learnings
changing directories and invoking the flag from a particular directory



## Implicit relative paths, from /
invoking the flag using relative path from the / directory

### Solve
**Flag:** `pwn.college{4AT4P0jNKkvupFXRCnUoTrSmhLh.QX4QTN0wSNyEzNzEzW}`

change pwd to / and invoke the challenge(beggining with 'c') from there

```bash
~$ cd /

/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{0XShY_XPiH9qaG3uCHRVRTUhL61.QX5QTN0wSNyEzNzEzW}
```

### New Learnings
changing directories, relative paths



## Explicit relative paths, from /
invoking the flag using relative path from the / directory, using .

### Solve
**Flag:** `pwn.college{UbOeOc63EzgCDWNIxTwzkAaMAXz.QXwUTN0wSNyEzNzEzW}`

change pwd to / and invoke the challenge from there while refrencing the / using .

```bash
~$ cd /

/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{UbOeOc63EzgCDWNIxTwzkAaMAXz.QXwUTN0wSNyEzNzEzW}
```

### New Learnings
refrencing current directory using .


## implicit relative paths
invoking the flag using relative path from the challenge directory, using ./

### Solve
**Flag:** `pwn.college{8oSdOi2pl4_r8YIxgdip2qxFhka.QXxUTN0wSNyEzNzEzW}`

change pwd to /challenge and invoke the challenge from there while refrencing the pwd using ./

```bash
~$ cd /challenge

/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{8oSdOi2pl4_r8YIxgdip2qxFhka.QXxUTN0wSNyEzNzEzW}
```

### New Learnings
naked paths, invoking files in pwd using relative paths



## home sweet home
refrencing the home directory using ~ to write in a file in home

### Solve
**Flag:** `pwn.college{A66s4SWQtgzbx23eE7l-NMgyqJK.QXzMDO0wSNyEzNzEzW}`

provide an argument to /challenge/run that is a path to a file in home

```bash
~$ /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{A66s4SWQtgzbx23eE7l-NMgyqJK.QXzMDO0wSNyEzNzEzW}
```

### New Learnings
Using ~ to refrence the home directory