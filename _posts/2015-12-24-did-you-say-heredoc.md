---
layout: default
title:  "Did you say HEREDOC ?"
date:   2015-12-24 23:42:00
author: Mehdi FARSI
---

## Did You Say HEREDOC ?

The purpose of this code snippet is to play (by using simple examples) with the HEREDOC syntax in Ruby.

An HEREDOC permits to group a multiline string by scoping it using a spicy syntax

str = <<-EOF
Leonardo: I am the master of the world !
Me: No! you are dead bro..
EOF

By default, an HEREDOC enables `String` interpolation (as double-quoted string)

{% highlight ruby %}
venue = "world"

str = <<-EOF
Leonardo: I am the master of the #{venue} !\n
Me: No! you are dead bro..
EOF

puts str
{% endhighlight %}

Output:

{% highlight ruby %}
?> ruby heredoc.rb
Leonardo: I am the master of the world !

Me: No! you are dead bro..
?> 
{% endhighlight %}

To disable interpolation (as single-quoted string)

{% highlight ruby %}
venue = "world"

str = <<-'EOF'
Leonardo: I am the master of the #{venue} !\n
Me: No! you are dead bro..
EOF

puts str
{% endhighlight %}

Output:

{% highlight ruby %}
?> ruby heredoc.rb
Leonardo: I am the master of the #{venue} !\n
Me: No! you are dead bro..
?> 
{% endhighlight %}

Some text editors understand heredocs and pretty print the string depending on the heredoc flag.<br />
List of common heredoc flags: <<-SQL, <<-HTML, <<-XML, <<-JSON

{% highlight ruby %}
<<-SQL
SELECT id
FROM table
WHERE
clause1 AND
clause2
ORDER BY
id DESC;
SQL
{% endhighlight %}

for further information: [Using heredoc for prettier Ruby code](http://makandracards.com/makandra/1675-using-heredoc-for-prettier-ruby-code)

Voilà !