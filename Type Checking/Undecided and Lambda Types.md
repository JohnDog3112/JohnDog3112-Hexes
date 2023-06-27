Undecided types and lambda functions sort of go hand in hand.

When trying to evaluate a lambda function, undecideds can be a good way of figuring out possible inputs/outputs

Here is the current idea:
* All lambda functions will be evaluated down to their base inputs/outputs
* Undecideds can be used to help flesh out what inputs are going to be with the assumption that it's not going to crash
* If it will crash based on the inputs, that will be worked out when the lambda function is evaluated with respects to everything else


Lambda functions should be able to handle *multiple* input/output variations including crash possibilities 

In addition, it should be able to handle recursive or unknown repeats
For instance: [[Repeat Types]] should be evaluated such that you can know for sure it works or be able to push requirements out of the lambda function with the required parameters. In addition, unbound herme's repeats could possibly be discovered and show to crash, though not necessarily a guaranteed crash? don't know how to handle that.

Problems with Repeat Types:
* the repeat types would need to be converted to repeat input lists. However, the list might not 100% match the repeat input list in format. So there would need to be some universal type conversion. Though, maybe this won't show up at all.

Problem with herme's:
* What happens if you have like  meta-eval 1 -> meta-eval 2 -> metal-eval 1. How do you show they match up. Maybe have some meta-eval linked list that can detect loops? I'm not sure.
* How do you handle charron's gambit? maybe just save the current stack-frame as a part of an option?

Extra's about lambda types:
* things that *could* be lambda types will not be evaluated until an executor consumes them. This is because they might be changed arbitrarily later down before execution.
* Might need links between copies of lambda functions. That way repeated/recursive setups can be evaluated properly *and* it is much cheaper on evaluation to just cache the result
	* However, cached results must be ignored when the pattern is changed and no longer "linked" to the original