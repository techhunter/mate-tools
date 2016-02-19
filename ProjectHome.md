## Tools for Natural Language Analysis ##

**Google Code closed its upload section. Hence, you will find newer parsers and models [HERE](https://code.google.com/p/mate-tools/wiki/ParserAndModels).**

The tools provide a pipeline of modules that carry out lemmatization, part-of-speech
tagging, dependency parsing, and semantic role labeling of a sentence. The system’s
two main components draw on improved versions of a state-of-the-art dependency
parser (Bohnet, 2010) and semantic role labeler (Björkelund et al.,2009) developed independently by the authors.  The tools are language independent, provide a very high accuracy and are fast. The dependency parser had the top score for German and English dependency parsing in the CoNLL shared task 2009.

<br><br>
Demos of the system are hosted for English (<a href='http://barbar.cs.lth.se:8081/'>Lund</a>), for German (<a href='http://de.sempar.ims.uni-stuttgart.de/'>Stuttgart</a>) and for Chinese (<a href='http://barbar.cs.lth.se:8091/'>Lund</a>). Information about the usage and training can be found in a  <a href='https://code.google.com/p/mate-tools/downloads/detail?name=shortmanual.pdf&can=2&q=#makechanges'>short manual</a> or in the <a href='http://code.google.com/p/mate-tools/w/list'>wiki</a>. In the Download section, we provide compiled packages and pre-trained models for the tools.<br>
<br>
If you have any questions, feel free to contact Bernd Bohnet or Anders Björkelund.<br>
<br>
<h2>News</h2>

<ul><li><b>New Deep-Syntactic Parser</b> available at: <a href='https://code.google.com/p/deepsyntacticparsing/'>https://code.google.com/p/deepsyntacticparsing/</a></li></ul>

<ul><li><b>Google Code closed its upload section. Hence, we have to provide the parser and models for download in the Wiki <a href='https://code.google.com/p/mate-tools/wiki/ParserAndModels'>HERE</a>.</b>
</li><li>Joint morphologic and syntactic dependency parser is available.</li></ul>

<ul><li>New transition-based parser is available! The parser has a very high accuracy and linear complexity (worst case quadratic) and tags and parses jointly (!). The parser is transition-based and has a graph-based completion model so that it combines the properties of both parser types. See <a href='http://code.google.com/p/mate-tools/wiki/Transition_based_parser'>detailed description</a> and the papers below.</li></ul>

<ul><li>New German parsing model is available <a href='http://code.google.com/p/mate-tools/downloads/list'>(download)</a>, which is based on an improved phrase to dependency conversion developed by Wolfgang Seeker (see reference below for details).</li></ul>

<ul><li>Version 4 of the SRL system is available!</li></ul>

<ul><li>New graph-based parser version - faster, more precise; faster tagger; fasster morphologic tagger and lemmatizer in sync with the provided source code. <br></li></ul>

<h2>References</h2>
Please cite the following paper, if you use the <b>graph-based dependency parser</b><br>

<ul><li>Bernd Bohnet. 2010. <i>Very High Accuracy and Fast Dependency Parsing is not a Contradiction</i>. The 23rd International Conference on Computational Linguistics (COLING 2010), Beijing, China. <br></li></ul>

or if you use the <b>transition-based dependency parser</b>:<br>
<br>
<ul><li>Bernd Bohnet and Joakim Nivre. 2012 <i>A Transition-Based System for Joint Part-of-Speech Tagging and Labeled Non-Projective Dependency Parsing.</i> EMNLP-CoNLL, pages  1455-1465   <a href='http://www.aclweb.org/anthology-new/D/D12/D12-1133.pdf'>[pdf</a>| <a href='http://www.aclweb.org/anthology-new/D/D12/D12-1133.bib'>bib</a>]</li></ul>

<ul><li>Bernd Bohnet  and  Jonas Kuhn. 2012. <i>The Best of BothWorlds -- A Graph-based Completion Model for Transition-based Parsers.</i> Proceedings of the 13th Conference of the European Chapter of the Association for Computational Linguistics (EACL), pages 77--87    <a href='http://www.aclweb.org/anthology-new/E/E12/E12-1009.pdf'>[pdf</a>|<a href='http://www.aclweb.org/anthology/E/E12/E12-1009.bib'>bib</a>]</li></ul>

If you use the <b>semantic role labeler</b>, please cite<br>

<ul><li>Anders Björkelund, Love Hafdell, and Pierre Nugues. <i>Multilingual semantic role labeling.</i> In Proceedings of The Thirteenth Conference on Computational Natural Language Learning (CoNLL-2009), pages 43--48, Boulder, June 4--5 2009. <br></li></ul>

The full pipeline including the http interface is described in<br>
<br>
<ul><li>Anders Björkelund, Bernd Bohnet, Love Hafdell, and Pierre Nugues. <i>A high-performance syntactic and semantic dependency parser.</i> In Coling 2010: Demonstration Volume, pages 33-36, Beijing, August 23-27 2010.</li></ul>

The <b>German parsing model</b> was trained on the dependency conversion (without ellipses) described here:<br>
<br>
<ul><li>Seeker, Wolfgang, and Jonas Kuhn. <i>Making Ellipses Explicit in Dependency Conversion for a German Treebank.</i> In Proceedings of the 8th International Conference on Language Resources and Evaluation, 3132–3139. Istanbul, Turkey: European Language Resources Association (ELRA), 2012. <a href='http://www.lrec-conf.org/proceedings/lrec2012/pdf/235_Paper.pdf'>pdf</a></li></ul>

All German models were trained on the full German Tiger corpus, so you cannot(!) use Tiger to evaluate them.