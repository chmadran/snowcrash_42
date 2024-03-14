<h1>LEVEL13</h1>


<h4>GETTING STARTED</h4>

Another day another executable...

<h4>INJECTION VULNERABILITY</h4>

The script we're dealing with exits unless it's run by a user with UID 4242.
But there is no user with a uid 4242.

We will exit with 0 if uid is in use and 2 if not.
/// forget all the UID stuff in the code you have the function to decode the token, it's `ft_des`.

Reproduce `ft_des` and you'll be able to decode the token by passing it as parameter. 



<details><summary> SOLUTION </summary>

* `su level12`
  
<p align="center">
👑  2A31L79asukciNyi8uppkEuSx 👑
</p>
                                           
</details>

