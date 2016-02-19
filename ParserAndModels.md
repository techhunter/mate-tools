#Parser and Models for Joint Morphologic and Dependency Parsing

## Parser and Models for Joint Tagging and Dependency Parsing ##

This parser provides the following technology: transition-based dependency parser, beam-search and early update, graph-based completion model, joint Part-of-Speech tagging, joint Morphologic tagging, Hash-Kernel

  * **Download** of joint parser:  [transition-1.30.jar](https://drive.google.com/file/d/0B-qbj-8rtoUMbVEzWDlvd0ZxVFU/edit?usp=sharing)   and a change log to previous version:  [log](https://drive.google.com/file/d/0B-qbj-8rtoUMem9pVEoxYUNVYzg/edit?usp=sharing)
  * Old versions with compatible models: [transition-1.29.jar](https://drive.google.com/file/d/0B-qbj-8rtoUMMlpQSGtRcmxLSms/edit?usp=sharing) [transition-1.28.jar](https://drive.google.com/file/d/0B-qbj-8rtoUMaEN5ZHhhN1JXMkk/edit?usp=sharing) [transition-1.26.jar](https://drive.google.com/file/d/0B-qbj-8rtoUMRHByX0NBMTk2TlE/edit?usp=sharing), [transition-1.24.jar](https://drive.google.com/file/d/0B-qbj-8rtoUMX3p3UjhfWlVRTXM/edit?usp=sharing)
  * New! - experimental version with selected feature template sets for different language [transition-63.jar](https://drive.google.com/file/d/0B-qbj-8rtoUMNW5iWnFtQkNQdzg/view?usp=sharing). The template sets and a script to train parser can be found in [templaes+scripts.tgz](https://drive.google.com/file/d/0B-qbj-8rtoUMbk9VXzlrZ3ZkazQ/view?usp=sharing) . The version is based on the following paper:

> Miguel Ballesteros and Bernd Bohnet   2014.   Automatic Feature Selection for Agenda-Based Dependency Parsing . 25th International Conference on Computational Linguistics (COLING 2014) Dublin, Ireland [pdf](http://anthology.aclweb.org/C/C14/C14-1076.pdf)
  * **Sample Code** for integration into other java-code: [LemmatizeAndParse.java](https://drive.google.com/file/d/0B-qbj-8rtoUMenh3VllFVUYtbDg/edit?usp=sharing)
  * Terms of use: research only (GPL), please cite:
> > _Bernd Bohnet, Joakim Nivre, Igor Boguslavsky, Richárd Farkas, Filip Ginter, Jan Hajic: Joint Morphological and Syntactic Analysis for Richly Inflected Languages. TACL 1: 415-428 (2013)_ [pdf](http://www.transacl.org/wp-content/uploads/2013/10/paperno34.pdf)
  * Commercial license and consulting is available, please contact `Bernd Bohnet`

### English Models ###
  * **Download** of Joint-Parsing-Model: [parser+tagger](https://drive.google.com/file/d/0B-qbj-8rtoUMWWlINVhqdTU0bjQ/view?usp=sharing) ; script to apply the parser [csh script](https://drive.google.com/file/d/0B-qbj-8rtoUMTUhKQ3RwNFB3amM/view?usp=sharing)


### German Models ###
  * **Download** of Joint-Parsing-Model: [parser+tagger+morphology](https://drive.google.com/file/d/0B-qbj-8rtoUMLUg5NGpBVW9JNkE/edit?usp=sharing) ; script to apply the parser [csh script](https://drive.google.com/file/d/0B-qbj-8rtoUMeUhjNWM5Qkd2VUk/edit?usp=sharing) and script for training [csh training-script](https://drive.google.com/file/d/0B-qbj-8rtoUMN2hWSlJPYWxJMmM/edit?usp=sharing)
  * **Download** of Lemmatizer-Model: [lemmatizer-model](https://drive.google.com/file/d/0B-qbj-8rtoUMaUVsWUFuOE81ZW8/edit?usp=sharing) ; script to apply the lemmatizer [csh script](https://drive.google.com/file/d/0B-qbj-8rtoUMaGwzalFKT1hYUXM/edit?usp=sharing)

### French Models ###
  * **Download** of Joint-Parsing-Model: [parser+tagger+morphology](https://drive.google.com/file/d/0B-qbj-8rtoUMYV8yalAtcFk0WFE/edit?usp=sharing)  ; script to train and apply the parser: [csh script](https://drive.google.com/file/d/0B-qbj-8rtoUMSlY4SmtTaHQtZU0/edit?usp=sharing)
  * **Download** of Lemmatizer-Model: [lemmatizer](https://drive.google.com/file/d/0B-qbj-8rtoUMMEYwY0FFLUVmeEU/edit?usp=sharing) ; script to train and apply the lemmatizer  [csh script](https://drive.google.com/file/d/0B-qbj-8rtoUMWWRzR09zblNXcDg/edit?usp=sharing)
  * We used the treebank described in the following paper for training


> _Candito M.-H., Crabbé B., and Denis P., 2010. Statistical French dependency parsing: treebank conversion and first results, Proceedings of LREC'2010, La Valletta, Malta_