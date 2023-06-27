Syntax:
(String(Num), String(Item)) -> (Num, String(Item))
(String(Item-p1), String(Item-p2)) -> (1, String(Item))
(String(Item), String("")) -> (1, String(Item))

Summary:
\--If there isn't a number in the inputs, re-merge inputs and insert a 1
\-- otherwise, just parse the number

![[Ensure Number logo.png]]
![[Ensure Number.png]]
Code:
```
Jester's Gambit
Gemini Decomposition
Input Purification
Augur's Purification
Numerical Reflection: 1
Fisherman's Gambit II
Input Purification
Numerical Reflection: 3
Fisherman's Gambit II
Numerical Reflection: 2
Flock's Gambit
Numerical Reflection: 1
Numerical Reflection: 4
Fisherman's Gambit
Numerical Reflection: 5
Fisherman's Gambit
Gemini Decomposition
Blank Reflection
Equality Distillation
Jester's Gambit
Spacing Reflection
Jester's Gambit
Concatenation Distillation
Blank Reflection
Jester's Gambit
Augur's Exaltation
Concatenation Distillation
Numerical Reflection: 2
Flock's Gambit
Augur's Exaltation
Flock's Disintegration
```
Testing: [[Testing/Ensure Number|Ensure Number]]