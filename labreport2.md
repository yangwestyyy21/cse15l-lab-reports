# This is the lab report for lab 2

  link to homepage: [title](https://yangwestyyy21.github.io/cse15l-lab-reports/index.html)
  
## Code change 1

explanation: This was the week 3 changes. The bug here is that if a line has a website with a url with 2 sets of paranthesis like *(google.com/search")("/url)*, the file will only output the website's url up to the first paranthesis and completely skip everything after it. In the test file above, there was a case of a website as mentioned above, so it put out the wrong output. My code change attempted to solve this issue by saving the location of the current last ']' symbol and the next '\[' symbol to find the very last ')' symbol before the next '\[' in order to not prematurely stop. However it didn't work, and will be solved later.

code change: ![codechange1ss](https://user-images.githubusercontent.com/33038975/151465946-b02359e4-315e-42f5-aa00-1203fa9d0402.png)

bug: ![codechange1error](https://user-images.githubusercontent.com/33038975/151465927-53889231-cb9a-461f-94c9-03ac9638a584.png)

test file: https://github.com/yangwestyyy21/markdown-parse/blob/47e001f98db4b81a2b63fef114e3d53ac7f9d886/breakcode.md

## Code change 2

explanation: This was part of what our group worked on in the week 4 lab. Aldrin was the one who committed and did these changes to his repository, so the test file link is to his repository. All credit is given to Aldrin and Andrew for coming up with their solution while we were alternating while pair programming in the lab. In the lab we were trying to solve the issue of the code going into an infinite loop if there was any text below the last ')' in the markdown file. In the error showcase screenshot below, it says it runs out of memory after freezing for a minute, meaning it was running again and again until the computer ran out of memory. This happens because in the original code, the line ```currentIndex = closeParen + 1;``` causes the loop to repeat over and over again if there is anything after the last ')' as there is no stopping mechanism for the while loop other than ```currentIndex < markdown.length()```, which will never kick in if the currentindex goes back to the last parantheis every time. 

code change: ![codechange2ss](https://user-images.githubusercontent.com/33038975/151481393-ab5d52d4-ad9b-4018-bcb3-28d9999de60f.png)

bug: ![codechange2error](https://user-images.githubusercontent.com/33038975/151481868-bcfdd03e-4489-4176-aa4a-cfe85eb75580.png)

test file: https://github.com/aldrincheung/markdown-parse/blob/742a5372bfea28ad4da66a67be647033c4fe17dc/error-inducing.md

## Code change 3

explanation: These are changes I made to my own markdown parsing code after the week 4 lab. After some prior edits from week 3, there was a bug where the code will have am index on the string array go out of bounds while running. This is because I did not account for whether the file will contain a '\[' after the first set, or a bracket and paranthesis at all. The symptom, as shown below, is where it shows the error message when running any tests, including the default one. To fix this I added some if conditions checking whether if there were brackets and paranthesis, as well as checking whether there was a '\[' after the first set of brackets, and breaking from the loop if there wasn't any. After fixing this issue all 9 of the tests ran smoothly. 

code change: ![codechange3ss](https://user-images.githubusercontent.com/33038975/151486114-8653fd94-7725-4465-9115-0f7ce28997be.png)

bug: ![codechange3error](https://user-images.githubusercontent.com/33038975/151486128-887489f7-91bb-49ca-aaa8-ed215b2cb910.png)

test file: https://github.com/yangwestyyy21/markdown-parse/blob/67a29acae95912e07ba51c18ab2b34bad19a4244/test-file.md!

![codechange3tester](https://user-images.githubusercontent.com/33038975/151486196-bfa59dcd-2cbb-476e-b385-26f63489eda6.png)

![codechange3solvedalltests](https://user-images.githubusercontent.com/33038975/151486178-9b81113b-85b6-4748-a1db-8c47e2931452.png)


