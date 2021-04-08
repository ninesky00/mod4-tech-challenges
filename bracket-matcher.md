# Bracket Matcher

Ever wonder how your linter knows if you have matching brackets? Well it's time to think of a solution to that!

Given a set of brackets, `[, {, (`, create a function that determines if the brackets are well-formed (match) or not - even with bracket nesting. For example:

```javascript
bracket('{}');

// => true
```

```javascript
bracket('{(');

// => false
```

```javascript
bracket('{()}');

// => true
```

```javascript
bracket('{[)][]}');

// => false
```

```javascript
bracket(']');

// => false
```

```javascript
bracket('({[]}{[]})');

// => true
```

## Instructions

1. Copy this markdown and paste in your own, private gist
2. In your private gist, fill out the questions below
4. Submit by the due time as instructed in Zoom


## Rewrite the question in your own words:
given brackets, check if they are properly matched, () = true, (() = false


## What assumptions will you make about this problem if you cannot ask any more clarifying questions? What are your reasons for making those assumptions?
I think the instructions for this problem is fairly straight forward.

## What are your initial thoughts about this problem? (high level design, 2-3 sentences)
I think this problem would require a stack data type.  
Must check for each type of bracket notation, so probably a hash map.  

## How would you identify the elements of this problem?

- [ ] Searching of Data
- [ ] Sorting of Data
- [x] Pattern Recognition
- [ ] Build/Navigate a Grid
- [ ] Math
- [ ] Language API knowledge
- [ ] Optimization


## Which data structure(s) do you think you'll use? What pros/cons do you see with that choice?
Hash map, because of the brackets being binary, ( => ) is very suitable.  
Stack, I think a stack data structure of first in last out allows the check for proper bracket match, ie. {(}) would be an incorrect match whereas {()} would be.

## Write out a few lines of initial pseudocode: (mid-level design, NOT REAL CODE)
 - create a hash map
 - create a stack data structure
 - for given string, check character, if character is a left bracket, insert into stack, if character is right bracket, pop from stack and check if they are matched, ignore all other characters
 - return true or false based on if the stack is empty or if there was a mismatch of brackets 
 - 
## Write out any implementation code OR link to repl

## What is the Big O complexity of your solution?
O(n) + O(1) + O(1)
