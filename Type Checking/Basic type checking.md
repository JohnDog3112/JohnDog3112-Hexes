As said before, two main components, the current stack and lookup table

Lookup table:
\[
	\[HexPattern(....), HexPattern(....)], 
	\[
		\[\[inputs...], \[outputs...]],
		\[\[inputs....],\[outputs....]]
	]
]

OR

\[
	\[HexPattern(....), HexPattern(....)], 
	\[
		\[
			\[\[inputs...], \[outputs... ]],
			\[\[inputs...], \[outputs...]]
		\]
		\[
			\[\[inputs...], \[outputs... ]]
		\]
	]
]

OR

\[
	\[HexPattern(....), HexPattern(....)], 
	\[
		\[
			\[\[inputs...],\[inputs...]],
			\[\[outputs...], \[outputs...]]
		\]
		\[
			\[\[inputs...]],
			\[\[outputs... ]]
		\]
	]
]

so that a pattern can have multiple inputs/output variations

Stack is just simply:
\[type1, type2, type3, etc...]


Basic premise is you have a list of elements to evalutate:
\[elm1, elm2, elm3...]

You pop one off the stack

elm1
\[elm2, elm3...]

check the look up table to get variations:
\[
	\[\[inputs...], \[outputs... ]]
	\[\[inputs...], \[outputs...]]
\]

if what's on the stack doesn't match any input variations, return a crash and stop checking
if it's undecided, and there is only one match resolve the undecided
if it can't be resolved, and has copies (might require smart pointers?) wait for later evaluation

if there is a possibility of a crash, return an option with the crash in it. Under the right implementation it should cascade to the end as an optional
Though maybe this isn't really necessary? idk. I feel like there are cases in which you might want intentional crashes. However, there are cases (such as arbitrary wisp code execution) in which you might want to ensure it can't crash at all