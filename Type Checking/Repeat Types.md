Sometimes things need repeated. For instance with the repeat or variable copy patterns. (add names later). With repeated types, these can be simplified such that they are (hopefully) easier to evaluate. Especially with complex types or when the number of repeats is unknown.

Things to consider:
* Once one part of the type is modified, it should be separated from the repeat
* makes stack based sections harder to handle. Like if you are using fisherman's gambit, how do you decide where it's taking from? You either have to check each thing independently, *OR* do something like:
	* \[num of known, variable of unknown, num of known etc.]
	* and then iterate that to hopefully figure it out. Though this might be more trouble than it's worth


