## Lab 8 Blog

#### Installation & Tutorial
1. For this lab, I installed `Networkx` located [here](https://networkx.github.io/ using GitHub clone method).
2. After Networkx, I attempted to install `matplotlib` but I ran out of memory on my virtual box.
3. To get familiar with `Networkx`, I worked through the [tutorial](https://networkx.github.io/documentation/latest/_downloads/networkx_tutorial.pdf) until I felt comfortable.

#### Read & Understand
4. The wordladder [implementation](https://github.com/networkx/networkx/blob/master/examples/graph/words.py) provided to us was relatively simple and easy to understand.
5. I tested the code for the following 5 letter words:
    1.   `chaos` to `order`
    2.   `nodes` to `graph`
    3.   `moron` to `smart`
    4.   `pound` to `marks`
    ![]()
6. All but the last test case yield no results.
7. After modifying the code to work for 4 letter words, I tested the following 4 letter words:
    1.   `cold` to `warm`
    2.   `love` to `hate`

![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab8_1.png)
8. All of those test cases worked.

#### Implementation
9. Finally I implemented a variation of wordladder where we consider two words are adjacent if the number of letters that differ (not necessarily in same position) by 1. I modified the `edit_distance` function by adding 4 lines to it.
 ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab8_4.png)
10. Basically the code generates all permutations of `word`, and for each permutation it performs what `edit_distance` used to do.
11. Once again, I tested the new variation with the 5 letter words indicated above and it was a success.
 ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab8_3.png)
