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
- Replace 'S' with 's' everywhere, there is no difference
- Replace 'W' with 'w' everywhere, there is no difference
- Replace all "a" with "A", signifying IPA "a"
- Replace all "/ju/" with more often used "/j//u/"

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
- Fix many wrong usages of bare vowels like "a", "u", "i" with correct phoneme
- Replace all instances of "/oU/r" with "/O/r" (rhymes with "score", "north" etc)

Editorial decisions

- Replace many 'e' in French words with '/E/'
- Replace 'Z' in French words with 'z'
- End 'chutspah' with 'tsp/@/' not 'tzp/@/'
- Replace 'g' in some German words (eg 'Zug') with 'k'
- Replace many 'V' with 'v'
- Encode French ɛ̃ as in "point" as "/E/N" instead of "aN"
- Remove all "O" and replace with appropriate phoneme

Documentation

- Document phonemes used in database but not mentioned in readme
- Explain use of '(...)' as optional phoneme.

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
- "V" is sometimes Spanish β (like "b") but sometimes Dutch ʋ (like "w")
- Pronuciation of grass, glass, plant etc: /A/ or /&/?

Other to do

- Reduce redundancy of compound words: find all cases where both parts
  of a compound word can be correctly encoded independently, ensure the single
  word entries exist, then delete the compound entry.
- Swap "A" and "a", so that "a" means IPA /a/ and "A" means IPA upside-down a.
- Use "0" instead of "y" and "y" instead of "Y"
- Sort out /j//u/ vs /ju/
- Simplify encoding: use j instead of /j/, x instead of /x/, S instead of /S/, Z instead of /Z/
  E instead of /E/, I instead of /I/, D instead of /D/, maybe B instead of Spanish V, get rid of /z/
- Possibly use other sources to cross check: CMU dictionary (included); Oxford Dictionaries
  API https://developer.oxforddictionaries.com; Lingorado http://lingorado.com/ipa/;
  Words API https://www.wordsapi.com.
