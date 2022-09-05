---
sidebar_position:  182
---

# Annex H High Integrity Systems

:::warning
We're still working on the Reference manual output.  Internal links are broken,
as are a bunch of other things.
See the [tracking issue](https://github.com/ada-lang-io/ada-lang-io/issues/20)
:::
{AI95-00347-01} This Annex addresses requirements for high integrity systems (including safety-critical systems and security-critical systems). It provides facilities and specifies documentation requirements that relate to several needs: 

Understanding program execution;

Reviewing object code;

{AI12-0439-1} Restricting language constructs whose usage can complicate the demonstration of program correctness 

Execution understandability is supported by pragma Normalize_Scalars, and also by requirements for the implementation to document the effect of a program in the presence of a bounded error or where the language rules leave the effect unspecified. 

The [pragma](./AA-2.8#S0019)s Reviewable and Restrictions relate to the other requirements addressed by this Annex. 

NOTE   {AI12-0440-1} The Valid attribute (see 13.9.2) is also useful in addressing these needs, to avoid problems that can otherwise arise from scalars that have values outside their declared range constraints.

Discussion: The Annex tries to provide high assurance rather than language features. However, it is not possible, in general, to test for high assurance. For any specific language feature, it is possible to demonstrate its presence by a functional test, as in the ACVC. One can also check for the presence of some documentation requirements, but it is not easy to determine objectively that the documentation is "adequate". 


#### Extensions to Ada 83

This Annex is new to Ada 95. 


#### Wording Changes from Ada 95

{AI95-00347-01} The title of this annex was changed to better reflect its purpose and scope. High integrity systems has become the standard way of identifying systems that have high reliability requirements; it subsumes terms such as safety and security. Moreover, the annex does not include any security specific features and as such the previous title is somewhat misleading. 
