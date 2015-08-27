---
layout: default
title:  "Extract email from string using REGEX"
date:   2015-08-22 08:43:59
author: Mehdi FARSI
---

## Extract email from string using REGEX


The goal of this code snippet isn't to make an email validator.

So the REGEX is not steady but works for the most common cases.

```ruby
line = "Congratulation ! here is your email : mehdi-farsi@long-and_boring-company_name.com. Are you happy ?"
email = line[/(\w|[\.\-])+@(\w|[\.\-])+\.[a-zA-Z]+/]
```

You can extract whatever you want by changing the Regex. :)
