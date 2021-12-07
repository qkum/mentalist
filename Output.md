# Full Wordlist

This option outputs the entire wordlist, as specified by the chain. The estimated number of words and filesize can be found in the top menu of Mentalist.

# Hashcat/John Rules

For offline cracking, there are times where the full wordlist is too large to output as a whole. In this case, it makes sense to output to rules so that Hashcat or John can programmatically generate the full wordlist.

Note that the First and Last Substitution attributes are not compatible with Hashcat/John. When a chain contains these attributes, saving to Hashcat/John will warn that First or Last will be changed to All in the rules output.

# Base Words Only

This output option allows you to output the base words into a single file to be used with your rules. This is useful if you have multiple sources of base words (multiple Base Word attributes).