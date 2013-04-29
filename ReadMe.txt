ReadMe.txt

maindict.txt is my main 18/19c dictionary, containing English, French, Latin, German, and Dutch words. Spanish, Italian, and Portuguese may still need to be added. Forms not attested in the 18c could be filtered out.

addToDictionary.txt is a list of archaic verb forms that were missing from the dictionary and probably should be folded into it.

The primary "maindict" was generated mostly by fusing existing dictionaries, although I did a bit of manual addition. I supplemented this with a "Gazetteer" of likely proper nouns that I generated myself from the 18/19c volumes by indexing them and recording tokens that occur overwhelmingly in a capitalized form (see the LexiconFlow illustration). There are more sophisticated ways of identifying proper nouns, but they don't tend to work reliably with dirty text, which is what I had to work with. The Gazetteer could be a useful supplement to existing dictionaries for OCR purposes.

maindict.txt and gazetteer.txt both have three columns: the word itself, the number of times it appeared in my corpus (capitalized or uncapitalized), and the proportion of the time it appeared capitalized (i.e., in Titlecase).

VariantSpellings.txt file has two columns, where the first is the variant and the second is the correction. For your purposes, you don't want to use these as correction rules. For one thing, I use these rules to normalize everything to Modern British spelling, and you guys presumably want to preserve American spelling where it occurs. However, the first column will be valuable as a list of variant possibilities that should count as "words," even if you just ignore the second column.

The same thing goes for my SyncopeRules.txt. You probably don't care about translating the syncopes into a normalized form. But you probably do care about recognizing the syncopat'd forms as correctly-spell'd words. I could probably make the syncope list more inclusive. I produced it by using a set of predictable rules about syncope to translate known dictionary words. But there are some really weird, unpredictable versions of syncope in the 18c. Using the larger corpus I now have, I could probably extract some of those oddities.

I've also got rules about hyphenated forms, because e.g. I want to make sure that "to day" and "to-day" always end up normalized to "today." But you guys may not care so much about this, since normalization isn't your mission.

I'm also assuming that you don't care about OCR correction, but if you do, my current list of rules is in OCRrules.txt. To be clear, I know there are some mistaken or dubious rules in this list. My goal has not been "never make any mistake" -- it's been to maximize good corrections while keeping bad ones down to an acceptable minimum. I'm always coming up with new ways to filter, refine, or expand the list; if you're interested, I could explain at more length how it was generated. But for the moment I'm assuming you're more interested in lexica.