# moby
Corrected versions of Moby lexical database

The original Moby database is in the public domain and is
available at http://icon.shef.ac.uk/Moby/

So far, this repository contains only the pronunciation
database, with some corrections.

## Summary of changes

### mpron - pronunciation database

Standardisation

- Change all line endings to Unix standard (single CR, 0x0a)
- Remove trailing white space from all lines

Errors

- Replace spaces with underscores inside words or phonetic encodings
- Remove underscores in phonetic encodings of words not containing underscores
- Replace 'c' with 's' or 'k' as necessary
- Replace 'x' with 'gz', '/x/' or 'ks'
- Remove doubled stress markers
- Miscellaneous fixes to bad or incomplete encodings
- Arabic pronunciation of 'Bent' is closer to 'b/I/nt'
- Remove parenthetical comments mistakenly included in phonetic encoding
- Remove some non-ascii characters and replace with best guess
- Replace double slashed '//Oi//' with '/Oi/'

Editorial decisions

- Replace 'feR' in French 'affaire...' with 'f/E/R'
- Replace 'Z' in French words with '/Z/'
- End 'chutspah' with 'tsp/@/' not 'tzp/@/'
- Replace 'g' in some German words (eg 'Zug') with 'k'
- Replace 'S' with 's' everywhere, there is no need for a distinction
- Replace 'W' with 'w' everywhere, there is no need for a distinction
- Replace many 'V' with 'v'

Documentation

- Document phonemes used in database but not mentioned in readme
- Explain use of '(/@/)' as optional phoneme.

Remaining questions

- Should 'Cipriano' begin with 's' or 'tS' (Italian pronunciation)?
- What does /z/ mean? German or Italian sound? If so, it should be 'ts'.
- When should /-/ be used instead of /@/?
- A few other issues and inconsistencies concerning non-English words.
- Inconsistent use of optional /@/ in some words, eg 'operative' and related words.
- What about several symbols used in non-English words which are (a) not
  described in the original documentation, and (b) are already encoded by
  existing symbols? Eg, "S" in some French words is just "s", and "/z/" in
  German is just "ts". Also, many uses of "e" in French words.
- American vs English pronunciations, esp, eg "Bob": "b/O/b" or "b/A/b"?
- "V" is sometimes Spanish β (like "b") but sometimes Dutch ʋ (like "w")

- Pronuciation of grass, glass, plant etc: /A/ or /&/?
