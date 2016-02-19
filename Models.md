# Introduction #

All our components are data-driven and depend on pre-trained models. This page is meant to give an introduction to the models required by different components, where to get them, possible differences between etc. We are still in the process of training and providing more models for various languages. If you cannot find what you are looking for on this page or in the Downloads section, do not hesitate to send an email and ask.

# Table of contents #


# Models by component #

## Tokenization ##
We have not developed any tokenizers ourselves, but merely rely on other open source implementations. Tokenizers are employed by the SRL system when running the HTTP interface or the complete pipeline from the command line. The binaries of these tokenizers are included in the srl distribution, but the models are not. They will have to be downloaded separately from the corresponding websites.

### English and German tokenizer ###
For English and German, we rely on the [OpenNLP Tools](http://opennlp.sourceforge.net/) tokenizer, version 1.4. The appropriate models are available for download on their website.

### Chinese tokenizer ###
For Chinese, we use the [Stanford Chinese Word Segmenter](http://nlp.stanford.edu/software/segmenter.shtml), version 2008-05-21. The archive available for download on their website contains a number of files, and the model is not one specific file alone. Rather, when invoking the SRL system, the proper file to provide as tokenizer model is the folder called _data_ in the downloaded archive.

## Semantic Role Labeling ##
The SRL models are all zip archives containing several files, most of which are binary (models), but also the feature sets used while training the models. This way it is easy to find out what featuresets were used to train a certain model.

SRL models may or may not contain a reranker. This should be noted where the model is documented/hosted. Any model containing a reranker can be used for pipeline only, but not the other way around.

Depending on size of training corpus and feature sets, the models for the SRL system may get rather big. In the worst case, the sizes exceed the maximum size of 100mb of files that can be put on the Download page here. This is the case for English. See below for links to models hosted elsewhere.


### Chinese SRL ###
A Chinese pipeline only SRL model is available on the Downloads page.

### English SRL ###
The English SRL model is too big to host here. We provide a pipeline only SRL model hosted at http://fileadmin.cs.lth.se/nlp/models/srl/en/srl-20100906/srl-eng.model.