This might not need it's own page, but here it is

An option has two, and only two variations. However, an option is itself a type, so you can have:

Option\<A, Option\<B, C>> as far down as needed

When an option is consumed, both option variations (recursive) will be evaluated with the pattern and the return will be an option of all possibilities. 

Possible additions
* option compacting. If it's like Option\<String, String>, maybe just collapse down to String (recursive)
* option linking, sometimes options are intrinsically linked, where you'll have two options where if A on option 1 is selected, A on option 2 is selected as well. This can be considered if both options are consumed at the same time (with linked options, transformations will stay linked as well)