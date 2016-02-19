How do I tag, lemmatize, etc. a text?

# Spliting, Tagging, Morphologic Tagging and Lemmatizing #

The input text has to be tokenized and in one word per line format. For example, the OpenNLP tokenizer could be used to obtain such an input. The input text should looks as:

**input: one-sentence-per-line.txt**

_Airfields have been constructed on a number of the islands ._<br>
Private investment has even made an increasingly modern ferry fleet possible . <br>
Politically , the 1990s have been relatively quite times for the islands . <br>
<i><br>
<h2>From Tokenized one sentence per line format to one-word per line 2009 CoNLL format</h2></i>

The following command maps tokenized text (one-sentence-per-line format) into the input format of the lemmatizer, tagger, etc. The one word per line text format starts with a number followed by a word form, and 13 underscores that are separated by tabs. The sentences are separated by empty lines.<br>
<br>
<pre><code>java -cp anna.jar is2.util.Split one-sentence-per-line.txt &gt; one-word-per-line.txt<br>
</code></pre>

<b>one-word-per-line.txt</b> <br>

<i><br>
1	Airfields	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code></i><br>
2	have	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code> <br>
3	been	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code> <br>
4	constructed	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code> <br>
5	on	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code> <br>
6	a	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code> <br>
7	number	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code> <br>
8	of	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code> <br>
9	the	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code> <br>
10	islands	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code> <br>
11	.	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code> <br>

1	Private	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code> <br>
2	investment	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code>	<code>_</code> <br>
...<br>
<i><br>
<h2>Lemmatizing</h2></i>


<pre><code>java -Xmx2G -cp anna.jar is2.lemmatizer.Lemmatizer -model &lt;lemmatizer.model&gt; -test &lt;input-file-name&gt; -out &lt;output-file-name&gt;<br>
</code></pre>

Example:<br>
<br>
<pre><code>java -Xmx2G -cp anna.jar is2.lemmatizer.Lemmatizer -model  lemma-ger.model -test one-word-per-line.txt -out  lemmatized.txt<br>
</code></pre>


<h2>Tagging</h2>

<pre><code>java -Xmx2G -cp anna.jar is2.tag3.Tagger  -model &lt;tagger.model&gt; -test &lt;input-file-name&gt; -out &lt;output-file-name&gt;<br>
</code></pre>

Example:<br>
<br>
<pre><code>java -Xmx2G -cp anna.jar is2.tag3.Tagger  -model  tag-ger.model -test lemmatized.txt -out  tagged.txt<br>
</code></pre>

<h2>Morphologic Tagging</h2>

input: one-word per line format<br>
<br>
<pre><code>java -Xmx2G -cp anna.jar is2.mtag.Main  -model &lt;morph-tagger.model&gt; -test &lt;input-file-name&gt; -out &lt;output-file-name&gt;<br>
</code></pre>

Example:<br>
<br>
<pre><code>java -Xmx2G -cp anna.jar is2.mtag.Main  -model  mtag-ger.model -test tagged.txt -out  morph-tagged.txt<br>
</code></pre>