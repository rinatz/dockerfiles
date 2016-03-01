# docker-graphillion

This is the Docker image installed [Graphillion].

From [Graphillion] site:

Graphillion is a Python library for efficient *graphset* operations.
Unlike existing graph tools such as [NetworkX], which are designed to
manipulate just a single graph at a time, Graphillion handles a large
*set* of graphs very efficiently.  Surprisingly, trillions of
trillions of graphs can be processed on a single computer with
Graphillion.

You may be curious about an uncommon concept of *graphset*, but it
comes along with any graph or network when you consider multiple
subgraphs cut from the graph; e.g., considering possible driving
routes on a road map, examining feasible electric flows on a power
grid, or evaluating the structure of chemical reaction networks.  The
number of such subgraphs can be trillions even in a graph with just a
few hundreds of edges, since subgraphs increase exponentially with the
graph size.  It takes millions of years to examine all subgraphs with
a naive approach as demonstrated in the fun movie above; Graphillion
is our answer to resolve this issue.

Graphillion allows you to exhaustively but efficiently search a
graphset with complex, even nonconvex, constraints.  In addition, you
can find top-k optimal graphs from the complex graphset, and can also
extract common properties among all graphs in the set.  Thanks to
these features, Graphillion has a variety of applications including
graph database, combinatorial optimization, and a graph structure
analysis.  We will show some practical use cases in the following
[tutorial], including evaluation of power distribution networks.

Graphillion can be used freely under the MIT license.  It is mainly
developed by [JST ERATO Minato project].  We would really appreciate
if you would refer to our paper and address our contribution on the
use of Graphillion in your paper.

> Takeru Inoue, Hiroaki Iwashita, Jun Kawahara, and Shin-ichi Minato:
  "Graphillion: Software Library Designed for Very Large Sets of
  Labeled Graphs," International Journal on Software Tools for
  Technology Transfer, Springer, vol.18, issue 1, pp.57-66, February 2016. ([pdf](http://dx.doi.org/10.1007/s10009-014-0352-z))

Graphillion is still under the development.  We really appreciate any
pull request and patch if you add some changes that benefit a wide
variety of people.

Now, install Graphillion and go to the tutorial.  You'll find its
power and utility.

[Graphillion]: https://github.com/takemaru/graphillion
[NetworkX]: http://networkx.github.io/
[JST ERATO Minato project]: http://www-erato.ist.hokudai.ac.jp/?language=en
[tutorial]: #tutorial
