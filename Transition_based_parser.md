#This page describes the usage of our transition-based parser (Joint Pos-Tagging / Graph-based completion model)

# Transition-based parser including a pos-tagger and graph-based model #

Please, note that the parser is a research parser and we will provide later versions that use less memory and disc space. The parser is most similar to the parser in (Bohnet and Nivre, 2012). However, I fixed a few bugs and improved the speed.

For the training settings of different language, we would recommend to have a look on our paper (Bohnet and Nivre, 2012). For the performance of the settings of the completion model, I recommend (Bohnet and Kuhn, 2012).


## Training ##

  * For the training, a computer with 18G free main memory is needed as we jackknife 10 taggers in the training phase; I recommend to use a newer  Intel CPU with a minimum number of 4 cores better 6. I use currently mostly a (cheap) desktop CPU (Intel, 3930K, 6core, 3.2 Ghz) for the training. The training is carried out within 24 hours (beam 40, English) on this type of machine. Warning: AMD CPUs even with many cores seem not to work so well, it might take up to several days.

  * Version anna-3.3.jar is needed; Note: I have not yet included the soucre code in the repository.

  * Training and parsing settings

| **Options**               | **Description** |
|:--------------------------|:----------------|
| -train file-name          | training corpus name|
| -test file-name           | testing corpus name|
| -eval file-name           | evaluation corpus name|
| -i number                 | number of training iterations |
| -beam number              | beam size       |
| -hsize number             | size of hash kernel |
| -1st a                    | use first order factor  |
| -2nd abcd                 | use second order factors (each letter denotes a factor)  |
| -2nd abc                  | use third order factors (each letter denotes a factor)  |
| -x train:test             | train and test the pos taggers |
| -tnumber number           | number of taggers trained for jackknifing |
| -thsize     number        | hash kernal size of each of the tagger |
| -ti number                | training iterations of the pos tagger |
| -tsize                    | number of n-best tags used in the parser |
| -tthreshold number        | score threshold for used pos-tags in the parser |
| -half number              | maximum number of alternatives pos tag variants per syntactic alternative in the beam|
| -tt number                | tagger normalization factor |
| -count number             | use the first n sentences of the training corpus |


  * Example command for training of the parser
```
java -Xmx17g -classpath ~/dist/anna-3.3.jar is2.transitionR6j.Parser -train CoNLL2009-ST-English-train.txt -test CoNLL2009-ST-evaluation-English.txt -eval CoNLL2009-ST-evaluation-English.txt -out prs-result-eng -model model-eng-b40-R6j.mdl -i 20 -hsize 500000001 -cores 12 -beam 40 -1st a -2nd abcd -3rd ab -tsize -tnumber 10 -ti 10  -x train:test -thsize 90000001 -tthreshold 0.2 -tx 2  -half 2  -tt 25 
```

  * Hint: test your first model with a part of the corpus by using the option `-count 100 `


