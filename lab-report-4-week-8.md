# CSE 15l lab report 3 Hongchao Hu

## [My Repository](https://github.com/HongchaoHu/markdown-parser)
## [Reviewed Repository](https://github.com/ohuynh21/markdown-parser)

## Expect output for snippet 1 to 3:

<img width="599" alt="Screen Shot 2022-05-22 at 12 25 51" src="https://user-images.githubusercontent.com/91580944/169712524-4eaf50db-b370-4f02-9303-39b3aeee4bc3.png">

## Test case for my markdown-parse file for snippet 1 to 3:

<img width="744" alt="Screen Shot 2022-05-22 at 12 02 42" src="https://user-images.githubusercontent.com/91580944/169711668-1a328e17-e46b-40f9-acd5-cc8132f0d894.png">

<img width="754" alt="Screen Shot 2022-05-22 at 12 02 52" src="https://user-images.githubusercontent.com/91580944/169711673-b53c1c61-e0b6-41a8-b9ce-47f08c29580e.png">

<img width="743" alt="Screen Shot 2022-05-22 at 12 03 11" src="https://user-images.githubusercontent.com/91580944/169711678-e0b70415-2d04-4a7d-b67f-100ce7dceb1e.png">

## Test case for the reviewed markdown-parse file from week 7 for snippet 1 to 3:


<img width="752" alt="Screen Shot 2022-05-22 at 12 08 08" src="https://user-images.githubusercontent.com/91580944/169711779-741f97ac-cbad-46d7-b12a-e82540f27847.png">

<img width="746" alt="Screen Shot 2022-05-22 at 12 08 17" src="https://user-images.githubusercontent.com/91580944/169711781-e691092b-1a71-46de-8f18-8d90f8246387.png">

<img width="760" alt="Screen Shot 2022-05-22 at 12 08 25" src="https://user-images.githubusercontent.com/91580944/169711804-89ecd82d-47fe-40e1-a142-f636c4ae2e30.png">

## Test result for my markdown-parse file:

<img width="1026" alt="Screen Shot 2022-05-22 at 12 50 34" src="https://user-images.githubusercontent.com/91580944/169713380-a07e83c2-5267-435c-a0a8-b6f4ccbbe5c9.png">

## Test result for the reviewed markdown-parse file:

<img width="911" alt="Screen Shot 2022-05-22 at 12 51 15" src="https://user-images.githubusercontent.com/91580944/169713393-d18f55dd-3bf3-40af-bf6e-166e89b76280.png">

# Short response questions:
1. Snippet 1 will need a very complex change to debug because the "`" in the snippet is a big problem when distinguishing the code and normal text comments. To solve this bug, we need to implement another special helper method to deal with the relationship between "`" and the bracket parentheses because "`" has a higher priority than the other two.
2. Yes, snippet 2 can be solved with an easy change. We set a temporary integer variable for the open and close parentheses and compare them. If those two integers are not equal, the code should keep searching.
3. Yes, snippet 3 should be easy to fix. The major problem with the snippet 3 is the newline format. We just need to check if there is blank space and/or newlines between the open and close bracket, if there is, skip to the next "(" and ignore this current link.
