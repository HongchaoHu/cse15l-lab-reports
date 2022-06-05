# CSE 15l lab report 5 Hongchao Hu

## Comparing Implementations

How you found the tests with different results (Did you use vimdiff on the results of running a bash for loop? Did you search through manually? Did you use some other programmatic idea?)

* I found the test case # 489 and test case # 201 are very different from my usual tester I ran before so I used the vimdiff to comfirm my code did not pass those two tests. I initially thought the case #489 will work fine for my code since I encountered the similar tester case for my lab report 4 that also has the newliner problem. For the test case # 201, it appears that the "()" ordering may cause problem since my markdown parser only detect the content between "()". In this file, the space between the name and the link will mess up the algorithm. Then I did the vimdiff below.


    <img width="441" alt="Screen Shot 2022-06-05 at 11 03 55" src="https://user-images.githubusercontent.com/91580944/172064120-f127b736-dffd-4513-bf23-bc86c72db3bf.png">


    [#489](https://github.com/nidhidhamnani/markdown-parser/edit/main/test-files/489.md):
    
    <img width="335" alt="Screen Shot 2022-06-03 at 11 25 42" src="https://user-images.githubusercontent.com/91580944/171924315-0e387f32-25f7-4926-ae5e-5377daa0756a.png">
    <img width="313" alt="Screen Shot 2022-06-03 at 11 26 01" src="https://user-images.githubusercontent.com/91580944/171924320-0d5ad91e-6010-470c-97df-bf279f856eec.png">
    
    The TA's implementation is correct, the answer should be empty. The reason for my code failed the tester case #489 is because there is a line change in the middle of the url link. However my algorithm just check the content between the "()" and "[]" and do not care the link's completion. The solution is to when the link has newliner inside the "()" or "[]", ignore the current link and skip to the next "(".
    
    solution: 
    
    <img width="248" alt="Screen Shot 2022-06-03 at 19 00 11" src="https://user-images.githubusercontent.com/91580944/171972272-83fb9755-24fc-46c5-9e3f-b51815a90b75.png">


    [#201](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/201.md?plain=1):
    
    <img width="278" alt="Screen Shot 2022-06-03 at 11 25 36" src="https://user-images.githubusercontent.com/91580944/171924283-cb530032-05bc-40c5-a060-4ead9395f131.png">
    <img width="290" alt="Screen Shot 2022-06-03 at 11 25 29" src="https://user-images.githubusercontent.com/91580944/171924260-97a042de-5df8-43c3-97cb-444d2057324d.png">
    
    For this test case, the answer should be empty. There are two pair's of "()" and one "[]", the problem is whihinthe ordering of those pair: my code mistakenly combine the first line's second "()" with the second line's "[]" and create the false link. My solution to fix this bug is to set up a condition statement that check is the "(" exactly one index after the "]". If the format passed the condition, continue the process as usual; if not, skip the current process and go to the next "[".
    
    solution:
    
    <img width="267" alt="Screen Shot 2022-06-03 at 19 07 10" src="https://user-images.githubusercontent.com/91580944/171972659-bc4f64b6-e343-4c9e-9790-45f118abd88c.png">
