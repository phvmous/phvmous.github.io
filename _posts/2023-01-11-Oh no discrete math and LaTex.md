---
layout: post
author: Thomas Pham
tags: [latex, math]
keywords: latex, discrete math, proofs
latex: true
---
This semester I am finally biting the bullet and taking discrete math with Prof. Tannen. The first week has been painful as I haven't touched math for almost 10 years. It has definitely been a struggle refreshing on all the math I need to know for this class. So, this post isn't going to be anything special but a brain dump for all the things I learned this first week. I will also use LaTex for any math since I have to use it to write my proofs.

We'll start off with the definitions of odd and even, which is really simple. 

By definition of odd, an odd number is a integer that can be written in the form $$2k + 1$$, for some integer $$k$$. 
And, by definition of even, a even number is a integer that can be written in the form $$2k$$, for some integer $$k$$. Ok.. that was simple right? How about we do a simple proof using these definitions.

Prove if $$m + n$$is even, then $$m - n$$ is even.
Let $$m$$ and $$n$$ be any two integers.
Assume the integers $$m$$ and $$n$$ are such that $$m + n =$$ even and $$m - n =$$ even.
By definition of even, $$m + n = 2k$$. So, $$m = 2k - n$$. We can substitute $$m$$ into $$m - n$$ and get $$(2k - n) - n = 2k - 2n = 2(k - n)$$.
Because $$k - n$$ is some integer, let h denote $$k - n$$. Thus, the integers h and k are such that $$2h = 2k$$. Therefore, $$m - n$$ is even.

Furthermore, I would like to note the definition of prime numbers. By definition, an integer $$p$$ is said to be prime when $$p$$ has exactly two positive integers: 1 and itself and $$p \geq 2$$. With this definition, let's do a proof.

Proposition: if $$p$$, $$r$$, $$s$$ are positive integers such that $$p = r * s$$ and $$p$$ is prime then one of $$r$$ and $$s$$ is 1 and the other one equals $$p$$.

So to prove this, assume that $$p = r * s$$ and $$p$$ is prime. By definition of prime, either $$r = p$$ or $$r = 1$$. In the first case, if $$r = p$$, then we can write $$p = p * s = 1 = s$$. Therefore, if $$r = p$$ then $$s = 1$$. In the second case, if $$r = 1$$, then we can write $$p = 1 * s$$ to $$p = s$$. Therefore, if $$r = 1$$, then $$s = p$$. Therefore, by definition of prime, $$p$$ is prime if $$r$$ and $$s$$ is 1 and the other one equals to $$p$$.

That should complete our proof for both cases where $$r = 1$$ or $$r = p$$.
Another proof I can use under my belt is something that Prof. Tannen had in the lecture notes. Without going into too much detail, it has been proven that for all integers $$x$$, if $$x > 1$$, then $$x^3 + 1$$ is not prime. 

OK, enough of proofs for now. I'm going to talk about sets, set builder notation, and powersets, cardinality, and cartesian products.

From what I understand, sets are similar to the data structures we use in programming like Java. In math, they are said to contain unique elements. So, in other words, no elements in the set are repeated. Furthermore, in math, sets can contain objects like integers, letters of the alphabet, and even strings.

For example, here is an example of a set. $$A = \{1, 3, 5, 7\}$$. The set $$A$$ contains the elements 1, 3, 5, 7. If I wanted to refer to one element like the integer 3 in the set, I can say  $$3 \in A$$, which means 3 is an element of $$A$$. Likewise, we can say $$10 \not\in A$$, since $$A$$ does not contain the integer 10.
Let's get into subsets. With the example of the above, we can say $$\{1, 3\} \subseteq A$$, meaning $$\{1, 3\}$$ is a subset of $$A$$. We can also say that $$\{1, 3\}$$ is a proper subset of $$A$$, or $$\{1, 3\} \subset A$$ if they have no chance of being itself. Then, we have empty sets, or $$\emptyset$$.So, $$\emptyset \subseteq A$$ 

We can't forget about set builder notation now, so let's talk about it. This notation is similar to python's list comprehension `[x for x in range(1, 6)]`, which basically says that this list consists of those elements x that have the property of a number from 1 to 5. So, for set notation, if I had a set $$A$$, I can some write something like $$A = \{x \mid x \in \mathbb{Z} but x > 0 and x < 6\}$$. We also have unions and intersections. Let's have another set $$B$$ where $$B = \{2, 4, 6\}$$. Then $$A \cup B = \{1, 2, 3, 4, 5, 6, 7\}$$. So the union of set $$A$$ and $$B$$ is the set that contains elements of $$A$$ or elements of $$B$$, including those that are elements of both $$A$$ and $$B$$. We can use set builder notation for this as well, $$A \cup B = \{x \mid x \in A \text{or} x \in B\}$$ Likewise, the intersection of $$A$$ and $$B$$ is the set that contains elements of both $$A$$ and $$B$$. We can write that as $$A \cap B = \{x \mid x \in A \text{and} x \in B\}$$. The key difference between union and interset for two sets is that union is the set where elements are in one set **or** in the other set(s). In contrast, the intersection of two sets is the set that consists of elements in one set **and** in the other sets.

Now, let's get into pairwise disjoints and difference of sets. A disjoint is where a set $$A$$ and a set $$B$$ have no elements in common, which can be expressed as $$A \cap B = \emptyset$$. Now the difference of sets for set $$A = \{1, 2, 3\}$$ and set $$B = \{2, 3\}$$ can be expressed as $$A \setminus B = \{1\}$$ or $$A = \{x \mid x \in A \text{and} x \not\in B\}$$. Cardinality is basically the number of elements in the given set. So, $$\midA\mid = 3$$. And last, we have powersets and cartesion products. The powerset of $$A$$ is basically a set that contains all the subsets of $$A$$. In other words, a set that contains sets as elements. So, the powerset of $$A$$ can be expressed as, $$\mathbb{P}(A) = \{ \{1\}, \{2\}, \{3\}, \{1, 2\}, \{2, 3\}, \{1, 2, 3\}, \emptyset, \{\emptyset\}\}$$ Using set builder notation, we can say $$A = \{X \mid X \subseteq A\}$$. Sequences are known as a collection of an order of elements. They can be written as tuples. Then last we have cartesian product. It is basically pairs where the first component is a element of $$A$$ and the second component is a element of $$B$$.