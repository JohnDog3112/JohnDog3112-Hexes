
At a basic level, you can have a lookup table of patterns and their inputs/outputs and a stack for the current types. With this, you could just push the type data to the stack as it passes along and pop it off on consumption based on the lookup table. However, this system has issues it can't handle such as with gemini's gambit. With any stack based manipulation patterns (other than jester's gambit) you need an actual number, or a representation of a number if unknown, to actually check the validity. 

All of this leading to these primitives:
* Any of the normal pattern types: list, number, vector, pattern, etc.
* The any type for when type doesn't matter
* AnyType for when the type doesn't matter but it's preserved
* Option<type, type> for when there are multiple possibilities (such as after Augur's Exaltation)
* Range\[a..b] for when there is a range of possibilities for a number
* StackSize for general bounds checking and flock's reflection
* Possible math and variable operators for more concise things?
* Constants (for things that can't change)
* Undecided for when it hasn't yet been determined what type something is
* Lambda functions (for embedded and executed patterns), the inner pattern is evaluated separately once it's been seen to execute and outputs it's needed inputs and outputs
* Repeated type (might be too much trouble?) makes recursive evaluation a bit easier


Things to figure out:
* How to handle *infinite* recursion such as copying pattern, gemini's gambit, repeat. 
* How to allow pattern loading from scribe's gambit
* Possible type conversion, such as allowing native ItemTypeA -> ItemTypeB
* How to handle possible crashes. Allow it but notify about it? or completely block it?
* How to allow type annotations. Such as allowing scribe's reflection to allow for a certain type
* Allow for checking notation. Such as properly adjusting the read loop on consideration and introspection
* How to handle great spells
* How vanilla do I want it to be? completely (difficult)? or just go full in on hexal typing or use patternmaster's instead of direct pattern matching so great spells can be universally applied.

In depths:
[[Basic type checking]]
[[Option]]
[[Range Parameters and Math]]
[[Undecided and Lambda Types]]
[[Repeat Types]]