# Some good links

**To learn regex**
<br>
https://regexone.com/problem/matching_phone_numbers?

**To parse regex**
<br>
https://regex101.com/

**Good straight to the point tutorial(in portuguese)**
<br>
https://aurelio.net/regex/apostila-conhecendo-regex.pdf


# Quick reference
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
