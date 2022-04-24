# CSE 15l lab report 2 Hongchao Hu

## Screenshot of code change diff from Github:
![solutions](https://user-images.githubusercontent.com/91580944/164990107-54c073cc-fba4-4f18-8442-866920782f63.png)
https://github.com/HongchaoHu/markdown-parser/commit/51dd87b4c86d51288cf1e653e85cb911c1dbc0da

## Link to the test file for a failure-inducing input:
https://github.com/HongchaoHu/markdown-parser/blob/main/test-file4.md

## Show the symptom of that failure-inducing input: test-file4
![2](https://user-images.githubusercontent.com/91580944/164990909-36e7d06b-01d7-45f5-ac12-98eda0d5d46d.png)

## Describe the relationship between the bug:
The oringinal code has bug because it can not detect the "[]" and "()" symbol. What I did is to set up a series of if condition that return empty if the format of test file is invalid. For example, the test-file4 I listed above do not have proper ")" symbol, thus it should return empty.
