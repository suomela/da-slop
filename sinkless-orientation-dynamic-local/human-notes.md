# Sinkless orientation in dynamic-LOCAL

(Notes by Jukka Suomela)

Here is the algorithm the way I'd explain it. Let T ≈ locality of your det-online-LOCAL algorithm A. The dyn-LOCAL algorithm A' works like this:

- Let X = "escapes" = nodes of degree less than 3.
- Let C = "committed" = nodes more than T hops away from X.

We handle edge insertions like this:

- Update X and C as appropriate.
- For each node v that joined C, invoke the online-LOCAL algorithm A to T-neighborhood of v. This is fully known and finalized. And the incident edges of the committed nodes will be never touched, committed nodes won't become sinks, we don't need to worry about them.
- Then consider a node v that is still problematic. That is, it is not yet committed, and it is no longer an escape, and it is a sink. How could this happen? Something must have changed next to v, so either there was an edge addition or there was a fresh commitment next to it, so v is within distance ≤ T from the original point of edge addition. Now because v is not committed, there is still an escape u in X within distance ≤ T of v. In this case we can eliminate the sink locally by orienting edges from v towards u. A key observation is that all nodes on the short path from v to u are also uncommitted, since they are close to u, and hence this operation does not interfere with the committed nodes.

And that's it. Repairs reach up to distance ≈ 2T from the point of addition.

[This assumed we have max degree 3. If not, we can do the obvious local tweaks to handle it. For example, a node of degree 5 is split in nodes of degree 3 and 2, etc.]
