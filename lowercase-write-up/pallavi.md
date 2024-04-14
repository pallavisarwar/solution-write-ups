# [pallavi](link-to-user)

```js
function toLowerCase(s: string): string {
    let ans = '';

    for(const char of s){
        const curr = char.charCodeAt(0) - 65;
        if(curr >= 0 && curr <= 25){
            ans+= String.fromCharCode(97+curr);
        }else{
            ans+=char;
        }
    }

    return ans;
};
```

## Strategy

<!--
  Describe what strategy they used to pass this challenge.
  Careful! your strategy description should not mention
    the code they wrote to solve the challenge.

  Practice describing their strategy at a higher level:
  a simple way to understand strategy is to think of the important steps
  between the argument values and the return values.

  For example if they use a `for` loop
  you won't mention that `i` was incremented,
  but you might mention how the final result changes at each iteration.
-->
1. Iterate Over Characters: The function      iterates over each character in the input string.
2. Check for Uppercase Letters: It checks if the current character is an uppercase letter.
3. Convert to Lowercase: If the character is an uppercase letter, it converts it to lowercase using its ASCII code.
4. Build Result String: It builds the result string by appending each modified character or leaving non-alphabetic characters unchanged.
5. Return Result: Finally, it returns the resulting lowercase string.

## Implementation

<!--
  Describe the solution written by this user.
  How did they use JS to implement their strategy?
  What language features did they use?
  What decisions do you think they made and why?
-->
1. Initialize an empty string to hold the result
2. Iterate over each character in the input string
3. Get the ASCII code of the current character
4. Check if the character is an uppercase letter (ASCII range: 65-90)
5. Convert the uppercase and append to the result
6. Append non-alphabetic characters unchanged to the result
7. Return the resulting lowercase string

## Possible Refactors

<!--
  List a couple changes you could make in their code without changing their strategy.
  For example:
    `while` loops and `for` loops can often be interchanged.
    `if else`, `switch case` and `_ ? _ : _` can sometimes be interchanged.

  You don't need to actually rewrite the function.
  The goal of this section is that you exploring different JS language features
  and think of different ways to implement the same strategy.
-->
 We can use if-else instead of for-of loop.
 In if-else condition, when the condition curr >= 0 && curr <= 25 is true, 
 the uppercase character gets converted to lowercase and appended to the result.
 Otherwise, the character is left unchanged. This change doesn't affect the 
 behavior or strategy of the function. 

## References

<!--
  links that helped you to understand this solution or to think of possible refactors
-->
For ASCII code : https://www.ascii-code.com/