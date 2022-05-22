# Week 8 Lab Report
## Markdown Snippet Testing

### Repositories
[Mine](https://github.com/ohuynh21/markdown-parser)

[Reviewed Group's](https://github.com/brandoluu/markdown-parser)

## Test 1:
<span style="color: red;">FAILED</span>
### Expected output:
![Image](/L4_screenshots/Test1exp.png)

Based on VSCode's preview, the expected output should be:
```
[`google.com, google.com, ucsd.edu}
```
### Tester code:
![Image](/L4_screenshots/Test1test.png)

### My output:
![Image](/L4_screenshots/Test1out.png)

### Reviewed Group's output:
![Image](/L4_screenshots/Test1groupout.png)



## Test 2:
<span style="color: red;">FAILED</span>
### Expected output:
![Image](/L4_screenshots/Test2exp.png)

Based on VSCode's preview, the expected output should be:
```
[a.com, a.com(()), example.com]
```
### Tester code:
![Image](/L4_screenshots/Test2test.png)

### My output:
![Image](/L4_screenshots/Test2out.png)

### Reviewed Group's output:
![Image](/L4_screenshots/Test2groupout.png)



## Test 3:
<span style="color: red;">FAILED</span>
### Expected output:
![Image](/L4_screenshots/Test3exp.png)

Based on VSCode's preview, the expected output should be:
```
[https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]
```
### Tester code:
![Image](/L4_screenshots/Test3test.png)

### My output:
![Image](/L4_screenshots/Test3out.png)

### Reviewed Group's output:
![Image](/L4_screenshots/Test3groupout.png)



## Discussion:
Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks?
> Yes. In lab report 2 (week 4) I added a way for MarkdownParse.java to differentiate between hyperlink and image syntax by checking for the existence of a "!" before each "[". I believe I could apply a similar logic to my code to address cases where there is a backtick before the "[" and check to see if there is another "`" in between "[" and ")", and if there is, exclude the link in the parenthesis from the list of links.

Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets?
> No. While I think I can fix why example.com is not being added to the list of links by simply getting rid of these lines of code:
```
//check to make sure that "]" and "(" are side by side
if (closeBracket != openParen - 1){
                return toReturn;
            }
```
> I'm not quite sure if I can address why "a.com((" is being added instead of "a.com(())" and all other cases with nested parenthesis, brackets, and backticks with a small and simple fix. I think I need a way to find out what and where the first "(" and last ")" is (as well as brackets and backticks), then include everything in between. This will likely require a couple of for loops and some conditional statements for each (nested brackets and parentheses), which will probably exceed the number of lines needed to consider the change small.

Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses?

> Yes. It seems that the problem arises when there are new lines in the "[]", more than one new line in the body of the "()", and when there is no closing parenthesis after the 1 permitted new line. To fix this, some conditional statements need to be written to check for the existence of "\n" and how many times they appear in between both the brackets and parenthesis. If it exceeds the limit, skip to the next "[" after the last "(" to avoid adding anything to the list of links. I think this change will get very close to the <10 line limit, but it's probably doable.




