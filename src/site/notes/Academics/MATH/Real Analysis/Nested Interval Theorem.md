---
dg-publish: true
---
## Nested Interval Theorem
Suppose that:
- For all $i \in\mathbb{N}$, we have that $a_{i}$ and $b_{i}$ are real numbers with $a_{i}\leq b_{i}$
- For all $i\in \mathbb{N}$, we have that $a_{i}\leq a_{i+1}$ and $b_{i}\geq b_{i+1}$ (or $b_{i+1}\leq b_{i}$)
($a$'s are moving to the right, $b'$s are moving to the left)

Then 
$$
\bigcap_{i\in\mathbf{N}}[a_i,b_i]\neq\emptyset
$$
- there exists an interval in the middle ($\neq \emptyset$) between the ends of $a_{i}$ and $b_{i}$
### Proof
Every element of the set $\{ b_{i} \}$ must serve as an upper bound for the set $\{ a_{i} \}$
$\to$ There exists a least upper bound $a^{*}$ on the set $\{ a_{i} \}$
1. $a^{*}$ is $\geq$ all elements of $\{ a_{i} \}$ since it is an upper bound
2. $a^{*}$ is $\leq$ all elements of $\{ b_{i} \}$ since all of the $b_{i}$ are upper bounds with $a^{*}$ being the least upper bound

Similarly, every element of $\{ a_{i} \}$ must serve as a lower bound for the set $\{ b_{i} \}$
$\to$ There exists a greatest lower bound $b^{*}$ on the set $\{ b_{i} \}$
3. $b^{*}$ is $\leq$ all elements of $\{ b_{i} \}$ since it is a lower bound
4. $b^{*}$ is $\geq$ all elements of $\{ a_{i} \}$ since all of the $a_{i}$ are lower bounds with $b^{*}$ being the greatest lower bound

Claim: $a^{*}\leq b^{*}$
If this is true, then the interval $[a^{*},b^{*}]$ is contained in every single $[a_{i},b_{i}]$, since:
- $a^{*}>a_{i}$
- $b^{*}<b_{i}$

Suppose the negation, that $a^{*}>b^{*}$ $= sup(\{ a_{i} \})> inf(\{ b_{i} \})$

By an earlier theorem , $\forall \epsilon>0$ there would exist and element of $\{ a_{i} \}$ within the interval $(a^{*}-\epsilon,a^{*}]$.
But then if $\epsilon$ is taken to be less than $a^{*}-b^{*}$ , there would be elements of $\{ a_{i} \}$ in the interval $(b^{*},a^{*})$
- $a^{*}-b^{*}$ is positive because of $a^{*}>b^{*}$
- $(b^{*},a^{*})$ exists as $b^{*}<a^{*}$ 

But such elements would be greater than $b^{*}$. This contradicts (4)!

Hence we have that $a^{*}\leq b^{*}$, and so choosing any $x\in [a^{*},b^{*}]$, $x$ is also in each $[a_{i},b_{i}]$ (meaning the intersection is non empty)

- As such, there would be an interval $[b^{*},a^{*}]$ with elements of the set 