---
tags:
  - 1033-Data-Sci
---
Standard ***ordinary queries*** have a lot of imprecision:

- Multiple words can mean the same thing
- one can mean two different things
- one word can have multiple spellings
- etc.

Query expansion solves this by reformulating a given [[SQL|query]] to improve its performance.
This is achieved either through:

- [[Query expansion#Dictionary approach|Dictionary or thesaurus]]
- [[Query expansion#Machine learning|Machine learning]]

## Dictionary approach
The dictionary approach can either be done manually through the inclusion of multiple known words, e.g. "organise" and "organize". This is <mark class="hltr-green">simple</mark>, but <mark class="hltr-red">time consuming</mark>.

Usually instead we opt to use computerised dictionary tools to help with this.

## Machine learning
If we have a very large dataset, machine learning is particularly useful. It recognises patterns and trends in data, which can help in many areas. 
In query expansion, machine learning is used to indicate how likely a word is *similar* to another word - essentially a dynamic thesaurus, based on its own training data :0
So if someone queries using "*organize*", the machine learning algorithm knows they might mean "*organise*".