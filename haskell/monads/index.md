---
title: "Monads"
nav_order: 1
parent: "Haskell"
has_children: false
has_toc: true
---

# Monads

After having understood monads, I don't get why there's so much tiptoeing around what they are.
Ultimately, monads are a pattern we use to compose functions.
If a computer scientist named them, they'd probably call it the "compositional pattern", but it's much deeper than that.
Obviously, being derived from mathematics and category theory, it's a more abstract idea, and it's nice to understand the phrase "Monads are Monoids in the category of endofunctors".
There's a good [article](https://garlandus.co/OfGroupsAndMonads.html) about why you should learn mathematics in the context of programming, but it's not necessary to understand group theory or category theory to apply monads in your code.

The actual pattern involves 3 things: a type, a bind function, and an identity. 
We know what types are, `String`s, `Int`s, etc., which in the context of Monads are our "monadic types", and the bind function / identity will be discussed in the next sections.