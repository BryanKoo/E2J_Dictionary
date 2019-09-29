# Vietnamese translation for each english word.
I will describe how to get vietnamese word(s) as translation of each english word.

### E2V On-line Dictionaries
I have found 3 on-line English-Vietnamese dictionaries.
* http://tratu.soha.vn/
* https://dict.laban.vn/
* https://tracau.vn/index.html

### Manual draft translation without Vietamese language capability
1. prepare (word, pos-tag, key-example) triplets
(once, adverb, They have a meeting once a week), e.g.

2. look-up a E2V dictionary
There are cases that an English word cannot be found in the dictionary.
It is usually the case when there are multiple spells for an English word.
(catalog, catalogue; hardworking, hard-working; everyone, everybody; and so on)
Dictionary explains an English word with hierachy of etymologies > pos-tags > meanings > examples.
It is need to know the vietnamese translation for each pos-tag.
Phó từ is the vietnamese translation of adverb, e.g.
There is only 1 etymology for once.
There are multiple pos-tag for once (adverb, conjunction, noun, ..) but we need to check only the part of adverb(=Phó từ).
There are multiple meanings for adverb usage.
There is none or one or multiple examples for each meaning.

3. Determine the translation
If there are multiple etymology, it is highly likely that the etymology with more meanings is the more common case.
If we are looking for the most common meaning of the word, we can easily choose a etymology.
By comparing the dictionary example and the key-example, we can choose a Vietnamese translation for once.
With laban on-line dictionary, we can determine the most proper translation for once is một lần by the dictionary examples (I've only been there once, he cleans the car once a week)
If there is no dictionary example, then we cannot determine the most proper translation and we need to use group of translations, so that a vietnamese capable person can choose one among group of translations.

### Automated translation
#### Pos-tagging
If the source is only the (word, key-example) pair, it is need to find pos-tag of the word by NLP technology.
It is known that Stanford pos-tagger is one of the good NLP resource.
But it is not very correct and there are many error in finding pos-tag even for very simple sentences.

Usually a word with multiple pos-tag makes errors.
Cement in "The proportion of sand to cement used was three to one." is a noun but easy to mistake it as a verb.

And also it is naturally hard to differenciate from verb and adjective and noun if a verb is used with -ing.
Hardworking in "he is hardworking and creative" is a adjective but hard to determine pos-tag.
Melting in "the ice is melting in the sun" is verb but hard to determine pos-tag.

Someone is usually pronoun in the dictionary but pos-tagger may take it noun instead of pronoun.

While in "Please be quiet ^while^ I am studying." is conjunction but pos-tagger may take it as preposition to differenciate subordinating conjunction from coordinating conjunction.

#### Finding the most common meaning
It is likely that the meaning with more examples is the more common case.
If we are looking for the most common meaning of the word, we can choose meaning(s) with more examples.
