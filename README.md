# scheme-hashtable
An implementation of a hash table written in portable Scheme

## Example
```scheme
(define foo (hash-table '(foo . "foo") '(bar . "bar")))
(hash-table-ref foo 'foo) ;; "foo"
(hash-table-ref foo 'bar) ;; "bar"
(hash-table-set! foo 'bar "baz")
(hash-table-ref foo 'bar) ;; "baz"
```

## API Reference
### Procedure: `(make-hash-table)`
### Procedure: `(make-hash-tableq)`
### Procedure: `(make-hash-tablev)`
Create and return a new hash table using `equal?`, `eq?` or `eqv?` respectively for comparison of keys.
All hash tables are mutable.
### Procedure: `(hash-table? obj)`
Return #t if _obj_ is a hash table.
### Procedure: `(hash-table-equal? obj)`
### Procedure: `(hash-table-eq? obj)`
### Procedure: `(hash-table-eqv? obj)`
Return #t if _obj_ is a hash table using `equal?`, `eq?` or `eqv?` respectively for comparison of keys.
### Procedure: `(hash-table-set! ht key val)`
Set _key_ in the hash table _ht_ to _val_.
### Procedure: `(hash-table-ref ht key)`
Lookup the value of _key_ in the hash table _ht_.
### Procedure: `(hash-table-remove! ht key)`
Remove _key_ from the hash table _ht_.
### Procedure: `(alist->hash-table alist)`
### Procedure: `(alist->hash-tableq alist)`
### Procedure: `(alist->hash-tablev alist)`
Convert the associative list _alist_ to a hash table using `equal?`, `eq?` or `eqv?` respectively for comparison of keys.
### Procedure: `(hash-table pairs ...)`
### Procedure: `(hash-tableq pairs ...)`
### Procedure: `(hash-tablev pairs ...)`
Make a hash table using `equal?`, `eq?` or `eqv?` respectively for comparison of keys, with the key/value pairs in _pairs_.
### Procedure: `(hash-table-aproc ht)`
Get `assoc`, `assq` or `assv` depending on which predicate the hash table _ht_ uses for comparison of keys.
### Procedure: `(hash-table-pred ht)`
Get the predicate the hash table _ht_ uses for comparison of keys.
