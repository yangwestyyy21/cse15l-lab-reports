# This is the lab report for lab 2

  link to homepage: [title](https://yangwestyyy21.github.io/cse15l-lab-reports/index.html)
  
## Code change 1

explanation: This was the week 3 changes. The bug here is that if a line has a website with a url with 2 sets of paranthesis like *(google.com/search")("/url)*, the file will only output the website's url up to the first paranthesis and completely skip everything after it. In the test file above, there was a case of a website as mentioned above, so it put out the wrong output. My code change attempted to solve this issue by saving the location of the current last ']' symbol and the next '\[' symbol to find the very last ')' symbol before the next '\[' in order to not prematurely stop. However it didn't work, and will be solved later.

code change: ![codechange1ss](https://user-images.githubusercontent.com/33038975/151465946-b02359e4-315e-42f5-aa00-1203fa9d0402.png)

bug: ![codechange1error](https://user-images.githubusercontent.com/33038975/151465927-53889231-cb9a-461f-94c9-03ac9638a584.png)

test file: https://github.com/yangwestyyy21/markdown-parse/blob/47e001f98db4b81a2b63fef114e3d53ac7f9d886/breakcode.md

## Code change 2

explanation: This was part of what our group worked on in the week 4 lab. Aldrin was the one who committed and did the changes to his repository, so the test file link is to his repository. All credit is given to Aldrin and Andrew for coming up with their solution while we were alternating while pair programming in the lab. In the lab we were trying to solve the issue of the code going into an infinite loop if there was any text below the last ')' in the markdown file. In the error showcase screenshot below, it says it runs out of memory after freezing for a minute, meaning it was running again and again until the computer ran out of memory. This happens because in the original code, the line ```currentIndex = closeParen + 1;``` causes the loop to repeat over and over again if there is anything after the last ')' as there is no stopping mechanism for the while loop other than ```currentIndex < markdown.length()```, which will never kick in if the currentindex goes back to the last parantheis every time. 

code change: ![codechange2ss](https://user-images.githubusercontent.com/33038975/151481393-ab5d52d4-ad9b-4018-bcb3-28d9999de60f.png)

bug: ![codechange2error](https://user-images.githubusercontent.com/33038975/151481868-bcfdd03e-4489-4176-aa4a-cfe85eb75580.png)

test file: https://github.com/aldrincheung/markdown-parse/blob/742a5372bfea28ad4da66a67be647033c4fe17dc/error-inducing.md

## Code change 3

explanation: 

code change: 

bug: 

test file: 
