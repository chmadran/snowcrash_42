<h1>LEVEL14</h1>

<h4>GETTING STARTED</h4>

We started with a brute force method, which is to exploit the iso's vulnerability that was detected by linPEAS. See below.. 

https://github.com/carlospolop/PEASS-ng/tree/master/linPEAS
https://github.com/firefart/dirtycow/blob/master/dirty.c

But there's also a way to exploit the getflag executable and reverse engineering the encoding of each token. Simply reproduce `ft_des` and pass to it the last token, which you can get access to after decompiling / analzing the executable `./bin/getflag`. You know what it is thanks to `whereis getflag`.

Another way is to exploit the `getflag` executable again, by using `gdb`. But when you try to use `gdb` there's a protection and the program will return "You should not reverse this" : 

```
  if ( ptrace(PTRACE_TRACEME, 0, 1, 0) < 0 )
  {
    puts("You should not reverse this");
    return 1;
  }
```

There's a way to go around it. We need to create a shared library that intercepts calls to ptrace and returns success when the PTRACE_TRACEME command is detected. By using the LD_PRELOAD environment variable to load the custom library before any other library (including the standard C library, libc), we can ensure that the ptrace wrapper function is called instead of the real one. 

But you can't do that either as the program is protected against it... 

```
level14@SnowCrash:~$ LD_PRELOAD=/var/crash/fake_ptrace.so /bin/getflag
ERROR: ld.so: object '/var/crash/fake_ptrace.so' from LD_PRELOAD cannot be preloaded: ignored.
Injection Linked lib detected exit..
```


