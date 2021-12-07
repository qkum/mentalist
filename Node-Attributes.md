# Base Words
|Attribute|Description|
|:--------|:----------|
| No Words                 | Provides an empty string |
| Custom File...           | User-specified custom wordlist file |
| Custom String...         | User-specified custom string |
| English Dictionary       | English dictionary taken from the Unix `words` file |
| **Common Names**         |
| &emsp;Men                | 1,000 most common mens' names in the US |
| &emsp;Women              | 1,000 most common womens' names in the US |
| &emsp;Pets               | 1,200 most common pets' names in the US |
| **Other**                |
| &emsp;Slang & Expletives | Wordlist of US slang and expletives |
| &emsp;Months & Seasons   | Wordlist of months and seasons |

# Case
|Attribute|Description|Input|Result|
|:--------|:----------|:---:|:----:|
| No Case Change                          | Perform no action                                                 | TeSt | TeSt |
| **Lowercase**                           |
| &emsp;Lowercase All                     | Make word all lowercase                                           | TeSt | test |
| &emsp;Lowercase First, &emsp;Upper Rest | Make first character lowercase and the rest of the word uppercase | TeSt | tEST |
| **Uppercase**                           |
| &emsp;Uppercase All                     | Make word all uppercase                                           | TeSt | TEST |
| &emsp;Uppercase First, &emsp;Lower Rest | Make first character uppercase and the rest of the word lowercase | TeSt | Test |
| Toggle Nth...                           | Change the case of the Nth character                              | TeSt (N=2) | TESt | 

# Substitution
|Attribute|Description|Input|Result|
|:--------|:----------|:---:|:----:|
| No Substitution...        | Perform no action                                  | test | test |
| Replace All Instances...  | Replaces all instances of specified characters     | test<br>('t'&rightarrow;'+') | +es+ |
| Replace First Instance... | Replace the first instance of specified characters | test<br>('t'&rightarrow;'+') | +est |
| Replace Last Instance...  | Replace the last instance of specified characters  | test<br>('t'&rightarrow;'+') | tes+ | 

If a word does not match criteria for substitution, it will be output unchanged.

_**Note:** `Replace First Instance` and `Replace Last Instance` are not compatible with Hashcat & John rules. If attempting to output rules using one of these attributes in your chain, Mentalist will ask if you would like to replace these attributes with the `Replace All Instances`, which is a supported rule._

### Additional Substitution Options

**One at a Time** substitution will only substitute one specified character at a time.

**All at Once** substitution will substitute all characters at once.

|Option|Input|Substitutions|Output|
|:-----|:---:|:-----------:|:----:|
| One at a Time | apple | 'a'&rightarrow;'@'<br>'e'&rightarrow;'3' | @pple<br>appl3 |
| All at Once   | apple | 'a'&rightarrow;'@'<br>'e'&rightarrow;'3' | @ppl3 |

# Append / Prepend
|Attribute|Description|
|:--------|:----------|
| No Append / Prepend            | Perform no action |
| **Words**                      |
| &emsp;Custom File...           | User-specified custom wordlist file |
| &emsp;Custom String...         | User-specified custom string |
| &emsp;English Dictionary       | English dictionary taken from the Unix `words` file |
| &emsp;**Common Names**         |
| &emsp;&emsp;Men                | 1,000 most common mens' names in the US |
| &emsp;&emsp;Women              | 1,000 most common womens' names in the US |
| &emsp;&emsp;Pets               | 1,200 most common pets' names in the US |
| &emsp;**Other**                |
| &emsp;&emsp;Slang & Expletives | Wordlist of US slang and expletives |
| &emsp;&emsp;Months & Seasons   | Wordlist of months and seasons |
| **Numbers**                    |
| &emsp;User Defined...          | User-specified numbers (From, To, 0-padding) |
| &emsp;Small: 0-100             | Numbers ranging from 0 to 100 |
| &emsp;Basic: 0-1000            | Numbers ranging from 0 to 1000 |
| &emsp;Full: 0-10000            | Numbers ranging from 0 to 10000 |
| &emsp;Years: 1950-2025         | Numbers ranging from 1950 to 2025 |
| &emsp;Dates...                 | Dates: From Year, To Year, Format (e.g. mmddyy), Leading 0 |
| Special Characters...          | Special characters (one at a time only) |
| **Area Codes (US)**            |
| &emsp;By State                 | Area codes by state |
| &emsp;By City                  | Area codes by city (largest 50 available) |
| **Zip Codes (US)**             |
| &emsp;By State                 | Zip codes by state |
| &emsp;By City                  | Zip codes by city (largest 50 available) |