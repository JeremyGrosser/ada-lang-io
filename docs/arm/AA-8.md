---
sidebar_position:  64
---

# 8 Visibility Rules

:::warning
We're still working on the Reference manual output.  Internal links are broken,
as are a bunch of other things.
See the [tracking issue](https://github.com/ada-lang-io/ada-lang-io/issues/20)
:::
{AI05-0299-1} [The rules defining the scope of declarations and the rules defining which [identifier](./AA-2.3#S0002)s, [character_literal](./AA-2.5#S0015)s, and [operator_symbol](./AA-6.1#S0202)s are visible at (or from) various places in the text of the program are described in this clause. The formulation of these rules uses the notion of a declarative region.

{AI05-0299-1} {AI12-0439-1} As explained in Clause 3, a declaration declares a view of an entity and associates a defining name with that view. The view comprises an identification of the viewed entity, and possibly additional properties. A usage name denotes a declaration. It also denotes the view declared by that declaration, and denotes the entity of that view. Thus, two different usage names can denote two different views of the same entity; in this case they denote the same entity.] 

To be honest: In some cases, a usage name that denotes a declaration does not denote the view declared by that declaration, nor the entity of that view, but instead denotes a view of the current instance of the entity, and denotes the current instance of the entity. This sometimes happens when the usage name occurs inside the declarative region of the declaration. 


#### Wording Changes from Ada 83

We no longer define the term "basic operation;" thus we no longer have to worry about the visibility of them. Since they were essentially always visible in Ada 83, this change has no effect. The reason for this change is that the definition in Ada 83 was confusing, and not quite correct, and we found it difficult to fix. For example, one wonders why an [if_statement](./AA-5.3#S0175) was not a basic operation of type Boolean. For another example, one wonders what it meant for a basic operation to be "inherent in" something. Finally, this fixes the problem addressed by AI83-00027/07. 
