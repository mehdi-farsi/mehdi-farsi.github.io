---
layout: default
title:  "Demystify Bitwise Operators"
date:   2015-11-29 23:42:00
author: Mehdi FARSI
---

##Demystify Bitwise Operators


The goal of this code snippet is to play (using as simple as possible examples) with bitwise operators in `Ruby`.

The method [`Fixnum#to_s`](http://ruby-doc.org/core-2.2.0/Fixnum.html#method-i-to_s) takes an argument which define the base of the displayed Integer.

```ruby
3.to_s(2) # => "00000011"
```

This is helpful for displaying the result of the bitwise operations in `base 2`.

```ruby
8.to_s(2)         # => "00001000"
6.to_s(2)         # => "00000110"
2.to_s(2)         # => "00000010"
1.to_s(2)         # => "00000001"

(2 & 1).to_s(2)   # => "00000000" because it applies an AND operation on each bit. (1 & 1) match
(2 | 1).to_s(2)   # => "00000011" because it applies an OR  operation on each bit. (1 | 1), (1 | 0), (0 | 1) match !
(6 ^ 2).to_s(2)   # => "00000100" because it applies a XOR operation on each bit.  (1 | 0), (0 | 1) match !
(8 >> 2).to_s(2)  # => "00000010" right-shift operator. Each bit is shifted 2 bits to the right.
(2 << 2).to_s(2)  # => "00001000" left-shift operator.  Each bit is shifted 2 bits to the left.
```

I'm pretty sure that after few minutes and a little headache, this will be pretty obvious for you !

