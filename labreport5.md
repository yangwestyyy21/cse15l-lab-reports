# This is the lab report for lab 5

  link to homepage: [title](https://yangwestyyy21.github.io/cse15l-lab-reports/index.html)
  
  The following differences were found by just using the ```diff``` command on my personal markdown parse's output data and the lab report's output data. I'll use the first difference at test 212 and the 3rd difference at test 270 as the 2 test differences required for this lab. With the ```diff``` command the '<' icon should mean the code from my repository while the '>' icon should mean code from the lab's repository. 
  
  ![cse15lab10diffs](https://user-images.githubusercontent.com/33038975/157772217-814ad966-c9c4-47b5-b77d-e0def0bae71d.png)
  
## Test 212

Since my markdown parse had an empty output while the lab one had an output of "url", I think the difference is that my code checks for the ending of .hmtl or .com or other web domains to see whether the text in the brackets is a website, while the lab code does not do that. The actual code of the test file is the following: 

```
[foo]: /url
```

[foo]

With this I think that my code is correct in outputting a blank since there is no parathesis around the "url" test, meaning that the expected output should not have anything in it, and that means that there is no link. The lab code probably judged that the "/" indicated it was a link or something, then outputted "url". I don't think that would output a website link in many cases, so fixing the bug might be best done by exclusively checking for paranthesis on the code for the lab. 

## Test 270

My code output some weird gibberish with a bunch of "/", "\", and "\*", while the lab code outputted an empty string. I think the difference is becuase my code got confused when reading "\*" or the "/" characters and ended up outputting some mess of an output. The actual code of the test file is:

- foo

      bar
      
There is not even brackets around something or parathesis in this case, so I'm pretty sure the correct answer should be empty and the lab code is correct. I honestly have no clue how my code ended up outputting what it did, it's probably due to it getting confused by the bullet point before "foo" and outputting it as "/bar\" and then being unable to find a title so it just output title in a weird way afterwards. I have no idea on how to address the bullet point, maybe just add an if condition that checks for them and returns empty.  
