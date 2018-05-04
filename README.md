# English2Japanese Dictionary
Build Japanese dictionary for English vocabulary learning

Vocabulary learning is one of the first thing to do for learning any foreign languages.

We can build vocabulary learning content based on data structure as below.
* word of the foreign laguage (string)
  * the example phrases/sentence of the foreign language (strings and/or images)
  * meaning of the word (images)
  * short corresponding word examples of the native language (string)

Only the fourth record are in the native language and the other three can be reused for any other native languages.
The forth record is actually not very important because the meaning of the word is meant be understood by images.
If we have English vocabulary learning content for Korean, it is relatively easy to create vocabulary learning content for Japaese.

With this project I am going to build an English to Japanese dictionary for Leedovoca, a famous English vocabulary learning content for Korean.

Requiremants (SRS)
* Language utilities for the native/foreign language (Japanese, English)
  * alphabet check, symbol replacement, locale, etc.,
* Scrapers for on-line dictionaries
  * extract native explanation for each word of the foreign language
    * 1 or more etymology > 1 or more part ot speech > 1 or more native words
* Word selector
  * choose a few representative words frin many candidates
