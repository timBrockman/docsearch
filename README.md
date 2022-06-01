# DocSearch
Creates a json search index to allow for ranked search of static sites.
Consists of 2 parts, an indexer that creates an index of terms for each doc and a search interface that compares the search terms to the index.


Should be pretty quick, easily interfaced with any js search form

find reasonable test corpus

## indexer 
Creates index from html files

1. strip html (string-strip-html)
2. porter stemmer (stemmer)
3. term frequency
4. inverse document frequency
5. generate index

## searcher
Uses index file to generate ranked search results
Vector comparison between search terms and index (cosine similarity)
