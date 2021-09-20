
# Table of Contents

-   [Agents and environments](#org9b8fb0e)
    -   [Microworld-view](#org83d1c75)
    -   [Rational agent success](#org858089e)
    -   [Example: Vacuum-cleaner](#org53b94aa)
    -   [Definition of a rational agent](#org94979d4)
    -   [Process view](#org7d51bb4)
-   [References](#org4e610ef)



<a id="org9b8fb0e"></a>

# Agents and environments


<a id="org83d1c75"></a>

## Microworld-view

AIMA: agent-world vs. environment view

![img](./img/agents.png)


<a id="org858089e"></a>

## Rational agent success

Success of a rational agent in this simple picture depends on:

1.  the performance measure that defines success
2.  the agent's knowledge of the environment
3.  the actions that the agent can perform
4.  the agent's percept sequence to date


<a id="org53b94aa"></a>

## Example: Vacuum-cleaner

The microworld of the vacuum cleaner has a known boundary, and it
is divided in subspaces that the agent can navigate. In each
subspace, there is an unspecified amount of dirt. The overall
mission is to clean the space.

![img](./img/vacuum.png)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">ASPECT</th>
<th scope="col" class="org-left">EXAMPLE</th>
<th scope="col" class="org-left">FUNCTIONS</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Performance</td>
<td class="org-left">Award cleanliness</td>
<td class="org-left">Maximize</td>
</tr>


<tr>
<td class="org-left">Environment</td>
<td class="org-left">Spatial dimensions</td>
<td class="org-left">Minimize</td>
</tr>


<tr>
<td class="org-left">Actions</td>
<td class="org-left">Movements + sucking</td>
<td class="org-left">Table</td>
</tr>


<tr>
<td class="org-left">Perceptions</td>
<td class="org-left">Location + dirt</td>
<td class="org-left">Table</td>
</tr>
</tbody>
</table>

Can such a simple agent behave irrationally, too?


<a id="org94979d4"></a>

## Definition of a rational agent

> "For each possible percept sequence, a rational agent should select
> an action that is expected to maximize its performance measure,
> given the evidence provided by the percept sequence and whatever
> built-in knowledge the agent has." ([AIMA](#org19baab9))


<a id="org7d51bb4"></a>

## Process view

Modified process modeling view (BPMN diagram):

![img](./img/agents_and_environments.png)


<a id="org4e610ef"></a>

# References

<a id="org19baab9"></a> Norvig P/Russell S (2021). AI - A Modern Approach (4th ed). Pearson.

