---
layout: page
permalink: /cheatsheet/
---

# Cheat Sheet

We all need three things for efficiently maintaining a faculty homepage;
code highlighting, inline math, and latex-style bibliography.[^1]  This
cheatsheet shows how to do all of these things.

## Math

The site is configure to use [mathjax](https://www.mathjax.org/).  To use
LaTeX, just use it:

Inline equations look like $z$ and $j+1 \approx \log(8\pi)$.

Equation array style

$$ f = ma \label{f}$$

$$
\begin{align}
x &= 7  \\ \label{eq1}
j &= 90
\end{align}
$$

$$ \left[
    \begin{matrix}
    1 & x & x^2 \\
    1 & y & y^2 \\
    1 & z & z^2 \\
    \end{matrix}
    \right]
$$

with referencing $\eqref{eq1}$

## References

Standard citations look like {% cite staton2016semanticslics %} and the
bibliography at the end is how to include the bibliography elements that are
included in the document.  References are maintained in the standard ```.bib```
files we all know and love.

## Code

Highlighting code fragments, should you wish to use them, works well.  If you
want line numbers use this form

{% highlight clojure linenos %}
(let [x y]
  (prn x)
  (observe (normal 1 0) y))
{% endhighlight %}

Code fencing works just as well

```clojure
    (let [x y]
      (prn x)
      (observe (normal 1 0) y))
```


Inline code fragments like this one work too ```(observe (normal 1 0) y)```.

### Bibliography

{% bibliography --cited %}

--------------------------------------

[^1]: Footnotes work this way
