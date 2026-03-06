---
layout: project_page
permalink: /

title: "High-Density Automated Valet Parking with Relocation-Free Sequential Operations"
authors:
    Anonymous Authors
affiliations: Anonymous Institute
    
# paper: https://www.cs.virginia.edu/~robins/Turing_Paper_1936.pdf
# video: https://www.youtube.com/results?search_query=turing+machine
# code: https://github.com/topics/turing-machines
# data: https://huggingface.co/docs/datasets

---

<!-- Using HTML to center the abstract -->
<div class="columns is-centered has-text-centered">
    <div class="column is-four-fifths">
        <h2>Abstract</h2>
        <div class="content has-text-justified">
In this paper, we present DROP, high-<b>D</b>ensity <b>R</b>elocation-free sequential <b>OP</b>erations in automated valet parking. DROP addresses the challenges in high-density parking & vehicle retrieval without relocations. Each challenge is handled by jointly providing area-efficient layouts and relocation-free parking & exit sequences, considering accessibility with relocation-free sequential operations. To generate such sequences, relocation-free constraints are formulated as explicit logical conditions expressed in boolean variables. Recursive search strategies are employed to derive the logical conditions and enumerate relocation-free sequences under sequential constraints. We demonstrate the effectiveness of our framework through extensive simulations, showing its potential to significantly improve area utilization with relocation-free constraints. We also examine its viability on an application problem with prescribed operational order.
        </div>
    </div>
</div>

---

# Concept of DROP

![DROP Concept ><](/static/image/drop-concept.svg)
<p style="font-size:120%; font-style:italic; text-align:center">
"DROP solves trade-off between area utilization and relocation-free exits."
</p>
# Overview of DROP

![Overview ><](/static/image/overview.svg)

<!-- TODO: add contents -->



<!-- ## Background
The paper "On Computable Numbers, with an Application to the Entscheidungsproblem" was published by Alan Turing in 1936. In this groundbreaking paper, Turing introduced the concept of a universal computing machine, now known as the Turing machine.

## Objective
Turing's main objective in this paper was to investigate the notion of computability and its relation to the Entscheidungsproblem (the decision problem), which is concerned with determining whether a given mathematical statement is provable or not. -->


<!-- ## Key Ideas
1. Turing first presented the concept of a "computable number," which refers to a number that can be computed by an algorithm or a definite step-by-step process.
2. He introduced the notion of a Turing machine, an abstract computational device consisting of an infinite tape divided into cells and a read-write head. The machine can read and write symbols on the tape, move the head left or right, and transition between states based on a set of rules.
3. Turing demonstrated that the set of computable numbers is enumerable, meaning it can be listed in a systematic way, even though it is not necessarily countable.
4. He proved the existence of non-computable numbers, which cannot be computed by any Turing machine.
5. Turing showed that the Entscheidungsproblem is undecidable, meaning there is no algorithm that can determine, for any given mathematical statement, whether it is provable or not.

![Turing Machine](/static/image/Turing_machine.png)

*Figure 1: A representation of a Turing Machine. Source: [Wiki](https://en.wikipedia.org/wiki/Turing_machine).*

## Table: Comparison of Computable and Non-Computable Numbers

| Computable Numbers | Non-Computable Numbers |
|-------------------|-----------------------|
| Rational numbers, e.g., 1/2, 3/4 | Transcendental numbers, e.g., π, e |
| Algebraic numbers, e.g., √2, ∛3 | Non-algebraic numbers, e.g., √2 + √3 |
| Numbers with finite decimal representations | Numbers with infinite, non-repeating decimal representations |

He used the concept of a universal Turing machine to prove that the set of computable functions is recursively enumerable, meaning it can be listed by an algorithm. -->

# Experiment Results

- Target Instances: $\texttt{15x12}$, $\texttt{20x16}$, and $\texttt{20x20}$
- Key Results per Instance:
  * Generated unique layouts
  * Adjacency graphs for all unique layouts
  * Number of relocation-free exit sequences
  * Parking-exit sequence pairs (under prescribed operation order $\pi$)
  * Animated example of parkiing and exit sequence pairs (under $\pi$)


Note: The count of relocation-free parking matches the number of relocation-free exit sequences.

<details>
    <summary>
    <h2 style="display: inline-block; margin: 0;">Instance 1: 15x12</h2>
  </summary>
  <div markdown="1">
<!-- ## Instance 1: $\texttt{15x12}$ -->

### Generated Unique Layouts

![Unique Layouts for Instances 1 ><](/static/image/unique_topologies_15x12.png)

Note:
- A gray large rectangular box (and its surroundings): Parking lot (boundary)
- A skyblue-colored rectangles: Parking stalls
- Label on each stall: Stall ID (0-4)

<b>3</b> unique layouts with packing capacity of <b>5</b> vehicles.

### Adjacency Graphs

![Adjacency Graphs for Instances 1 ><](/static/image/adjacency_graphs_all_topologies_15x12.png)

The adjacency graphs for all 3 unique layouts. No layouts skipped in postprocessing.

### The Number of Relocation-Free Exit Sequences

|                                     | Layout 1 | Layout 2 | Layout 3 |
| :---------------------------------: | :------: | :------: | :-------: |
| $\vert\textit{exitSeqs}_\omega \vert$ |    **56**    |    **34**    | 1        |

Note: <b>Bold</b> values indicate layouts with valid parking-exit sequence pairs under $\pi$.

### The Parking-Exit Sequence Pairs with $\pi$

| Operation order $\pi$   | Layout 1 | Layout 2 | Layout 3 |
| :-----------------------: | :--------: | :--------: | :--------: |
| $[0,1,2,3,4]$ | 8        | 2        | 0        |
| $[1,2,3,4,0]$ | 24        | 2        | 0        |
| $[2,3,4,0,1]$ | 48        | 4        | 0        |
| $[3,4,0,1,2]$ | 40        | 12        | 0        |
| $[4,0,1,2,3]$ | 16        | 26       | 0        |

Note: Each cell is the count of parking-exit sequence pairs per layout and operation order $\pi$.

- <b>Layouts 1, 2</b>: Valid pairs for all operational orders ($\pi$)
- Layout 3: No valid pairs identified

### Animated Example of Parking-Exit Sequence Pairs with $\pi$

![Parking-Exit Sequence Pairs for Instance 1 ><](/static/image/pair-example_15x12.gif)


</div>
</details>

<details>
    <summary>
    <h2 style="display: inline-block; margin: 0;">Instance 2: 20x16</h2>
  </summary>
  <div markdown="1">
<!-- ## Instance 2: $\texttt{20x16}$ -->

### Generated Unique Layouts

![Unique Layouts for Instances 2 ><](/static/image/unique_topologies_20x16.png)

Note:
- A gray large rectangular box (and its surroundings): Parking lot (boundary)
- A skyblue-colored rectangles: Parking stalls
- Label on each stall: Stall ID (0-4)

<b>22</b> unique layouts with packing capacity of <b>10</b> vehicles.

### Adjacency Graphs

![Adjacency Graphs for Instances 2 ><](/static/image/adjacency_graphs_all_topologies_20x16.png)

The adjacency graphs for all 22 unique layouts. No layouts skipped in postprocessing.

### The Number of Relocation-Free Exit Sequences

<div class="table-wrapper" markdown="block">

|   | Layout 1 | Layout 2 | Layout 3 | Layout 4 | Layout 5 | Layout 6 | Layout 7 | Layout 8 | Layout 9 | Layout 10 | Layout 11 | Layout 12 | Layout 13 | Layout 14 | Layout 15 | Layout 16 | Layout 17 | Layout 18 | Layout 19 | Layout 20 | Layout 21 | Layout 22 |
| :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: |
| $\vert\textit{exitSeqs}_\omega \vert$ | 3,816     | 5,760     | 348      | **9,382**     | 172      | 5,475     | 6,480     | **159,465**   | 4,320     | 18,120     | 2,070      | 3,418      | 90        | **4,500**      | 896       | 120       | 6,249      | 4,214      | 1,352      | **6,594**      | 85        | 896       |

</div>

Note: <b>Bold</b> values indicate layouts with valid parking-exit sequence pairs under $\pi$.

### The Parking-Exit Sequence Pairs with $\pi$

| Operation order $\pi$   | Layout 4 | Layout 8 | Layout 14 | Layout 20 | 
| :-----------------------: | :--------: | :--------: | :--------: | :--------: | 
| $[0,1,2,3,4,5,6,7,8,9]$ | 0        | 0        | 0         | 0         |  
| $[1,2,3,4,5,6,7,8,9,0]$ | 2        | 0        | 0         | 0         | 
| $[2,3,4,5,6,7,8,9,0,1]$ | 4        | 0        | 0         | 0         |  
| $[3,4,5,6,7,8,9,0,1,2]$ | 0        | 0        | 0         | 0         |  
| $[4,5,6,7,8,9,0,1,2,3]$ | 0        | 0        | 0         | 0         |    
| $[5,6,7,8,9,0,1,2,3,4]$ | 0        | 14,400    | 0         | 0         |   
| $[6,7,8,9,0,1,2,3,4,5]$ | 0        | 14,400    | 0         | 0         |  
| $[7,8,9,0,1,2,3,4,5,6]$ | 92       | 7,392     | 0         | 0         |  
| $[8,9,0,1,2,3,4,5,6,7]$ | 112      | 2,496     | 32        | 32        | 
| $[9,0,1,2,3,4,5,6,7,8]$ | 82       | 534      | 0         | 44        | 

Note: Each cell is the count of parking-exit sequence pairs per layout and operation order $\pi$.

- <b>Layouts 4, 8, 14, 20</b>: Valid pairs for some operational orders ($\pi$)
- The other layouts: No valid pairs identified

### Animated Example of Parking-Exit Sequence Pairs with $\pi$

![Parking-Exit Sequence Pairs for Instance 2 ><](/static/image/pair-example_20x16.gif)

</div>
</details>


<details>
    <summary>
    <h2 style="display: inline-block; margin: 0;">Instance 3: 20x20</h2>
  </summary>
  <div markdown="1">
<!-- ## Instance 3: $\texttt{20x20}$ -->

### Generated Unique Layouts

![Unique Layouts for Instances 3 ><](/static/image/unique_topologies_20x20.png)

Note:
- A gray large rectangular box (and its surroundings): Parking lot (boundary)
- A skyblue-colored rectangles: Parking stalls
- Label on each stall: Stall ID (0-4)

<b>52</b> unique layouts with packing capacity of <b>12</b> vehicles.

### Adjacency Graphs

![Adjacency Graphs for Instances 3 ><](/static/image/adjacency_graphs_all_topologies_20x20.png)

The adjacency graphs for 30 unique layouts. 22 layouts skipped in postprocessing.

### The Number of Relocation-Free Exit Sequences

<div class="table-wrapper" markdown="block">

|                                     | **Layout 1** | **Layout 2** | **Layout 3** | **Layout 4** | **Layout 5** | Layout 6 | **Layout 7** | **Layout 8** | **Layout 9** | **Layout 10** | **Layout 12** | Layout 13 | **Layout 14** | **Layout 15** | Layout 16 | **Layout 18** | **Layout 20** | **Layout 21** | **Layout 22** | **Layout 23** | Layout 24 | **Layout 26** | Layout 28 | **Layout 29** | **Layout 30** | **Layout 31** | Layout 32 | Layout 37 | Layout 39 | Layout 40 |
| :---------------------------------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: |
| $\vert\textit{exitSeqs}_\omega \vert$ | **1,061,400**  |  **952,826**  | **1,181,608**  | **1,811,594**  |  **972,222**  |  473,292  |  **573,888**  |  **869,010**  |  **201,876**  |  **198,552**   |  **2,250,000**  |  794,664   | **11,214,231**  |  **2,316,420**  |  2,234,592  |  **1,668,018**  |  **1,117,338**  |  **149,328**   |  **1,152,484**  |  **610,536**   |   99,888   |  **645,738**   |   21,968   | **390,100**    | **733,830** | **49,128** | 610,914 | 6,696 | 4,676 | 7,476 | 

</div>

Note: <b>Bold</b> values indicate layouts with valid parking-exit sequence pairs under $\pi$.

### The Parking-Exit Sequence Pairs with $\pi$

<div class="table-wrapper" markdown="block">

| Operation order $\pi$         | Layout 1 | Layout 2 | Layout 3 | Layout 4 | Layout 5 | Layout 7 | Layout 8 | Layout 9 | Layout 10 | Layout 12 | Layout 14 | Layout 15 | Layout 18 | Layout 20 | Layout 21 | Layout 22 | Layout 23 | Layout 26 | Layout 29 | Layout 30 | Layout 31 |
| :---------------------------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: |
| $[0,1,2,3,4,5,6,7,8,9,10,11]$ | 0        | 0        | 0        | 0        | 0        | 0        | 0        | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0 |
| $[1,2,3,4,5,6,7,8,9,10,11,0]$ | 0        | 16        | 0        | 72       | 0        | 0        | 0        | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0 |
| $[2,3,4,5,6,7,8,9,10,11,0,1]$ | 0        | 28        | 0        | 112      | 0        | 0        | 40       | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0 |
| $[3,4,5,6,7,8,9,10,11,0,1,2]$ | 0        | 0        | 0        | 132      | 132       | 0        | 108      | 0         | 108       | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0 |
| $[4,5,6,7,8,9,10,11,0,1,2,3]$ | 0        | 0        | 0        | 0        | 0        | 384        | 384      | 0         | 48        | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0 |
| $[5,6,7,8,9,10,11,0,1,2,3,4]$ | 0        | 0        | 0        | 0        | 0        | 0        | 0        | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0 |
| $[6,7,8,9,10,11,0,1,2,3,4,5]$ | 0        | 0        | 16       | 2,880     | 0        | 0        | 0        | 0         | 0         | 2,880      | 518,400    | 8,640         | 0         | 0         | 48        | 0         | 0         | 120         | 0         | 0         | 0 |
| $[7,8,9,10,11,0,1,2,3,4,5,6]$ | 0        | 2,016     | 32       | 1,120      | 0        | 0        | 0        | 0         | 0         | 5,760      | 604,800    | 16,320        | 0         | 2,880      | 24        | 1,008         | 336         | 0         | 0         | 0         | 0 |
| $[8,9,10,11,0,1,2,3,4,5,6,7]$ | 1,536      | 672      | 512      | 8,960     | 0        | 48       | 4,352      | 48         | 0         | 4,512      | 370,944    | 12,672       | 4,608         | 288        | 96         | 2,784         | 768         | 0         | 0         | 0         | 0 |
| $[9,10,11,0,1,2,3,4,5,6,7,8]$ | 2,232      | 2,672      | 3,628     | 49,400    | 0        | 48       | 5,832      | 36         | 0         | 2,016      | 156,384    | 6,840      | 4,896         | 360       | 120       | 7,932      | 2,064         | 0         | 144         | 5,184         | 72    |
| $[10,11,0,1,2,3,4,5,6,7,8,9]$ | 1,200      | 1,156       | 560      | 14,400     | 0        | 176      | 4,864      | 56         | 0         | 336      | 48,672     | 2,784       | 1,984         | 160        | 40         | 2,004      | 264         | 0         | 132        | 2,304         | 8 |
| $[11,0,1,2,3,4,5,6,7,8,9,10]$ | 480        | 392       | 64        | 2,816      | 0        | 10       | 510      | 4         | 0         | 0       | 10,096     | 792        | 252         | 42        | 12         | 280      | 42         | 0         | 16         | 722         |   4      |

</div>

Note: Each cell is the count of parking-exit sequence pairs per layout and operation order $\pi$.

- The layouts reported in the table: Valid pairs for some operational orders ($\pi$)
- The other layouts (not reported in the table): No valid pairs identified

<!-- - <b>Layouts 1, 3, 4, 5, 7, 8, 9, 10, 12, 14, 15, 18, 20, 21, 22, 23, 26, 29, 30, 31</b>: Valid pairs for some operational orders ($\pi$)
- The other layouts: No valid pairs identified -->

### Animated Example of Parking-Exit Sequence Pairs with $\pi$

![Parking-Exit Sequence Pairs for Instance 3 ><](/static/image/pair-example_20x20.gif)


</div>
</details>
