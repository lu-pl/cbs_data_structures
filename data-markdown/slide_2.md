**Arrays** <!-- .element: style="font-size:70px; margin-bottom:1.5em;" -->

<img src="./data-markdown/pics/array_icon.png" width="300">

+++


**General Notes on Arrays** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<ul>
  <li class="fragment">An array is an <em>ordered collection of elements</em></li>
  <li class="fragment">Arrays organize data by holding a collection of elements and making them accessible via an <em>index</em></li>
  <li class="fragment">Arrays can be statically or dynamically <em>typed</em> and statically or dynamically <em>sized</em></li>
</ul>


+++

**Array Index** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<img src="./data-markdown/pics/array_index.png" width="700">

+++

**Python Lists** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<ul>
  <li class="fragment">
	Python has several <em>Sequence</em> types<br>
	(see
	<a href="https://docs.python.org/3/library/stdtypes.html#bltin-types" target="_blank">Built-in Types</a>
	and
	<a href="https://docs.python.org/3/library/collections.abc.html#module-collections.abc" target="_blank">collections.abc</a>)
  </li>
  <li class="fragment">
	Python Lists are a dynamically typed, dynamically sized, mutable sequence type that implements an array interface
  </li>
  <li class="fragment">Python features [...] as a literal syntax for lists

  <pre><code class="language-python">
  l = [1, 2, 3]

  print(l)
  print(l[0])
  </code></pre>

  </li>
</ul>


+++

**Practical** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

- Open the colab sheet and go to the <a href="https://colab.research.google.com/drive/15BVAPh2cuGuV0_whxOIQr09KiUOfca7p#scrollTo=y1avUXmC9CAH">Arrays/Simple Arrays</a> section
- Perform basic index lookup operations on an array of your choice.
  What happens if you try to access an index that is out of bounds?
  What happens if you access a negative index?
- Have a look at the [Python docs for Mutable Sequences](https://docs.python.org/3/library/stdtypes.html#mutable-sequence-types).
  Run some of the operations defined here on an arbitrary list. (See examples in the colab sheet)


+++

**Associative Arrays** <!-- .element: style="font-size:70px; margin-bottom:1.5em;" -->

An associative array is an abstraction over an array type that implements a mapping type through <br> key–value associations. <!-- .element: class="fragment" -->

+++

**Parallel Arrays** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<p style="font-size:30px">A projection of two arrays so that an index in the key array can be used to retrieve the associated value in the value array.</p>

```python
keys = ["a", "b", "c"]
values = [1, 2, 3]

parallel_array = [keys, values]
print(parallel_array)
```

+++

**Association Arrays** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<p style="font-size:30px">An array of two-element arrays where the first element denotes a key and the second element denotes the associated value.</p>

```python
association_array = [
	["a", 1],
	["b", 2],
	["c", 3]
]

print(association_array)
```

+++

**Practical** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<p style="font-size:35px">Take a quick moment to think through the logic for retrieving a value by key in <em>parallel arrays</em> versus in an <em>associative array</em>.</p>
<p style="font-size:35px">How would each approach work?</p>

+++

**Python Dictionaries** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<ul>
  <li class="fragment">A <em>mapping type</em> that associates unique, hashable keys with arbitrary values</li>
  <li class="fragment">Implements efficient key-based <em>lookup, insertion, and deletion</em> using hash tables</li>
	<li class="fragment">Python’s dict is a hash-table-based implementation of an associative array.</li>
</ul>

+++

```python
d = {
	"a": 1,
	"b": 2,
	"c": 3
}

print(d["a"])
```

```python
bibliography = {
	"Ingeborg Bachmann": [
		"Die gestundete Zeit",
		"Anrufung des Großen Bären"
	],
	"Paul Celan": [
		"Mohn und Gedächtnis",
		"Sprachgitter"
	],
}

print(bibliography["Ingeborg Bachmann"])
```


+++

**Practical** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->
- Open the colab sheet and go to the <a href="https://colab.research.google.com/drive/15BVAPh2cuGuV0_whxOIQr09KiUOfca7p#scrollTo=NKI5SHhzubrm&line=1&uniqifier=1">Arrays/Python Dictionaries</a> section
- Tinker with dicts!


+++

**Mappings / Associative Arrays** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

```python
d = {"a": 1, "b": 2, "c": 3}

d.keys()    # dict_keys(['a', 'b', 'c'])
d.values()  # dict_values([1, 2, 3])

d.items()   # dict_items([('a', 1), ('b', 2), ('c', 3)])
```
<!-- .element: class="fragment" -->


+++

**Multi-dimensional Arrays** <!-- .element: style="font-size:70px; margin-bottom:1.5em;" -->

A multi-dimensional array is an array whose elements are themselves arrays, arranged conceptually in multiple dimensions (such as 2-D, 3-D, or more). <!-- .element: class="fragment" -->

+++

<ul>
  <li class="fragment">An element in a multi-array is accessed by providing an <em>array of indices</em> — one per dimension.</li>
  <li class="fragment">Multi-arrays are commonly used to represent grids, matrices, tensors, or higher-dimensional data.</li>
  <br>
  <li class="fragment">A 2-D array can actually be conceived as... <span class="fragment">a table!</span></li>
</ul>

+++

**Pandas DataFrames** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<div style="display: flex; gap: 2em;">
<div style="flex: 2;">

<pre><code class="python">import pandas as pd

data = {
	"a": [1, 2],
	"b": [3, 4],
	"c": [5, 6]
}

df1 = pd.DataFrame(data=data)
</code></pre>

<pre><code class="python">import pandas as pd

data = [(1, 3, 5), (2, 4, 6)]

df2 = pd.DataFrame(
	data=data,
	columns=["a", "b", "c"]
)
</code></pre>
</div>
<div class="fragment" style="flex: 1; border-left: 2px solid #ccc; padding-left: 2em; padding-top: 3em">
<table>
<tr><th></th><th>a</th><th>b</th><th>c</th></tr>
<tr><td>0</td><td>1</td><td>3</td><td>5</td></tr>
<tr><td>1</td><td>2</td><td>4</td><td>6</td></tr>
</table>
</div>
</div>


+++

**Summary Arrays** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<ul>
  <li class="fragment">An array is an ordered collection of elements</li>
  <li class="fragment">Arrays are indexed; elements can be retrieved from an array by looking up an index position</li>
  <li class="fragment">More complex data structures can be built on the basis of arrays: Mappings, Tables, Queues, ...</li>
  <li class="fragment">Typical array operations include: retrieval, sorting, searching, inserting, deleting, ...</li>
  <li class="fragment">Python lists implement an array interface. Technically, arrays are not lists though!</li>
</ul>
