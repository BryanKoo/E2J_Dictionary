# English2Japanese Dictionary
Vocabulary learning is one of the first thing to do for learning any foreign languages.

We can build vocabulary learning content based on data structure as below.
* word of the foreign laguage (string)
  * the example phrases/sentence of the foreign language (strings and/or images)
  * meaning of the word (images)
  * short corresponding word examples of the native language (string)

Only the fourth record is based on the native language and the other three can be reused for any other native languages.
The forth record is actually not very important because the meaning of the word is meant be understood by images.

With this project I am going to build an English to Japanese dictionary.
If we have English vocabulary learning content for Korean, it is relatively easy to create vocabulary learning content for Japaese.


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

## Resources
### Unihan_IRGSources.txt
Wiktionary is user-generated dictionary and thus it has lots of errors.
One type of error for Japanese string is using wrong kanji, which is usually from Chinese simplified character.
The file has the information about the dictionary source of each han character for each asian country.
The file is included in the following zip file. http://www.unicode.org/Public/UCD/latest/ucd/Unihan.zip

### wikt2dict https://github.com/juditacs/wikt2dict
The document format for wiktionary is wikimedia.
English wikitionary in xml file can be downloaded from the wikimedia archive.
With wikt2dict, we can get xml parsed wikimedia files for multiple languages at once.
