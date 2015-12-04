---
layout: default
title:  "Case statement Behind The Scene"
date:   2015-12-04 23:42:00
author: Mehdi FARSI
---

Case statement Behind The Scene
======================

### Syntax

A `case` statement consists of an optional condition followed by zero or more `when` conditions.
It returns the value of the first truthy `when` statement. Otherwise `nil`.

```ruby
str = case "match"
when "match" then "I match !"
end

# => str = "I match !"
```

```ruby
str = case "lolcat"
when "not match" then "lolcat"
end

# => str = nil
```

### Determine case equality

Case equality is determined by the `===` (threequal) operator.
The left operand is always the statement of the `when` clause.

```ruby
case "lolcat"
when String then "I'm a String"
when Fixnum then "I'm a Fixnum"
when Range  then "I'm a Range"
end
```

Equivalent to:

```ruby
if String === "lolcat"
  "I'm a String"
elsif Fixnum === "lolcat"
  "I'm a Fixnum"
elsif Range === "lolcat"
  "I'm a Range"
end
```

### Multiple statements

The `when` clause accepts multiple statements.

```ruby
case "lolcat"
when String, "I'm a string" then true
end
```

Equivalent to:

```ruby
if String === "lolcat" or "I'm a string" === "lolcat"
  true
end
```

Each statement is separated by an `or` operator.

Voilà !

##### Related Links

[http://ruby-doc.org/docs/keywords/1.9/Object.html#method-i-case](http://ruby-doc.org/docs/keywords/1.9/Object.html#method-i-case)