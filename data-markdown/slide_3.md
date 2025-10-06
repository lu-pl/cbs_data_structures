**Trees** <!-- .element: style="font-size:70px; margin-bottom:1.5em;" -->

<img src="./data-markdown/pics/tree_icon.png" width="300">

+++

**General Notes on Trees** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<ul>
  <li class="fragment">A tree is composite data structure that consists of nodes connected by links</li>
  <li class="fragment">A tree has a single root node and n <br> parent/child/ancestor/descendant/leaf nodes</li>
  <li class="fragment">A tree is well-formed only if every node has exactly one parent (expcept for the root, which has none)</li>
</ul>

+++

**Tree Terminology** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<!-- <div style="display: flex; gap: 1em"> -->
<div style="display: flex; gap: 1em; margin-bottom: 4em;">
<div style="flex: 2">
<img src="./data-markdown/pics/tree_terminology_1.png">
</div>

<div style="flex: 2">
<img src="./data-markdown/pics/tree_terminology_2.png">
</div>
</div>

+++

**<span class="fragment highlight-blue">Binary</span> <span class="fragment highlight-red">Search</span> Trees (BST)** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<ul>
  <li class="fragment">A Binary Search Tree is an n-ary tree where n = 2; <br>i.e. any node can have 2 links at max -> <br><span style="color:blue">binary relation</span></li>
  <li class="fragment">Values in a BST are allocated according to a <br><span style="color:blue">binary operator</span></li>
  <li class="fragment">These rules of a BST can be used to implement <span style="color:red">efficient search operations</span></li>
</ul>

+++

<img src="./data-markdown/pics/bst.png" width="700">

+++

**JSON** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<ul class="element" style="font-size:50px; margin-bottom:1.5em;">
  <li class="fragment">JavaScript Object Notation</li>
  <li class="fragment">Tree structure based on a mapping type</li>
  <li class="fragment">Simple grammar:
	<pre><code class="bnf">
object  ::= "{" "}" | "{" members "}"
members ::= pair | pair "," members
pair    ::= string ":" value
array   ::= "[" "]" | "[" elements "]"
elements::= value | value "," elements
value   ::= string | number |
			object | array |
			"true" | "false" | "null"
	</code></pre>
  </li>
</ul>



+++

**JSON BST** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->


<div style="display: flex; gap: 2em;">
<div style="flex: 2;">

<pre><code>{
  "value": 6,
  "left": {
	"value": 3,
	"left": {
	  "value": 2,
	  "left": {"value": 1}
	},
	"right": {
	  "value": 5,
	  "left": {"value": 4}
	}
  },
  "right": {
	"value": 8,
	"left": {"value": 7},
	"right": {"value": 9}
  }
}
</code></pre>
</div>

<!-- <div class="fragment" style="flex: 1; border-left: 2px solid #ccc; padding-left: 2em; padding-top: 3em"> -->
<div class="fragment" style="flex: 1; border-left: 2px solid #ccc; padding-left: 4em; padding-top: 2.5em">

<pre><code class="text">
		6
	  /   \
	 3     8
	/ \   / \
   2  5  7  9
  /
 1
  \
   4

</code></pre>

</div>
</div>

+++

**JSON APIs** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->
<ul class="element" style="font-size:50px; margin-bottom:1.5em;">
  <li class="fragment">Application Programming Interface</li>
  <li class="fragment">Information exchange layer for inter- and intra-software communication</li>
  <img class="fragment" src="./data-markdown/pics/api.png">
</ul>

+++

**Practical** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<p style=>Have a look at the PFP API and retrieve a <br>JSON response from it.<p>

- [PFP Project](https://www.oeaw.ac.at/acdh/research/dh-research-infrastructure/activities/modelling-humanities-data/pfp-prosopographical-research-platform-austria)
- [PFP API Docs](https://pfp-api.acdh-ch-dev.oeaw.ac.at/docs)

+++

**XML** <!-- .element: style="font-size:70px; margin-bottom:1.5em;" -->
<ul class="element" style="font-size:50px; margin-bottom:1.5em;">
  <li class="fragment"><span class="fragment highlight-blue">Extensible</span> <span class="fragment highlight-red">Markup Language</span></li>
  <li class="fragment">A <span style="color: red">markup language</span> is a way of encoding text so that, besides the plain text itself, there’s also extra information (“markup”) about the structure, meaning, or presentation of the text</li>
  <li class="fragment"><span style="color: blue">Extensible</span> means that the language can be extended to suit specific needs and domains</li>
</ul>


+++

<img src="./data-markdown/pics/xml.jpg">

+++

**XML Example: BST (1)** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<pre><code class="xml">
<node>
  <value>6</value>
  <left>
	<node>
	  <value>3</value>
	  <left>
		<node>
		  <value>2</value>
		  <left>
			<node>
			  <value>1</value>
			</node>
		  </left>
		</node>
	  </left>
	  <right>
		<node>
		  <value>5</value>
		  <left>
			<node>
			  <value>4</value>
			</node>
		  </left>
		</node>
	  </right>
	</node>
  </left>
  <right>
	<node>
	  <value>8</value>
	  <left>
		<node>
		  <value>7</value>
		</node>
	  </left>
	  <right>
		<node>
		  <value>9</value>
		</node>
	  </right>
	</node>
  </right>
</node>

</code></pre>

+++

**XML Example: BST (2)** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<pre><code class="xml">
<tree>
  <node value="6">
	<left>
	  <node value="3">
		<left>
		  <node value="2">
			<left>
			  <node value="1"/>
			</left>
		  </node>
		</left>
		<right>
		  <node value="5">
			<left>
			  <node value="4"/>
			</left>
		  </node>
		</right>
	  </node>
	</left>
	<right>
	  <node value="8">
		<left>
		  <node value="7"/>
		</left>
		<right>
		  <node value="9"/>
		</right>
	  </node>
	</right>
  </node>
</tree>
</code></pre>

+++

**XML Example: Embedded Markup** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<pre><code class="xml">
<div>
	<p>Lastly, That, upon his solemn oath to observe all the above
	articles, the said man-mountain shall have a daily allowance of
	meat and drink sufficient for the support of
	<choice>
		<sic>1724</sic>
		<corr>1728</corr>
	</choice>
	of our subjects,
	with free access to our royal person, and other marks of our
	<choice>
		<orig>favour</orig>
		<reg>favor</reg>
	</choice>.</p>
</div>
</code></pre>

+++

**TEI** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<ul>
  <li class="fragment"><a href="https://tei-c.org/">Text Encoding Initiative</a></li>
  <li class="fragment">Major effort to provide an infrastructure for developing machine-actionable cultural heritage texts</li>
  <li class="fragment"><a href="https://tei-c.org/release/doc/tei-p5-doc/en/html/index.html">TEI Guidelines</a> define an XML format for text encoding and define and document XML tags and attributes</li>
  <li class="fragment">TEI XML is <em>re-presentational</em> rather than <em>presentational</em> markup</li>
</ul>

+++

**TEI Example (1)** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<pre><code class="xml"><lg type="quatrain" rhyme="abab">
 <l>I wander thro' each charter'd <rhyme label="a">street</rhyme>,</l>
 <l>Near where the charter'd Thames does <rhyme label="b">flow</rhyme>,</l>
 <l>And mark in every face I <rhyme label="a">meet</rhyme>
 </l>
 <l>Marks of weakness, marks of <rhyme label="b">woe</rhyme>.</l>
</lg>
<lg rhyme="abab">
 <l>In every cry of every <rhyme label="a">Man</rhyme>
 </l>
 <l>In every Infant's cry of <rhyme label="b">fear</rhyme>,</l>
 <l>In every voice, in every <rhyme label="a">ban</rhyme>,</l>
 <l>The mind-forg'd manacles I <rhyme label="b">hear</rhyme>.</l>
</lg>
</code></pre>

+++

**TEI Example (2.1)** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->
<pre><code class="xml"><teiHeader>
 <fileDesc>
  <titleStmt>
   <title>
   <!-- title of the resource -->
   </title>
  </titleStmt>
  <publicationStmt>
   <p>
   <!-- Information about distribution of the resource -->
   </p>
  </publicationStmt>
  <sourceDesc>
   <p>
   <!-- Information about source from which the resource derives -->
   </p>
  </sourceDesc>
 </fileDesc>
</teiHeader>
</code></pre>


+++

**TEI Example (2.2)** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<pre><code class="xml"><teiHeader>
 <fileDesc>
  <titleStmt>
   <title>Common sense, a machine-readable transcript</title>
   <author>Paine, Thomas (1737-1809)</author>
   <respStmt>
	<resp>compiled by</resp>
	<name>Jon K Adams</name>
   </respStmt>
  </titleStmt>
  <editionStmt>
   <edition>
	<date>1986</date>
   </edition>
  </editionStmt>
  <publicationStmt>
   <distributor>Oxford Text Archive.</distributor>
   <address>
	<addrLine>Oxford University Computing Services,</addrLine>
	<addrLine>13 Banbury Road,</addrLine>
	<addrLine>Oxford OX2 6RB,</addrLine>
	<addrLine>UK</addrLine>
   </address>
  </publicationStmt>
  <notesStmt>
   <note>Brief notes on the text are in a
	   supplementary file.</note>
  </notesStmt>
  <sourceDesc>
   <biblStruct>
	<monogr>
	 <editor>Foner, Philip S.</editor>
	 <title>The collected writings of Thomas Paine</title>
	 <imprint>
	  <pubPlace>New York</pubPlace>
	  <publisher>Citadel Press</publisher>
	  <date>1945</date>
	 </imprint>
	</monogr>
   </biblStruct>
  </sourceDesc>
 </fileDesc>
 <encodingDesc>
  <samplingDecl>
   <p>Editorial notes in the Foner edition have not
	   been reproduced. </p>
   <p>Blank lines and multiple blank spaces, including paragraph
	   indents, have not been preserved. </p>
  </samplingDecl>
  <editorialDecl>
   <correction status="high"
	method="silent">
	<p>The following errors
		 in the Foner edition have been corrected:
	<list>
	  <item>p. 13 l. 7 cotemporaries contemporaries</item>
	  <item>p. 28 l. 26 [comma] [period]</item>
	  <item>p. 84 l. 4 kin kind</item>
	  <item>p. 95 l. 1 stuggle struggle</item>
	  <item>p. 101 l. 4 certainy certainty</item>
	  <item>p. 167 l. 6 than that</item>
	  <item>p. 209 l. 24 publshed published</item>
	 </list>
	</p>
   </correction>
   <normalization>
	<p>No normalization beyond that performed
		 by Foner, if any. </p>
   </normalization>
   <quotation marks="all">
	<p>All double quotation marks
		 rendered with ", all single quotation marks with
		 apostrophe. </p>
   </quotation>
   <hyphenation eol="none">
	<p>Hyphenated words that appear at the
		 end of the line in the Foner edition have been reformed.</p>
   </hyphenation>
   <stdVals>
	<p>The values of <att>when-iso</att> on the <gi>time</gi>
		 element always end in the format <val>HH:MM</val> or
	<val>HH</val>; i.e., seconds, fractions thereof, and time
		 zone designators are not present.</p>
   </stdVals>
   <interpretation>
	<p>Compound proper names are marked. </p>
	<p>Dates are marked. </p>
	<p>Italics are recorded without interpretation. </p>
   </interpretation>
  </editorialDecl>
  <classDecl>
   <taxonomy xml:id="lcsh">
	<bibl>Library of Congress Subject Headings</bibl>
   </taxonomy>
   <taxonomy xml:id="lc">
	<bibl>Library of Congress Classification</bibl>
   </taxonomy>
  </classDecl>
 </encodingDesc>
 <profileDesc>
  <creation>
   <date>1774</date>
  </creation>
  <langUsage>
   <language ident="en" usage="100">English.</language>
  </langUsage>
  <textClass>
   <keywords scheme="#lcsh">
	<term>Political science</term>
	<term>United States — Politics and government —
		 Revolution, 1775-1783</term>
   </keywords>
   <classCode scheme="#lc">JC 177</classCode>
  </textClass>
 </profileDesc>
 <revisionDesc>
  <change when="1996-01-22" who="#MSM"> finished proofreading </change>
  <change when="1995-10-30" who="#LB"> finished proofreading </change>
  <change notBefore="1995-07-04" who="#RG"> finished data entry at end of term </change>
  <change notAfter="1995-01-01" who="#RG"> began data entry before New Year 1995 </change>
 </revisionDesc>
</teiHeader>
</code></pre>

+++

**Summary Trees** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->


<ul>
  <li class="fragment">A tree is a data structure comprised of nodes connected by links, starting from a single root and branching into child nodes without cycles</li>
  <li class="fragment">JSON and XML are popular data formats that represent data as tree structures</li>
  <li class="fragment">Trees are best suited to represent <em>hierarchical</em> data</li>
</ul>
