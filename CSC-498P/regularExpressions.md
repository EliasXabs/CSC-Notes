# Regular expressions: (Regex)

>## Introduction to Regular Expressions:
> Regular expressions is a way to match patterns within datasets (HTML, sec code, database, ...)\
> Usualy people use regular expressions to find and replace patterns in text. (Sometimes the find tools are not enough)\
> Or to validate the input of a form\
>
> <b> Don't confuse Regex with programming languages, Regex is not a programming language.\
> </b>
>It's a feature that is supported by most programming languages. (JAVA, C#, C++, Python, JavaScript, PHP, Perl, Ruby, ...)
>
> <b> Regular expressions are used in many fields: </b>
>   - Text processing
>   - Data validation
>   - Data extraction
>

>## Example of a REGEX
>       Let's consider these inputs:
>       Where "laubyblos", "labyblos", "lauubyblos" are accepted
>       lubyblos", "liubyblos", "labyblo" are not accepted.
>
>       Therefore to build a regex validating inputs matchin the upper pattern we need to find the pattern.
>
>       Based on the inputs we can see that the the pattern must start with "la" and end with "byblos"
>       Therefore the regex to find the pattern is : la*byblos

> ## How to build a regex
> ### Steps to build a REGEX:
>  1. understand the requirements
>  2. identify patterns in the inclusions list or the exclusions list
>  3. Represent the patterns using a regular expression
>  4. test the regex (use a regex engine like grep, python or JAVA to apply the pattern on the input) 


> ## Regex syntax
> Regular expressions are divided into two sets:
>
> 1. Basic set:\
>   The basic set comes with a set of symbols, each of which has a specific meaning and interpretation.
> 
>       - *: zero or more of the preceding character
>       - +: one or more of the preceding character
>       - .: any character
>       - \: escape character
>       - []: any character within the brackets
>       - [a-d] any character within the range
>       - [^]: any character not within the brackets
>       - ^: start of the line
>       - $: end of the line
>       - |: or
>       - (): group
>       - {n}: n occurrences of the preceding character
>       - {n,}: n or more occurrences of the preceding character
>       - {n,m}: n to m occurrences of the preceding character
>       - ?: zero or one occurence of the preceding character
>
> 2. Extended set:\
>  The extended set comes with a set of symbols, each of which has a specific meaning and interpretation.
>       - \d: any digit ([0-9])
>       - \D: any non-digit ([^0-9])
>       - \s: any whitespace character (space, tab, newline)
>       - \S: any non-whitespace character ([^\s])
>       - \w: any alphanumeric character ([a-zA-Z0-9_])
>       - \W: any non-alphanumeric character ([^\w])
>       - \b: word boundary 
>       - \B: non-word boundary 
>       - \A: start of the string   
>       - \Z: end of the string
>       - \z: end of the string
>       - \G: end of the previous match
>       - \n: nth captured group
>       - \1: first captured group
>       - \2: second captured group
>       - \n : nth captured group

# EXERCISES: 
    accepted: lauabyblos, lauxbyblos, laucbyblos
    not accepted: laubyblos, bybloslau, lauxybyblos

    it should start with lau and end with byblos and have any character between them
    the regex is: lau.byblos
>

    accepted: foobar, fooabcbar, foobxcbar, foozbar
    not accepted: barfoo, barcbyfoo, barafoo, barabfoo

    it should start with foo and end with bar and have any and as much as possible characters between them
    the regex is: foo.*bar
>

    accepted: lau   byblos, lau byblos, lau                byblos, laubyblos
    not accepted: lauxxxbyblos, lauybyblos

    it should start with lau and end with byblos and have any number of spaces between them
    the regex is: lau\s*byblos
>
    accepted: jau, kau, lau, mau
    not accepted: bau, wau, zau, cau

    it should start with any character between j and m and end with au
    the regex is: [j-m]au
>
    accepted: jau, kau, lau, mau, zau
    not accepted: bau, wau, cau

    it should start with any character between j and m or z and end with au
    the regex is: [j-mz]au
>
    accepted: jau, Kau, Lau, mau, Zau
    not accepted: bau, wau, cau

    it should start with any character between j and m or z not case sensitive and end with au
    the regex is: [j-mJ-MzZ]au
>
    accepted: xxx.yy, xx.yyyy, x.yy
    not accepted: xy, xxyy, yyxx, yx, yxxx

    it should start with any number of x and end with any number of y with a dot between them
    the regex is: x*\.y*
>
    accepted: x#y, x:y, x.y x\y
    not accepted: x&y, x%y

    it should start with x and end with y and have #, :, .
    the regex is: x[#,:.,\,,\\]y
>
    accepted: laubybloslebanon, laulebanonbyblos
    not accepted: byblostlaulebanon, lebanonlaubyblos, lebanonbybloslau

    it should start with lau and end with anything
    the regex: ^lau.*

    