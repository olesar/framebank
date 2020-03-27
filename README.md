## Russian FrameBank. Offline version

### About FrameBank 
The Russian FrameBank is a spin-off of the Russian National Corpus. It further enriches the samples taken from the Main and Spoken Corpora with the annotation of frames, semantic roles, lexico-semantic constraints, and morphosyntactic structures constituting a lexical constructions with a given verb, noun, adjective or adverb. A typical example of the lexical construction is a predicate argument structure (valency pattern), e.g. Peter came to the party. We also document cases when the arguments are omitted or expressed outside their VP (or other predicate phrase), i.e. not syntactically related to their predicate directly. In addition, the non-core elements of frames such as adverbial adjuncts, negation, modal words, discursive particles are tagged within the sentence.  
Russian FrameBank can be used as a training resource for semantic role labeling (SRL), machine translation (MT), question answering (QA), and other applications like natural language processing (NLP), information retrieval (IR), and text generation (TG).  
Online version of the Russian FrameBank is available at: [http://framebank.ru](http://framebank.ru). 
For data processing, a version of FrameBank was made available by Artem Shelmanov at: [http://nlp.isa.ru/framebank_parser/](http://nlp.isa.ru/framebank_parser) and [https://github.com/IINemo/isanlp_srl_framebank](https://github.com/IINemo/isanlp_srl_framebank).   
Annotation guidelines are available at: http://framebank.wikispaces.com (in Russian).   

#### References 
When using this resource, please cite the Russian FrameBank and one of the following papers: Lyashevskaya & Kashkin 2015a (in English) or Lyashevskaya & Kashkin 2015b (in Russian).  
 
#### Key publications:  
In English:  
* Lyashevskaya, Olga, and Egor Kashkin. 2015a. FrameBank: a database of Russian lexical constructions. In M.Yu. Khachay, N. Konstantinova, A. Panchenko, D.I. Ignatov, G.V. Labunets (eds.), Analysis of Images, Social Networks and Texts. Fourth International Conference, AIST 2015, Yekaterinburg, Russia, April 9-11, 2015, Revised Selected Papers. Communications in Computer and Information Science, Vol. 542, Springer. Pp. 337-348.  
* Lyashevskaya Olga, and Egor Kashkin. 2014. Evaluation of frame-semantic role labeling in a case-marking language. Computational linguistics and intellectual technologies. Vol. 13 (20). Pp. 362-378. [PDF](http://goo.gl/eeZFzx)  

In Russian:  
* Lashevskaja, Olga, and Julia Kuznetsova. 2009. Russkij FrameNet: k zadache sozdanija korpusnogo slovarja konstrukcij [Russian FrameNet: towards a corpus-based dictionary of constructions]. In: Computational linguistics and intellectual technologies. Proceedings of International Workshop Dialogue'2009. Vol. 8 (15), 2009. Moscow: RGGU. Pp. 306-312. [PDF](http://goo.gl/YCkcjz)  
* Kashkin, Egor, and Olga Lyashevskaya. 2013. Semanticheskie roli i set' konstrukcij v sisteme FrameBank [Semantic roles and construction net in Russian FrameBank]. In: Computational linguistics and intellectual technologies. Proceedings of International Workshop Dialogue'2013. Vol. 12 (19), 2013. Moscow: RGGU. Pp. 325-343. [PDF](http://goo.gl/hWjUaT)  
* Lyashevskaya, Olga, and Egor Kashkin. 2015b. Tipy informacii o leksicheskikh konstrukcijakh v sisteme FrameBank [Annotation of lexical constructions in Russian FrameBank]. In Trudy Instituta russkogo jazyka imeni V.V.Vinogradova [Proceedings of Vinogradov Institute of the Russian Language]. Vol. 6, 2015. Pp. 464-555. [PDF](http://goo.gl/eeWGNF)  

COPYRIGHT NOTICE: The copyright of the texts used in the FrameBank samples belongs to their authors. The authors cited here (or their heirs) are kindly asked to contact olesar@yandex.ru in case they do not want their texts to be used in the Russian FrameBank.  

### Index of tables (offline release)  
All tables provided are in UTF-8, Unix (LF) line breaks, tab separated.  

Two main parts of the Russian FrameBank include:  
1. A dictionary of lexical constructions  
2. A corpus of annotated samples  

1.1. framebank_dict_cx.txt -- a dictionary of constructions: conscruction properties  
1.2. framebank_dict_cx_items.txt -- a dictionary of constructions: construction elements  

2.1. framebank_anno_ex_items.txt -- annotated samples: core frame elements annotation  
2.2  framebank_anno_ex_circ.txt -- annotated samples: non-core frame elements annotation  

3.1  exampleindex.csv -- samples used, provided with lexico-grammatical and (sometimes) semantic groups annotation (RNC). Available from: [https://cloud.mail.ru/public/5448/GWbqFPnwN](https://cloud.mail.ru/public/5448/GWbqFPnwN)    

Supplementary materials:
4.1  framebank_roles.txt -- a list of semantic roles 

RELEASE NOTE: A lot of information on word coordinates, word order, sentences underlying annotation, document properties such as author, creation time, register etc. is not available in the current offline release. Please contact olesar@yandex.ru of you need these data.

### Table structure  
===
1.1. framebank_dict_cx.txt -- a dictionary of constructions: conscruction properties
===
Header = {ConstrIndex,Constr,ConstrName,ConstrPattern,Example,Features,KeyLexemes}
ConstrIndex: construction ID
Constr: construction label (verb frameNo.patternNo) 
ConstrName: a short typical example
ConstrPattern: morphosyntactic pattern (valency pattern, idiom elements pattern)
Example: one or more examples illustrating the use
Features: aspectual etc. features
KeyLexemes: lexical constants of the construction such as a verb for its valency pattern


===
1.2. framebank_dict_cx_items.txt -- a dictionary of constructions: construction elements
===
Header = {ConstrIndex,Place,Form,Role,Rank,SemClass,KeyLexemes}

ConstrIndex: construction ID
Place: # of the element in the construction (usually mimics the so called "neutral" word order but not obligatory)
Form: morphosyntactic features
Role: semantic role
Rank: syntactic rank (e.g. Subject, DirectObject, Periphery, Clause)
SemClass: lexico-semantic constraints (e.g. Animate, InanimateConcrete, InanimateAbstract, Instrument, Sound, etc.)
KeyLexemes: lexical constants of the construction such as a verb for its valency pattern

Predicates and other lexical constants are listed as construction elements. Their roles are tagged as minus ("-"). The KeyLexemes column is provided mostly to support human assessment as it can be easily recovered from the other columns.

NOTES: Some Roles are tagged as mixed roles (e.g. "Instrument - Place") or double roles ("Instrument / Place"). The former means that the functional role of the element is both Instrument and Place while the latter means that the element can play either the role of Instrument ot the role of Place depending the context. The same rule applies to SemClass.
RELEASE NOTES: The annotation in the SemClass column has not been checked properly in v.1.0 and may contain mistakes.


===
2.1. framebank_anno_ex_items.txt -- annotated samples: core frame elements annotation
===
Header = {ConstrIndex,ExIndex,Place,PhraseGen,WordDep,Form,Role,Rank,Sem,Rea,ConstrExId,ItemExIndex,KeyLexemes}
ConstrIndex: construction ID
ExIndex: example ID
Place: No of the element in the construction
PhraseGen: PP, NP or other syntactic phrase that refer to the core frame element
WordDep: a head of PhraseGen (in quantifier phrases (QP), a content word is tagged, in PPs, a preposition + content noun are tagged)
Form: morphosyntactic features
Role: semantic role
Rank: syntactic rank (e.g. Subject, DirectObject, Periphery, Clause, Omitted, Moved)
Sem: lexico-semantic class of WordDep (e.g. Animate, InanimateConcrete, InanimateAbstract, Instrument, Sound, etc.)
Rea: class of (non)realisation (e.g. Standard; Passive, Imperative, GenNegation for standard morphosyntactic alernations; MentionedBefore, MentionedAfter, Impersonal, IndefinitePersonal, Generalized, etc. for omitted elements; ControlOrRaise, MentionedBefore, MentionedAfter for elements not directly related to the predicate syntactically) 
ConstrExId: example-construction match ID
ItemExIndex: unique ID for this table
KeyLexemes: lexical constants of the construction such as a verb for its valency pattern

NOTES: Predicates and other lexical constants are listed as construction elements. Their roles are tagged as minus ("-"). Their PhraseGens are tagged as "N/A".
RELEASE NOTES: Some core frame elements has not been fully tagged in v.1.0.


===
2.2  framebank_anno_ex_circ.txt -- annotated samples: non-core frame elements annotation
===
Header = {ConstrIndex,ExIndex,PlaceC,Phrase,Form,Role,Type,KeyLexemes}
ConstrIndex: construction ID
ExIndex: example ID
PlaceC: No of the element in the construction
Phrase: PP, NP or other syntactic phrase that refer to the non-core frame element
Form: morphosyntactic features
Role: semantic role
Type = {Circum,Modal,Gram,Control}
Circum: circumstances(adjuncts), Modal: modal (incl. negation) and speech navigating words, Gram: grammatical markers in the analytical forms of target words (cf. by, budu, etc.), Control: dependency heads of the target words which can syntactically control Subject, Object, etc.
KeyLexemes: lexical constants of the construction such as a verb for its valency pattern


===
3.1  exampleindex.csv -- samples used
===
Header = {ExIndex,Example}
ExIndex: example ID
Example: target sentence and its context, provided with lexico-grammatical and (sometimes) semantic groups annotation (RNC)

NOTES: FrameBank tags are not embedded, please use core and non-core frame elements annotation above. There are at least five different types of RNC annotation style in different parts of the table.
RELEASE NOTES: Due to the large size (ca. 500 MB) this table is available from the external repository.

===
3.1  framebank_roles.txt -- a list of semantic roles
===
Header = {Role}
Role: semantic role (explication)
NOTES: Includes core roles (ca. 100-150 roles), metaphorical roles, mixed roles, double roles, and double mixed roles.
"Mixed roles" are those where the participant plays both roles simultaniously. "Double roles" are those where the participant plays either one role or another depending on the situation. 


### Feedback 
Any feedback on annotation errors and possible improvements (taking into consideration your particular task) is much welcome. Use olesar@yandex.ru to share your experience with the Russian FrameBank.

### Other resources for Russian NLP 
Russian National Corpus: http://ruscorpora.ru
NLPub, a catalogue of resources available for Russian and other languages: https://nlpub.ru/
RU-EVAL, Russian NLP evaluation resources: http://ru-eval.ru
Univesal Dependencies for Russian: http://universaldependencies.org/

===============================================================================

=== Machine-readable metadata =================================================  
Title: Russian FrameBank v.1.1  
Documentation status: partial  
Data source: manual  
Data available since: 2016-08-07  
License: GNU GPL 3.0  
Genre: fiction news nonfiction science technology religion spoken  
Contributors: Lyashevskaya, Olga; Kashkin, Egor; Kudinov, Mikhail; Grishina, Yulia; Kuznetsova, Julia; Solonina, Ekaterina; Koroleva, Anna; Belova, Maria; Petrenko, Anna; Rusanova, Anna; Pyatykhina, Alexandra-Maria; Philippova, Alexandra; Shayakhmetova, Elena; Chudinova, Anna; Zhadaev, Nikita; Shapiro, Maria; Polyanskaya, Lyubov; Sudarikova, Eugenia; Tarasov, Arseny; Minkevich, Boris; Buturlakina, Anastasia; Kapanina, Victoria; Deputatov, Eduard; Makasheva, Zarina; Blazhievskaya, Alexandra; Lityagina, Anna; Stepanova, Daria; Bobrova, Margarita; Astafieva, Irina; Azerkovich, Ilya; Zverev, Alexey; Abdurashitiva, Galina; many other students at the School of Linguistics, Higher School of Economics, Lomonosov Moscow State University, Russian State University for the Humanities; Sholokhov Moscow State University for the Humanities (Moscow, Russia)
Affiliation: Vinogradov Russian Language Institute RAS (Moscow); National Research University Higher School of Economics (Moscow)  

===============================================================================  



@ Russian FrameBank v.1.0, 2016
