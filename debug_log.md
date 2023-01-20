# Debug Log

**Explain how you used the VSCode debugger tools to uncover the bugs in Exercise 7. Be specific. What breakpoints did you set? Where did you step to? What made you realize the error?**

_Example: I set a breakpoint on line 5 and stepped until line 12. There, I discovered that the `x` variable had a value of `-3`, whereas it should have had a value of `7`. That made me realize that we should be adding the two numbers `x` and `y`, instead of subtracting._

I set a breakpoint on line 9 and used the step over until I got to line 11. The variable, `remainder_of_sentence` is "" when it should have a value. I updated the `remainder_of_sentence` variable from `start_str[len(start_str):]` to `sentence[len(start_str):]`, which fixes that issue.

Continuing to go down through the recursions, we find a problem on line 13.

The line, `replace_substring(start_str[1:], start_str, replace_str)` should use the sentence instead of the target string, changing to `replace_substring(sentence[1:], start_str, replace_str)`.