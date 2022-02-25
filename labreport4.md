# This is the lab report for lab 4

  link to homepage: [title](https://yangwestyyy21.github.io/cse15l-lab-reports/index.html)
  
## Expected outputs:

![test1](https://user-images.githubusercontent.com/33038975/155639890-224ae17e-3866-4350-b0cd-f95ffdc2593e.png)

Test snippet 1 results would be [`google.com]

![test2](https://user-images.githubusercontent.com/33038975/155639898-a5309eeb-9afe-4956-8cc4-ae4e19f2d42b.png)

Test snippet 2 results would be [a.com, a.com(()), example.com]

![test3](https://user-images.githubusercontent.com/33038975/155639905-c355b12b-4a7f-45fa-bfe3-5682c113b8ab.png)

Test snippet 3 results would be [https://ucsd-cse15l-w22.github.io/]


## Running cases on my code

[Link to my MarkdownParse](https://github.com/yangwestyyy21/markdown-parse)

My MarkdownParseTest: 

![mdtest](https://user-images.githubusercontent.com/33038975/155674915-fcf0abc5-745f-4051-95d9-69cbdacd6f64.png)

Error messages (nothing works since I think this is still code from weeks 5 or 6): 

![owncodeerrormsg](https://user-images.githubusercontent.com/33038975/155674965-57eb6c1e-a99b-47b2-b6b4-c90884c07f06.png)

## Running cases on the reviewed code

[Link to the code](https://github.com/tylercyang/markdown-parse)

I had to add the test cases for snippets 1-3 and adjust the tester to test those, as their code didn't have that in the repository. Made changes in VIM and added them to the remote ssh. All of the cases failed on the reviewed code as well. Images are below in this order (added tests, changed tester, error outputs): 

![addteststoother](https://user-images.githubusercontent.com/33038975/155806599-2900b121-e174-480a-953c-d14fbcfa356b.png)

![edittedothertester](https://user-images.githubusercontent.com/33038975/155806644-fd0612f8-f65b-4b6a-a4a2-84bcf22f2227.png)

![Screenshot (20)](https://user-images.githubusercontent.com/33038975/155806661-5c40f138-0f68-4f93-90d5-413d833c74f1.png)

## Proposed solutions for each snippet case

Snippet 1: I think my code needs large edits in order to successfully handle the case of backticks as I never even thought of those as a potential issue. There's no loop or mechanism in the code that addresses the backticks so I'd have to write a bunch of new edge cases and loops involving backticks from the ground up.  

Snippet 2: For the second case of nested parenthesis, it will need more than 10 lines. There can be a pretty quick fix by adding a counter for paranthesis by adding a counter so for every '(', it goes up, and for every ')' it goes down, and once it hits 0 or a ')' before a new line, it will cut off and return the string inside as an output. However, checking for nested brackets and escaped parenthesis might require more work. For escaped brackets adding an if case that ignores chars with a '\' in front will take a few lines, and having the front bracket reset all the other brackets when a new '[' appears will also take some work. 

Snippet 3: For the 3rd case of addressing newlines I think there can be a solution that can be implemented pretty quickly. There just needs to be an additional part in the if statements checking if it is still in the same line throught checking if there is a \n character between startparen+1/endparen-1 or startbracket/endbracket. If it does find the \n character, it will just return nothing that loop with  ```continue;```.
