# DocSearch
DocSearch consists of 2 parts, an indexer that creates an index of terms for each document in the corpus, and a search interface that compares the search terms to the index. The index uses tf-idf values as a vector for each document, and compares that to the search terms.


Should be pretty quick, easily interfaced with any js search form

find reasonable test corpus

## indexer 
Creates index from html files

1. strip html (string-strip-html)
2. index all words for doc and corpus
3. porter stemmer (stemmer)
4. term frequency
5. inverse document frequency
6. generate index

## searcher
- Uses index file to generate ranked search results
- Vector comparison between search terms and index (cosine similarity)
- The same process used in indexing the corpus must be used here too, like stemming or removing punctuation
