# 0x16. C - Simple Shell
## Resources
- [Unix shell](https://intranet.alxswe.com/rltoken/f0YU9TAhniMXWlSXtb64Yw)
- [Thompson shell](https://intranet.alxswe.com/rltoken/7LJOp2qP7qHUcsOK2-F3qA)
- [Ken Thompson](https://intranet.alxswe.com/rltoken/wTSu31ZP1f7fFTJFgRQC7w)
- [Everything you need to know to start coding your own shell](https://intranet.alxswe.com/concepts/64)

<details>
<summary>List of allowed functions and system calls</summary>
<br>

- `access` (man 2 access)
- `chdir` (man 2 chdir)
- `close` (man 2 close)
- `closedir` (man 3 closedir)
- `execve` (man 2 execve)
- `exit` (man 3 exit)
- `\_exit` (man 2 _exit)
- `fflush` (man 3 fflush)
- `fork` (man 2 fork)
- `free` (man 3 free)
- `getcwd` (man 3 getcwd)
- `getline` (man 3 getline)
- `getpid` (man 2 getpid)
- `isatty` (man 3 isatty)
- `kill` (man 2 kill)
- `malloc` (man 3 malloc)
- `open` (man 2 open)
- `opendir` (man 3 opendir)
- `perror` (man 3 perror)
- `read` (man 2 read)
- `readdir` (man 3 readdir)
- `signal` (man 2 signal)
- `stat` (__xstat) (man 2 stat)
- `lstat` (__lxstat) (man 2 lstat)
- `fstat` (__fxstat) (man 2 fstat)
- `strtok` (man 3 strtok)
- `wait` (man 2 wait)
- `waitpid` (man 2 waitpid)
- `wait3` (man 2 wait3)
- `wait4` (man 2 wait4)
- `write` (man 2 write)

</details>

<details>
<summary>The shell will be compiled this way:</summary>
<br>

```
$ gcc -Wall -Werror -Wextra -pedantic -std=gnu89 \*.c -o hsh
```

</details>

## Output
- Unless specified otherwise, your program must have the exact same output as `sh` (`/bin/sh`) as well as the exact same error output.
- The only difference is when you print an error, the name of the program must be equivalent to your `argv[0]` (see below)

<details>
<summary>Example of error with sh:</summary>
<br>

```
$ echo "qwerty" | /bin/sh
/bin/sh: 1: qwerty: not found
$ echo "qwerty" | /bin/../bin/sh
/bin/../bin/sh: 1: qwerty: not found
$
```

</details>

<details>
<summary>Same error with your program hsh:</summary>
<br>

```
$ echo "qwerty" | ./hsh
./hsh: 1: qwerty: not found
$ echo "qwerty" | ./././hsh
./././hsh: 1: qwerty: not found
$
```

</details>

## Testing
<details>
<summary>The shell should work like this in interactive mode:</summary>
<br>

```
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$
```

</details>

<details>
<summary>But also in non-interactive mode:</summary>
<br>

```
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test\_ls\_2
$
$ cat test\_ls\_2
/bin/ls
/bin/ls
$
$ cat test\_ls\_2 | ./hsh
hsh main.c shell.c test\_ls\_2
hsh main.c shell.c test\_ls\_2
$
```

</details>

## Features
- To add as we progress

## Builtins
- To add as we progress

## Authors
- Brian Ike :wink:
