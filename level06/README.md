<h1>LEVEL06</h1>


<h4>GETTING STARTED</h4>

There's a `.php` script, which uncompiled displayes two functions. 

<h4>FUNCTIONS X AND Y</h4>

The functions `preg_replace` will be executed twice with the user input from the file passed as parameter. If in the file, something starts with `[x` then the script will take it into account and execute anything as owner of the file that is `flag06` because of the setuid. 

You need to inject `getflag` in the script, add x at the beginning so it takes it into account and then send for execution ```[x {${(`/bin/getflag`)}}]```.

<details><summary> SOLUTION </summary>
  
* `su level06`

<p align="center">
👑 wiok45aaoguiboiki2tuin6ub 👑
</p>
                                           
</details>

