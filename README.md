# Some good links
---

**To learn regex**
<br>
https://regexone.com/problem/matching_phone_numbers?

**To parse regex**
<br>
https://regex101.com/

**Good straight to the point tutorial(in portuguese)**
<br>
https://aurelio.net/regex/apostila-conhecendo-regex.pdf


#Quick reference
---
**\d** = any digit
<br>
**\w** = any word character([a-zA-Z0-9_])
<br>
**\S** = any non-whitespace character
<br>
**\b** = Matches, without consuming any characters, immediately between a character matched by \w and a character not matched by \w (in either order). It cannot be used to separate non words from words.
<br>
**.** = matches any character (except for line terminators)
<br>
**^** = asserts position at start of a line
<br>
**$** = asserts position at end of a line
<br>
**()** = capturing group
<br>
**?** = optional, matches between zero and one times.
<br>
**\*** = can exist in any quantity
<br>
**+** = at least once
<br>
**[]** = list of characters
<br>
**[^]** = negated list: anything inside that list should tell that it shouldn't appear
<br>
**[-]** = interval list: character between the range given
<br>
**{}** = quantifier, matches any times by the input inside the braces
<br>
<br>

# Examples
---
### 1. Insert bolding from markup(\*\*word\**) between the words before the "=" sign

```
\d = any digit  
\w = any word character([a-zA-Z0-9_])  
. = matches any character (except for line terminators)
^ = asserts position at start of a line
$ = asserts position at end of a line
() = capturing group
? = optional, matches between zero and one times.
* = can exist in any quantity
+ = at least once
[] = list of characters
[^] = negated list: anything inside that list should tell that it shouldn't appear
[-] = interval list: character between the range given
{} = quantifier, matches any times by the input inside the braces
```
Desired output:

```
**\d** = any digit
**\w** = any word character([a-zA-Z0-9_])
**.** = matches any character (except for line terminators)
**^** = asserts position at start of a line
**$** = asserts position at end of a line
**()** = capturing group
**?** = optional, matches between zero and one times.
***** = can exist in any quantity
**+** = at least once
**[]** = list of characters
**[^]** = negated list: anything inside that list should tell that it shouldn't appear
**[-]** = interval list: character between the range given
**{}** = quantifier, matches any times by the input inside the braces
```

<details><summary>Click to see the answer(gnu-sed)</summary>
<p>

`sed -E 's/(^\S*)/**\1**/'`

`(^\S*)`: Using capturing group `"()"` matches any non-whitespace character, from zero to unlimited times;

`**\1**`: Get the captured group `\1`, and put "**" between it.

**improve**: check if it is possible to put a "\" if the captured group has a "*"(to not conflict the character * with the reserved * from markdown)
</p>
</details>
