# JsLParsing


The Src file contains the javascript code that works s a lisp interpretter written in JS. 

It performs the following oerations.

The interpreter implements the following instructions as primitives:

    (+ z1 z2 ... zn)
    (- z1 z2 ... zn)
    (* z1 z2 ... zn)
    (/ z1 z2 ... zn)
    Returns z1 {+|-|*|/} z2 {+|-|*|/} ... {+|-|*|/} zn.

    (eq s1 s2 ... sn)
    (= s1 s2 ... sn)
    Returns t if the si are all the same object, nil otherwise.

    (< z1 z2 ... zn)
    (> z1 z2 ... zn)
    Returns t if the zi are in ascending or descending order, respectively, or nil otherwise.

    (and s1 s2 ... sn)
    (or s1 s2 ... sn)
    Returns t if the si are all non-nil (and) or if any si is non-nil (or). Evaluates arguments from left to right and stops when the return value is determined.

    (cond (p1 [s1]) (p2 [s2]) ... (pn [sn]))
    Evaluates the pi left to right. When one is found to be non-nil, if the corresponding si exists, it is returned; otherwise, the value of pi itself is returned. If no pi is non-nil, then nil is returned.

    (car s)
    Returns the first element of the list s. If s is not a list, returns nil.

    (cdr s)
    Returns the tail of the list s, i.e. s with its first element removed. If s is not a list, returns nil.

    (cons e s)
    Returns a new list whose car is e and whose cdr is s.

    (atom s)
    Returns t if s is an atom (i.e. not a list), nil otherwise.

    (list s1 s2 ... sn)
    Returns a list whose elements are the (evaluated) si.

    (quote s)
    Returns s uninterpreted.

    (set e s)
    Sets e to the evaluated value of s. The value of e must be a symbol, i.e. [a-z][a-z0-9]*.

    (eval s)
    Evaluates s and returns the result.

    (lambda (a1 a2 ... an) s1 s2 ... sm)
    When used at the head of a list, assigns the next n elements of the list to the symbols ai and then evaluates the si in order, returning the value of sm. 

In addition, the following are defined as composite functions; i.e. they're defined in Lisp itself as functions of the above primitives.

    The standard car and cdr composites cadr, cddr, caar, cddr, cadar, cddar, cdadr, caddr.

    (null s)
    (not s)
    Returns t if s is nil, nil otherwise.

    (equal x y)
    Tests equality, where equality of lists means structural equality, not that they are the same object as with eq.

    (append x y)
    Appends the lists x and y.

    (member e s)
    Returns t if e is in the list s, nil otherwise.

    (last s)
    Returns the last element in the list s.

    (reverse s)
    Returns the list s with the elements in reverse order.

    (remove e s)
    Returns s with all occurences of element e removed.

    (mapcar f s)
    Returns a list resulting from applying the function f to each element of s.

    (apply f s)
    Calls the the function f with argument list s.     

    (len s)
    Returns the number of elements in the list s.

    (flatten s)
    Returns the flattened version of the list s, i.e. a list containing the atoms in s in order. 
