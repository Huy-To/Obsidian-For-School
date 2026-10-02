

# Rules
1. CourseRule1 $$overall = (midterm + final)/2$$
2. CourseRule2 $$IF \ overall > 90 \ THEN \ grade = A$$

# Statement
$$\text{IF} \ midterm = 87 \ \text{AND} \ final = 95 \ \text{THEN} \ grade = A$$

 - `mk-IFTHEN-proof` (`with` ASSUMPTION = $proof_A = overall > 90$ ):
	 - $proof_B = grade = A$ (`with` ASSUMPTION = $proof_A$)

| Statements                                                           | Justifications |
| -------------------------------------------------------------------- | -------------- |
| 1. $Midterm = 87$ |  First Assumption | 
| 2. $Final = 95$ | Second Assumption | 
| 3. $Overall = (midterm + final)/2$ | CourseRule1 |
| 4. $Overall = (87 + final)/2$ | `SUBST` midterm = midterm |
| 5. $Overall = (87 + 95)/2$ | `SUBST` final = final|
| 5. $Overall = 182 / 2$ | `APPLY` ARITH to $proof_5$|
| 6. $Overall = 91$ | `APPLY` DIV to $proof_6$ |
| 7. $Overall > 90$ | Definition of NUMBERS$
| 8. $grade = A$ | `APPLY` $proof_7$ |  



