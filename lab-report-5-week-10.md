# CSE 15l lab report 5 Hongchao Hu

## Comparing Implementations

1. How you found the tests with different results (Did you use vimdiff on the results of running a bash for loop? Did you search through manually? Did you use some other programmatic idea?)

* I found the test case # 194 and test case # 201 are very different from my usual tester I ran before. I suspect my code would run into the infinite loop error for the # 194. For the test case # 201, it appears that the "()" ordering may cause problem since my markdown parser only detect the content between "()". In this file, the space between the name and the link will mess up the algorithm.

* vimdiff screenshots:

    #194:


    #201: