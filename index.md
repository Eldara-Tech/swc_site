---
title: swarmcli — lightweight Swarm management
layout: default
---

<section class="hero">
  <h2>Manage Swarm clusters faster</h2>
  <p>swarmcli provides a compact set of commands to inspect, list and manage services, nodes, and stacks in Docker Swarm.</p>
  <p><a class="btn btn_gradient" href="/topics/install.html">Get started</a></p>
</section>

<section class="features">
  <article>
    <h3>Quick inspection</h3>
    <p>Commands to quickly show node status, service health, and resource usage.</p>
  </article>
  <article>
    <h3>Lightweight</h3>
    <p>No heavy dependencies — designed to be simple and scriptable.</p>
  </article>
  <article>
    <h3>Extensible</h3>
    <p>Small codebase intended as a working model and learning resource.</p>
  </article>
</section>

<section class="example">
  <h3>Quick example</h3>
  <pre><code>$ swarmctl nodes
ID    HOST    STATUS  AVAIL  MANAGER
1     node1   Ready   Active  Yes
2     node2   Ready   Active  No
</code></pre>
</section>
