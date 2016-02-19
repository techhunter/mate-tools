# How to use the dependency parser from the command line? #

**What you need to run the parser:**

  1. The 'jar'-file containing the parser, please download anna.jar (see Downloads)
  1. A model for the parser (e.g. prs-eng.model, see Downloads)
  1. Input file with sentences in [CoNLL-2009 one word per line format](http://ufal.mff.cuni.cz/conll2009-st/task-description.html) (tagged and lemmatized)
  1. Java 1.6+, 64bit
  1. Computer with 3GB free memory

**How to parse a file from the command line**

`java -Xmx3G -classpath anna.jar is2.parser.Parser -model <parsing-model> -test <input-file> -out <output-file>`

Please replace the following parts:

  * 

&lt;parsing-model&gt;

 is the model used by the parser to build the dependency tree (see Downloads)
  * 

&lt;input-file&gt;

 is read by the parser and it has to be in [CoNLL-2009 one word per line format](http://ufal.mff.cuni.cz/conll2009-st/task-description.html)
  * 

&lt;output-file&gt;

 is the parsing result and written by the parser
