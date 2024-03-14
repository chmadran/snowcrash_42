<h1>LEVEL14</h1>

<h4>GETTING STARTED</h4>

We started with a brute force method, which is to exploit the iso's vulnerability that was detected by linPEAS. See below.. 

https://github.com/carlospolop/PEASS-ng/tree/master/linPEAS
https://github.com/firefart/dirtycow/blob/master/dirty.c

But there's also a way to exploit the getflag executable and reverse engineering the encoding of each token. Simply reproduce `ft_des` and pass to it the last token, which you can get access to after decompiling / analzing the executable `./bin/getflag`. You know what it is thanks to `whereis getflag`.

Another way is to exploit the `getflag` executable again, by using `gdb`. 
