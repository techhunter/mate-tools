# This page describes the training of the tagger, lemmatizer, morphologic tagger and dependency parser

# Traing of a tagger, lemmatizer, morphologic tagger, and dependency parser #

All the analyser tools have similar command line options. Some options are only applicable to some tools

`java -Xmx4G -classpath anna-<version>.jar <class>`
`[-model <model>]`
`[-train <training-corpus>]`
`[-test <test-file>]`
`[-out <result-file>]`
`[-eval <evaluation-file>]`
`[-i <trainig-iterations>]`
`[-count <sentences-used>]`
`[-hsize <weight-vector-size>]`

Additional parser options:
`[-decode proj]`
`[-cores <number-of-cores>]`
`[-decodeTH <threshold>]`

The Parameters are:
  * 

&lt;version&gt;

the version of the jar file (see download section)
  * 

&lt;class&gt;

 The class and path of the tool:  `is2.parser.Parser` | `is2.tag3.Tagger` | `is2.lemmatizer.Lemmatizer` | `is2.mtag.Main`
  * 

&lt;model&gt;

 The name of a model which is created during the traing or used by tool for tagger, parsing, etc.
  * 

&lt;training-corpus&gt;

 A corpus that is used for training in [CoNLL 2009 format](http://ufal.mff.cuni.cz/conll2009-st/task-description.html#Dataformat)
  * 

&lt;test-file&gt;

 The file contains the sentences that the tools has to process
  * 

&lt;result-file&gt;

 The output of the tools in CoNLL 09 format
  * 

&lt;evaluation-file&gt;

A file the output is compared to
  * 

&lt;training-iterations&gt;

 number training rounds; typically 10
  * 

&lt;count&gt;

 the first n sentences are used only for training
  * 

&lt;weight-vector-size&gt;

 the size of the weight vector
  * 

&lt;number-of-cores&gt;

 the number of maximal employed CPU cores
  * 

&lt;threshold&gt;

Threshold of the non-projective approximation. A higher treshold does causes less non-projective links. A threshold of 0.3 has proven for English, German, and Czech as a very good choice (cf. Bohnet, 2010)

### Examples ###

Training of a tagger:

`java -Xmx2G  -classpath anna-1.jar is2.tag3.Tagger  -model models/tag-v1-eng.model  -train connl_09_st_eng_train/CoNLL2009-ST-English-train.txt `

Training, Testing, and Evaluation of the tagger:

`java -Xmx2G  -classpath anna-1.jar is2.tag3.Tagger  -model models/tag-v1-eng.model  -train connl_09_st_eng_train/CoNLL2009-ST-English-train.txt  -test gold/CoNLL2009-ST-evaluation-English.txt  -out results/tagged-eng.txt  -eval gold/CoNLL2009-ST-evaluation-English.txt`

## Training Time and Memory Consumption ##

Typical training time of the **dependency parser** is about 10 hours (a night) on a fast 4 core machine (Intel Nehalem, 3.46 Ghz) for English.  The same training time is needed on a slower 8 core AMD system (2.2 Ghz). The training times for other languages are quite different. On the Chinese corpus, the training requires the most time and resources because of many long sentences. For English, 4GB free memory is needed and for Chinese about 11GB. The model needs only about 100MB of disk space.

Typical training time of the tagger and lemmatizer is less than an hour. The needed memory is less than 2GB.
