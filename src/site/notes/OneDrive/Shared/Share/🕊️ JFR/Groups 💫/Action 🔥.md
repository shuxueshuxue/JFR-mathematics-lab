---
{"dg-publish":true,"permalink":"/one-drive/shared/share/jfr/groups/action/"}
---


#groupAction

The Cayley diagram is the visualization of how a group G acts on itself by right (I prefer) multiplication. The action is free and transitive (and the only G-action that is both free and transitive, see [[OneDrive/Shared/Share/🕊️ JFR/Groups 💫/Move coset ⚽#remark\|Move coset ⚽#remark]]) . Any free action can be regarded as an embedding of G into the set X (but has multiple duplicates, if not transitive). Geometrically we say the local structure of every point is exactly the same.

Say now we want to model a world we want. The world(set) X has 2 status: fast and slow, 4 positions: 0, 1, 2, 3. And two operations: a. change speed b. change position.
![Pasted image 20221030151209.png](/img/user/OneDrive/Shared/Share/resource/Pasted%20image%2020221030151209.png)
In total 8 elements in the set.
We want to find a group to generalize the symmetry inside of it. Of course the generators are a and b. So we start with the biggest possible group: free group. But it's of no use. we need to discover "laws" for them, to make the group more concrete.
For we have defined how a, b act on X, we can extend this action to the whole free group F. And thus there is a natural group homomorphism $\varphi : F\to Aut(X)$ . We notice that this homomorphism is not an injective, for example, both $a^4$ and $e$ are mapped to the identity, which means there are redundant elements. So we let $G=F/ker(\varphi)$ . Because $G \cong Im(\varphi)< Aut(X)\cong S_8$ , its order must be finite, thus is much smaller and contains more information (more element, more unknown).  
The hard part is to find $ker(\varphi)$ and calculate $G$ . To do this we need to find "universal" equations that hold anywhere. In the above example, we find $a^4, b^2, (ab)^8$ to be in $ker(\varphi)$.  
The action is faithful, transitive, but not free. If it's free, we won't bother to make a group action, but instead investigate the group itself.

Sometimes the action we get is not transitive (so the group describe the general symmetry which exists in all the orbits), if we want to focus on only one orbit, we can do the quotient $G/n(Stab(x))$ , where x is an element in that orbit, $n(H)$ mimics the normalizer $N(H)$, means the largest normal subgroup of G contained by H.   
Then the resulting group is transitive, faithful on $Stab(x)$ . 
The reason is the following result

![Pasted image 20221030165348.png](/img/user/OneDrive/Shared/Share/resource/Pasted%20image%2020221030165348.png)

Rather than focus on a certain orbit, sometimes we just discard some elements in S. Like how we see $S_{n-2}$ can be embeded into $A_n$ . This is a different method.

Exp.
The group action given by left multiplication on the cosets of a subgroup H is transitive. $Stab(H)$ is H itself, so $n(Stab(x))$ is $n(H)$, and since only one orbit exists, this happen to be the kernel of the action (in general it contains the kernel because it has a weak condition : only demands elements in one orbit unchanged). 

This action is of particular importance because every possible transitive G-action can be given in this way by choosing a certain subgroup H.
