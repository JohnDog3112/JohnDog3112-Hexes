
Range:
I'm not quite sure if or how I should include the range parameter quite yet.

The basic idea is as follows: some things can only take in a range of parameters. For instance, anything to do with the stack or last manipulation must be within a certain range. Other things have limits too such as explosion, shrink/grow, etc. 

Things *required* for range parameters:
* type conversion
* mathematical operations (for more complex hexes)


Math:

Sometimes there are things that are linked. Such as when you duplicate something, for instance, [[Option]] requires some form of linking to work properly. In addition, you can have unknown stack sizes. etc. Especially if inputted from something in world. So, variables are needed to properly track this.

For instance, if you have a StackSize variable, StackSize might be the constants (like 3) and then the expansion of a stack with unknown size. This would ultimately leave you with (3 + List1Size). Which could help with tracking. 

Though, I am undecided *how* much math needs to be setup for this. Like addition, multiplication, division, subtraction, etc. Adding these would require some recursive setups though and possibly allowing multiplication of number lists