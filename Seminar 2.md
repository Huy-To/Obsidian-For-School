```
FUNCTION CheckBracketBalance(str)

    newStack <- New Empty Stack  // store opening brackets

    FOR i = 0 TO length(str) - 1 DO
        ch <- str[i]

        // Push any opening bracket onto the stack
        IF ch IN {'(', '{', '['} THEN
            PUSH ch TO newStack

        // Push any closing bracket onto the stack
        ELSE IF ch IN {')', '}', ']'} THEN

            IF newStack IS empty THEN
                RETURN "Not Balanced"
            END IF

            last <- POP(newStack)  // retrieve the most recent opening bracket

            // Verify 
            IF NOT IsMatchingPair(last, ch) THEN
                RETURN "Not Balanced"
            END IF
        END IF
    END FOR

    IF newStack IS empty THEN
        RETURN "Balanced"
    ELSE
        RETURN "Not Balanced" 
    END IF

END FUNCTION


HELPER FUNCTION IsMatchingPair(open, close)
    RETURN (open == '(' AND close == ')') OR
           (open == '{' AND close == '}') OR
           (open == '[' AND close == ']')
END FUNCTION
```

# Example
$$(a + b) * (c + d)$$

1. Step 1
	1.  `(`
	2. Stack = `[(]`
	3. Push
2. Step 2
	1.  `)`
	2. Stack = `[]`
	3. Pop (matching parentheses)
3. And So on