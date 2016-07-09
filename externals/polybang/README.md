#[polybang ]: A polymetric [bang]er

###What it does

Polybang internally counts the number of bangs it receives and bangs every A and B interval (initially entered as creation arguments). When both the A and B bang, the synch outlet (3rd outlet) bangs. Finally, the current count is sent out the 4th outlet with each bang received.

###Inlets

- __1st inlet__
	- `[bang (`: causes [polybang ] to fire
	- `[ratio A B (`: changes the ratio and resets polybang;
	- `[A B (`: Same as sending `[Ratio A B (`;
- __2nd and 3rd inlet__
	- Changes to A and B respectively
	- Does NOT reset `[polybang ]`

###Outlets

- __1st outlet__: Bang every A (first creation argument)
- __2nd outlet__: Bang every B (second creation argument)
- __3rd outlet__: Bang when A & B bang together
- __4th outlet__: Output the current count, starting from 0, proceeding to (A*B)-1, and then resetting back to 0
