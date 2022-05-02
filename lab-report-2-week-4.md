# CSE 15l lab report 2 Hongchao Hu

## Screenshot of code change diff from Github:
![solutions](https://user-images.githubusercontent.com/91580944/164990107-54c073cc-fba4-4f18-8442-866920782f63.png)
https://github.com/HongchaoHu/markdown-parser/commit/51dd87b4c86d51288cf1e653e85cb911c1dbc0da

## Link to the test file for a failure-inducing input:
test-file4:
https://github.com/HongchaoHu/markdown-parser/blob/main/test-file4.md

test-file5
https://github.com/HongchaoHu/markdown-parser/blob/main/test-file5.md

test-file8:
https://github.com/HongchaoHu/markdown-parser/blob/main/test-file8.md

## Show the symptom of that failure-inducing input: test-file4, test-file5, test-file8
![2](https://user-images.githubusercontent.com/91580944/164990909-36e7d06b-01d7-45f5-ac12-98eda0d5d46d.png)
![5](https://user-images.githubusercontent.com/91580944/166328175-050523ce-6571-4693-8ce1-1413c239238d.png)
![8](https://user-images.githubusercontent.com/91580944/166328179-0199ef6a-16dd-40ad-9888-9f1e4360a970.png)


## Describe the relationship between the bug:
test-file4: The oringinal code has bug because it can not detect the "[]" and "()" symbol. What I did is to set up a series of if condition that return empty if the format of test file is invalid. For example, the test-file4 I listed above do not have proper ")" symbol, thus it should return empty.

test-file5: The weblink in test-file5 run into problem because the program and only recognize the webilnk that sit inside of  
adjacent "[]" and "()". So even there is a whole paragraph between the "()" and "[]", the program still connect the name and website link together.

test-file8: The test-file8 only contain one set of complete name and link composition, so it only return the firt link which is correct. The second set was missing the rest of name and link part thus the program would not return it.
