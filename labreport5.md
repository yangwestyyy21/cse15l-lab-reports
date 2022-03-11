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



## Test 270


