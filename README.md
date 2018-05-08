# English2Japanese Dictionary
Vocabulary learning is one of the first thing to do for learning any foreign languages.

We can build English vocabulary learning content based on data structure as below.
* English word (string)
  1 example phrases/sentences in English (strings)
  2 meaning of the word (images)
  3 short corresponding words of the learner's language (string)

When we build above English vocabulary learning contents for multiple other languages, the first two records will be the same for all. Only the third record should be prepared for each language.
I am going to build English dictionaries for multiple other languages in programmatic way for the third record.
Japanese is the first and other asian languages will be followed.

## Homograph and Polysemes (from the definition of wikipedia)
Homographs are words that have two or more different meanings.
Two types of homographs are homonym and heteronym, distinguished by the prononciation.

## Software Requiremants
* Language utilities for the native/foreign language (Japanese, English)
  * alphabet check, symbol replacement, locale, etc.,
* Scrapers for on-line dictionaries
  * english dictionary which has japanese translation (wiktionary)
  * japanese dictionary (wiktionary, koto, weblio)
* Word selector
  * extract native explanations for each word of the foreign language
    * 1 or more etymologies > 1 or more pos's(part of speech) > 1 or more corresponding native words
  * choose a few representative words from many candidates
  * neet to process special symbols to connect each meaning (, : ;) in dictionaries
  * need to define policy for choosing representative word
  * common policy is choosing short word
  * preferences for japanese are kanji > hiragana > katagana > english

## External Resources
### wikt2dict https://github.com/juditacs/wikt2dict
The document format for wiktionary is wikimedia.
English wikitionary in xml file can be downloaded from the wikimedia archive.
With wikt2dict, we can get xml parsed wikimedia files for multiple languages at once.
However, it is needed to add some code in config.py for downloading wiktionary of asian countries.

### Unihan_IRGSources.txt
Wiktionary is user-generated dictionary and thus it has lots of errors.
One type of error for Japanese string is using wrong kanji, which is usually from Chinese simplified character.
The file has the information about the dictionary source of each han character for each asian country.
The file is included in the following zip file. http://www.unicode.org/Public/UCD/latest/ucd/Unihan.zip
