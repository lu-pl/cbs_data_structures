**Graphs** <!-- .element: style="font-size:70px; margin-bottom:1.5em;" -->

<img src="./data-markdown/pics/graph_icon.png" width="300">

+++

**General Notes on Graphs** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<ul>
  <li class="fragment">Graphs are comprised of nodes (vertices) connected by links (edges)</li>
  <li class="fragment">Graphs are a generalization of trees. <br>Trees are a type of graph.</li>
  <li class="fragment">Trees are <em>simple</em>, <em>undirected</em>, <em>acyclic</em> graphs.</li>
</ul>

+++

**Simple Graphs vs. Multigraphs** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<img src="./data-markdown/pics/simple_multi_graph.png">

+++

**Directed Graphs vs. Undirected Graphs** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<img src="./data-markdown/pics/directed_undirected_graphs.png" height="500em">

+++

**Cyclic Graphs vs. Acyclic Graphs** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<img src="./data-markdown/pics/cyclic_acyclic_graphs.png">


+++

<img src="./data-markdown/pics/tree_not_a_tree.png">

+++

**Knowledge Representation / Knowledge Graphs** <!-- .element: style="font-size:40px; margin-bottom:1.5em;" -->

<ul style="font-size: 0.8em;">
  <li class="fragment">
  <strong>Formal Knowledge Representation</strong>: Enable computational interpretations of concepts and relationships and perform automated reasoning over data.
  </li>
  
  <li class="fragment">
  <strong>Facts and Rules</strong> allow inference mechanism to derive new knowledge from existing data.
  </li>
  
  <br>

  <li class="fragment">
  <strong>Knowledge Graphs</strong> are one realization of formal knowledge representation, representing knowledge as a network of entities and relations.
  </li>
  <li class="fragment">
  <em>Knowledge Graphs are a graph-based approach to formal knowledge representation.</em>
  </li>
</ul>

+++

**RDF Knowledge Graphs** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<ul style="font-size: 0.8em;">
  <li class="fragment"><strong>RDF</strong> - Resource Description Framework</li>

  <li class="fragment">Semantic Triples: <strong>Subject – Predicate – Object</strong>
   <img src="./data-markdown/pics/triple.svg"
		 alt="Basic RDF Graph" style="max-width: 60%; margin-top: 0.5em;">
  </li>

  <li class="fragment">Directed Multigraph with labelled edges</li>
</ul>


+++

**Example RDF Graph (1)** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<img src="./data-markdown/pics/rdf_graph_beatles.png">

+++

**Example RDF Graph (2)** <!-- .element: style="font-size:50px; margin-bottom:0.0em;" -->

<img src="./data-markdown/pics/rdf_graph_example.png" height="550">

+++

**Ontologies** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<ul>
  <li class="fragment">
  Ontologies define the vocabulary of a KG: <br/>
  <ul>
        <li>Classes (types of entities),</li>
        <li>Properties (types of relations), and</li>
        <li>Axioms (rules and constraints).</li>
  </ul>
  </li>
  
  <li class="fragment">
  <em>Ontologies define what kinds of things exist in a domain and how they relate.</em>
  </li>
  
  <li class="fragment">
      OWL (Web Ontology Language) is a W3C standard for expressing formal ontologies.
  </li>
  
</ul>

+++

**Example Ontology** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

```ttl
@prefix ex:  <http://example.org/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:<http://www.w3.org/2000/01/rdf-schema#> .
@prefix owl: <http://www.w3.org/2002/07/owl#> .

ex:Person a owl:Class .

ex:isRelated a owl:ObjectProperty ,
               owl:TransitiveProperty ;
    rdfs:domain ex:Person ;
    rdfs:range  ex:Person .
```

+++

**CIDOC CRM** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

[CIDOC Conceptual Reference Model](https://cidoc-crm.org/)

<img src="./data-markdown/pics/crm_spatio_temporal.png">

+++

**Summary Graphs** <!-- .element: style="font-size:50px; margin-bottom:1.5em;" -->

<ul>
  <li class="fragment">Graphs represent relationships between entities as nodes and edges</li>
  <li class="fragment">Graphs enable linking, querying, and reasoning across interconnected data.</li>
  <li class="fragment">Graphs are well-suited for networked data (social connections, inter- and intratextual relationships, or linked datasets)</li>
  <li class="fragment">CIDOC CRM and CRM-compatible models are used to capture humanities domain knowledge</li>
</ul>
