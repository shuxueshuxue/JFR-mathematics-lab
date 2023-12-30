---
{"dg-publish":true,"permalink":"/one-drive/shared/share/jfr/groups/world/"}
---

#group #world

### Introduction
***Quasihedral 16*** - The quasihedral group of order 16

![Pasted image 20221011215637.png|500](/img/user/OneDrive/Shared/Share/resource/Pasted%20image%2020221011215637.png)

From its multiplication table we can see clearly that the left-top zone is ia copy of $C_8$ , and together with an order-2 element $t$ they form the whole group. But in which way do they connect with each other?

Given any two groups N and H and a group homomorphism φ: H → Aut(N), we can construct a new group N ⋊φ H, called the semidirect product of N and H with respect to φ, defined as follows:
- The underlying set is the Cartesian product N × H.
- The group operation ${\displaystyle \bullet }$ is determined by the homomorphism φ:
- $${\displaystyle {\begin{aligned}\bullet :(N\rtimes _{\varphi }H)\times (N\rtimes _{\varphi }H)&\to N\rtimes _{\varphi }H\\(n_{1},h_{1})\bullet (n_{2},h_{2})&=(n_{1}\varphi (h_{1})(n_{2}),\,h_{1}h_{2})=(n_{1}\varphi _{h_{1}}(n_{2}),\,h_{1}h_{2})\end{aligned}}}$$
>*Equivalence condition of a semidirect product*
>$$\begin{align}
\text{G is a semidirect product}&\Leftrightarrow \exists\ H\lhd G,K<G,HK=G,H\cap K=\{e\}  \\
&\Leftrightarrow \exists\ H\lhd G,K<G,G/H\cong K \\
\end{align}$$

---
##### diagram
The second condition can be rephrase as: the following exact sequence is split ($ps=id_H$)

![Pasted image 20221030142758.png](/img/user/OneDrive/Shared/Share/resource/Pasted%20image%2020221030142758.png)

---
![Pasted image 20221030140844.png|500](/img/user/OneDrive/Shared/Share/resource/Pasted%20image%2020221030140844.png)

In the game *Minecraft* , the player can live both in Overworld and in Nether. If he lives in Overworld, he can transmit himself to Nether if he build a portal (magic!), vice versa. There is a correspondence between the two world's coordinate systems: if he comes to Nether by portal A, and builds another portal B **10** meters away. Then transmit back to the Overworld through portal B, he will find himself **80** meters away from the portal A (another end, of course, it's "long" enough to connect two worlds) on the Overworld.  

***Quasihedral 16*** has a similar duel world structure, this can bee seen easily form its generators - 
⟨a, b : a<sup>8</sup> = b<sup>2</sup> = 1, bab<sup>-1</sup> = a<sup>3</sup>⟩
We can interpret $a$ as move some distance in the current world, and $b$ as change the world (or rewinding the road. Anyway, change the world's status).

We interpret an action series in Quasihedral 16 like
$abab^{-1}$ 
as "move 1 meter" "come into the Nether" "move 1 meter " "come back to Overworld"
and because 1 meter in the Nether = 3 meters on the Overworld
the result should be $a^4$, i.e.
$abab^{-1}=a^4$

Recall the first equivalence condition of semidirect product
$$\text{G is a semidirect product}\Leftrightarrow \exists\ H\lhd G,K<G,HK=G,H\cap K=\{e\}$$
We find the correspondence 
$H\lhd G$   $\Leftrightarrow$   world status can be recorded seperately
$K < G$   $\Leftrightarrow$   world status form a group (reversible, composition, identity)
$HK = G$   $\Leftrightarrow$   each group element is a combination of "move" and "change world"
$H\cap G=\{e\}$   $\Leftrightarrow$   move won't change the world, and change world status is never equivalent to a move

Metaphor : any world status is reversible. This is acceptable to me, if not romantic. At least we can restrict our view to semi-groups if necessary. But there is something more problematic : associativity. (See discussions below)

Quasihedral 16's Cayley diagram - 
![Pasted image 20221011230328.png|500](/img/user/OneDrive/Shared/Share/resource/Pasted%20image%2020221011230328.png)
 
More examples -
$D_n$ (Dihedral groups) : mirror world

### Further discussion
It's not a coincidence that Quasihedral 16 exists as a group. It is based on the fact
$$3^2=8+1$$
Why is it so important? Associative! *Associativity ristricts the group structure to be the "same" everywhere.*
Back to our *Minecraft* example. If someone has never played this game and has no idea what the Nether and what the Overworld is (even when he really sees them). The first time he enters the game world, he has to figure out where he is with the only fact he know "1 step in the Nether = 8 steps in the Overworld". And he does. Then he figures out successfully where he is. 
But will it work out the same way in the group Quasihedral 16?
***No!***
Look at the Cayley diagram. Although it does fit the pattern that "1 step on the inner circle, 3 steps on the outer circle", you will (surprisingly) find it also works on the contrary: "1 step on the outer circle, 3 steps on the inner circle".
And that's why $3^2=8+1$ is necessary. Also notice: the group acts on $C_8$ is $C_2$, so the automorphism which $e \neq x\in C_2$ maps to must be of order 2 (or order 1, in that case it becomes direct product).
The same idea can help us judge if a certain automorphism is reasonable for constructing a semidirect product. For example, the classification of groups with order $2p$ .


>$abb^{-1}=a(bb^{-1})=a$ 
>A man stands on the edge of the cliff (a). We claim if he steps forward (b), and steps back ($b^{-1}$), everything remains the same. 

To fix this, we need group [[OneDrive/Shared/Share/🕊️ JFR/Groups 💫/Action 🔥\|Action 🔥]] to be our tool.



