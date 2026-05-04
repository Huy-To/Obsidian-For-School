---
categories:
  - "[[Classes]]"
  - "[[Algorithm]]"
course:
source:
teacher:
email:
date:
---
Algorithm IsBalanced(expression) 

Create an empty stack S 
S = []
for each character ch in expression do 
for ch in "Hello"
	if ch is '(' or '{' or '[' then 
		Push ch onto S 
	else if ch is ')' or '}' or ']' then 
		if S is empty then 
			return "Not Balanced" 
		top ← Top element of S 
		Pop S 
		if (ch == ')' and top ≠ '(') or 
		(ch == '}' and top ≠ '{') or 
		(ch == ']' and top ≠ '[') then 
			return "Not Balanced" 
	end if 
end for 

if S is empty then 
	return "Balanced" 
else 
	return "Not Balanced" 
end Algorithm