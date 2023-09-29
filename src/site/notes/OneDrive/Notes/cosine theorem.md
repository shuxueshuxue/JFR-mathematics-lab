---
{"dg-publish":true,"permalink":"/one-drive/notes/cosine-theorem/"}
---


#elementary

![Pasted image 20220822093221.png](/img/user/OneDrive/Notes/Pasted%20image%2020220822093221.png)
Given that $AB=BC,CD=ED,\angle ABC=\angle CDE=90\degree$, can we represent the area of $ABCDE$ with only $BD$ ?
Sure. By adding auxiliary lines like this, we need only calculate the area of $BDF$, which is $\dfrac12BD^2$ .

But we can also connect $AC$ and $CE$. This way we have $S_{ABCDE}=S_{ABC}+S_{ACE}+S_{ECD}$ .
Notice 
$S_{ABC}=\dfrac12AB^2$, 
$S_{ACE}=\dfrac12\sin \angle ACE\cdot AC\cdot CE=-\dfrac12\cos \angle BCD\cdot AC\cdot CE=-\cos \angle BCD\cdot BC\cdot CD$ ,
$S_{ECD}=\dfrac12 CD^2$ .
So $S_{ABCDE}=\dfrac12AB^2+\dfrac12 CD^2-\cos \angle BCD\cdot BC\cdot CD$ .
This is equel to the $\dfrac12BD^2$ that we calculated before , and this equation happened to be the cosine theorem. 

