
# 1. DFAS and Regular Languages

IF M IS-a DFA Machine 
	AND M recognizes L
Then L is IS-A Regular Language

$$L_{cats} = {\{cat, sat, tat}\}$$

Prove the following statement: ==$L_{cats}$ IS-A **Regular** Language==

## DefDFACompute Table

| Example Str | Result of running `DFA C` | In the language $L_{cats}$ |
| ----------- | ------------------------- | -------------------------- |
| cat         | accept                    | true                       |
| sat         | accept                    | true                       |
| tat         | accept                    | true                       |
| sac         | reject                    | false                      |
| tas         | reject                    | false                      |
| tsa         | reject                    | false                      |
## Proof

| Statements                            | Justifications                                               |
| ------------------------------------- | ------------------------------------------------------------ |
| 1. C `IS-A` DFA machine               | `BY` **DefDFA**                                              |
| 2. C recognizes $L_{cats}$            | `APPLY` **DefDFACompute** to $proof_{1}$                     |
| 3. $L_{cats}$ `IS-A` Regular Language | `APPLY` **DefRegLang** to `mk-AND-proof` $proof_1 \ proof_2$ |

# 2. Is it a Regular Language?

Language definition 
$$L_{grad} = {\{w \ | \ w \ is \ a \ valid \ UMB \ CS \ grad \ course \ number}\}$$
Assumption:
1. Strings in the language contain only characters from alphabet ${\{0,2,4,6}\}$
2. "Any length-3 string made up of valid alphabet characters that begins with “6” is a valid grad course number" - Professor Chang [Link](https://piazza.com/class/mtj8rgri48noz/post/24#)

----
1. 3 strings in the language
	- {600, 602, 604}
2. 3 strings not in the language
	- {200, 450, 1244}
3. $L_{grad}$ `IS-A` **Regular** Language

| Example Str | Result of running `DFA StateDiagram` | In the language $L_{grad}$ |
| ----------- | ------------------------------------ | -------------------------- |
| 600         | accept                               | true                       |
| 620         | accept                               | true                       |
| 666         | accept                               | true                       |
| 090         | reject                               | false                      |
| 240         | reject                               | false                      |
| 590         | reject                               | false                      |


| Statements                             | Justifications                                               |
| -------------------------------------- | ------------------------------------------------------------ |
| 1. StateDiagram `IS-A` **DFA** machine | `BY` **DefDFAStateDiagram**                                  |
| 2. StateDiagram recognizes $L_{grad}$  | `APPLY` **DefDFACompute** to $proof_{1}$                     |
| 3. $L_{grad}$ `IS-A` Regular Language  | `APPLY` **DefRegLang** to `mk-AND-proof` $proof_1 \ proof_2$ |
# 3. DFAs Can Do "REAL" Computation

## ExampleTable

| Example Str       | Result of running `DFA StateDiagram_1` | In the language $L$ |
| ----------------- | -------------------------------------- | ------------------- |
| (1,0)             | accept                                 | true                |
| (1,0), (0,1)      | accept                                 | true                |
| (1,0), (0,1)(1,1) | accept                                 | true                |
|                   | reject                                 | false               |
| 240               | reject                                 | false               |
| 590               | reject                                 | false               |

Prove: **L** `IS-A` **Regular** Language

| Statements                                          | Justifications                                               |
| --------------------------------------------------- | ------------------------------------------------------------ |
| 1. $\text{StateDiagram}_{1}$ `IS-A` **DFA** machine | `BY` **DefDFAStateDiagram**                                  |
| 2. StateDiagram recognizes $L$                      | `APPLY` **DefDFACompute** to $proof_{1}$                     |
| 3. $L$ `IS-A` Regular Language                      | `APPLY` **DefRegLang** to `mk-AND-proof` $proof_1 \ proof_2$ |
