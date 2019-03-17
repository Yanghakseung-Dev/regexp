
## Page 1  
Regular expressions are case sensitive. Therefore Case 1 will find the specified text, but Case 2 will not.

## Page 2
Each character inside the search pattern is significant including whitespace characters (space, tab, new line).

## Page 3
Some characters have special meanings. Character ^ matches the beginning of the line (Case 1) while dollar sign $ the end of the line (Case 2)

## Page 4
If literal value of a special character is required, it must be escaped with a backslash \. Case 1 does not match anything as both characters a special, Case 2 matches all $, Case 3 matches $ only if it is the first and Case 4 the last character. Backslash has special meaning and must be also escaped for literal use (Case 5).

## Page 5
Point . matches any character.

## Page 6
The point must be escaped if literal meaning is required.

## Page 7
Inside square brackets "[]" a list of characters can be provided. The expression matches if any of these characters is found. The order of characters is insignificant.(Case 3)
## Page 8
A range of characters can be specified with [ - ] syntax. Case 1 and Case 2 are equivalent. Several ranges can be given in one expression (Case 5).

## Page 9
If a character class starts with ^, then specified characters will not be selected

## Page 10
Alternating text can be enclosed in parentheses and alternatives separated with |.

## Page 11
Quantifiers specify how many times a character can occur. Star * (Case 1) matches zero or more times, plus + (Case 2) once or more times and question mark ? (Case 3) zero or once.
## Page 12
Several examples of "*" quantifier

## Page 13
Several examples of "+" quantifier

## Page 14
Several examples of "?" quantifier

## Page 15
Curly brackets enable precise specification of character repetitions. {m} matches precisely m times (Case 1), {m,n} matches minimaly m times and maximaly n times (Case 2) and {m,}matches minimaly m times(Case 3).

## Page 16
Quantifiers "*", "+", and "?" are special cases of the bracket notation. "*" is equivalent to {0,} (Case 1, Case 2), "+" to {1,} (Case 3, Case 4), and "?" to {0,1} (Case 5, Case 6).

## Page 17
By default any subpattern matches as many times as possible. This behaviour is changed to matching the minimum number if quantifier is followed with the question mark. Compare "*" (Case 1) with "*?" (Case 2), "+" (Case 3) with "+?" (Case 4), and "?" (Case 5) with "??" (Case 6).

## Page 18
\w matches any word character ( alphanumeric plus "_" ). In some languages these letter abbreviations are not recognized. Use character classes ("[A-z0-9_]") instead (Case 5).

## Page 19
\W matches any non-word character (everything but alphanumeric plus "_" ). Compare Case 1 and Case 2. It is equivalent to "[^A-z0-9_]".

## Page 20
\s matches white space characters: space, new line and tab. \S matches any non-whitespace character.

## Page 21
\d matches any digit and \D anything else. Compare Case 1 and Case 2. Use "[0-9]" if your programming language does not support this abbreviation (Case 3).

## Page 22
\b matches a word boundary. A word boundary (\b) is defined as a spot between two characters that has a \w on one side of it and a \W on the other side of it (in either order).

## Page 23
\B matches a non (word boundary). A word boundary (\b) is defined as a spot between two characters that has a \w on one side of it and a \W on the other side of it (in either order).

## Page 24
\A matches the beginning of string. It is similar to ^, but ^ will match after each newline, if multiline strings are considered. Similarly, \Z matches only at the end of the string or before newline at the end of it. It is similar to $, but $ will match before each newline.

## Page 25
(?=<pattern>) will look ahead if the pattern exists, but will not include it in the hit.

## Page 26
(?!<pattern>) will look ahead if the pattern exists. If it does there will be no hit.