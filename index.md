---
layout: project_page
permalink: /

title: "DROP: High-Density Relocation-free Order-constrained Parking for Vehicle Fleet"
authors:
    Anonymous Authors
affiliations: Anonymous Institute
    
# paper: https://www.cs.virginia.edu/~robins/Turing_Paper_1936.pdf
# video: https://www.youtube.com/results?search_query=turing+machine
# code: https://github.com/topics/turing-machines
# data: https://huggingface.co/docs/datasets
---

![Overview ><](/static/image/overview.svg)

<!-- Using HTML to center the abstract -->
<div class="columns is-centered has-text-centered">
    <div class="column is-four-fifths">
        <h2>Abstract</h2>
        <div class="content has-text-justified">
In this paper, we present \workname, high-<b>D</b>ensity <b>R</b>elocation-free and schedule-C<b>o</b>nstrained <b>P</b>arking for automated valet parking systems (AVPS). \workname~addresses the challenges in high-density parking when precluding disruptive relocations and scheduled order violations. Each challenge is handled by providing relocation-free parking & exit sequences and identifying schedule-constrained parking allocations, respectively. To generate all valid parking & exit sequences, the relocation-free constraints are formulated as explicit logical conditions. For efficient computations, several techniques were designed such as infeasible layout skipping and adjacency-based recursive search with pruning to accelerate the derivation of these logical expressions. We demonstrate the effectiveness of our framework through computer simulations, showcasing its potential to significantly improve area utilization while respecting relocation-free and operation-order constraints.
        </div>
    </div>
</div>

---


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


# Instance 2: $\texttt{20x16}$

![Unique Layouts for Instances 2 ><](/static/image/unique_topologies_20x16.png)
![Adjacency Graphs for Instances 2 ><](/static/image/adjacency_graphs_all_topologies_20x16.png)
No layouts are skipped.

## All valid sequences

<div class="table-wrapper" markdown="block">


<!-- | Layout 1  | Layout 2  | Layout 3  | Layout 4  | Layout 5  |
| --------- | --------- | --------- | --------- | --------- |
| 3816      | 5760      | 348       | 9382      | 172       |
| Layout 6  | Layout 7  | Layout 8  | Layout 9  | Layout 10 |
| 5475      | 6480      | 159465    | 4320      | 18120     |
| Layout 11 | Layout 12 | Layout 13 | Layout 14 | Layout 15 |
| 2070      | 3418      | 90        | 4500      | 896       |
| Layout 16 | Layout 17 | Layout 18 | Layout 19 | Layout 20 |
| 120       | 6249      | 4214      | 1352      | 6594      |
| Layout 21 | Layout 22 |           |           |           |
| 85        | 896       |           |           |           | -->

|   | Layout 1 | Layout 2 | Layout 3 | Layout 4 | Layout 5 | Layout 6 | Layout 7 | Layout 8 | Layout 9 | Layout 10 | Layout 11 | Layout 12 | Layout 13 | Layout 14 | Layout 15 | Layout 16 | Layout 17 | Layout 18 | Layout 19 | Layout 20 | Layout 21 | Layout 22 |
| :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: |
| $\mid\textit{exitSeqs}_\omega \mid$ | 3816     | 5760     | 348      | **9382**     | 172      | 5475     | 6480     | **159465**   | 4320     | 18120     | 2070      | 3418      | 90        | **4500**      | 896       | 120       | 6249      | 4214      | 1352      | **6594**      | 85        | 896       |

</div>

## Parking allocations

| Operation order $\pi$   | Layout 4 | Layout 8 | Layout 14 | Layout 20 | 
| :-----------------------: | :--------: | :--------: | :--------: | :--------: | 
| $[0,1,2,3,4,5,6,7,8,9]$ | 0        | 0        | 0         | 0         |  
| $[1,2,3,4,5,6,7,8,9,0]$ | 2        | 0        | 0         | 0         | 
| $[2,3,4,5,6,7,8,9,0,1]$ | 4        | 0        | 0         | 0         |  
| $[3,4,5,6,7,8,9,0,1,2]$ | 0        | 0        | 0         | 0         |  
| $[4,5,6,7,8,9,0,1,2,3]$ | 0        | 0        | 0         | 0         |    
| $[5,6,7,8,9,0,1,2,3,4]$ | 0        | 14400    | 0         | 0         |   
| $[6,7,8,9,0,1,2,3,4,5]$ | 0        | 14400    | 0         | 0         |  
| $[7,8,9,0,1,2,3,4,5,6]$ | 92       | 7392     | 0         | 0         |  
| $[8,9,0,1,2,3,4,5,6,7]$ | 112      | 2496     | 32        | 32        | 
| $[9,0,1,2,3,4,5,6,7,8]$ | 82       | 534      | 0         | 44        | 


# Instance 3: $\texttt{20x20}$

![Unique Layouts for Instances 3 ><](/static/image/unique_topologies_20x20.png)
![Adjacency Graphs for Instances 3 ><](/static/image/adjacency_graphs_all_topologies_20x20.png)

30 layouts are analyzed while the 22 layouts are skipped.

## All valid sequences

<div class="table-wrapper" markdown="block">

|                                     | **Layout 1** | **Layout 2** | **Layout 3** | **Layout 4** | **Layout 5** | Layout 6 | **Layout 7** | **Layout 8** | **Layout 9** | **Layout 10** | **Layout 12** | Layout 13 | **Layout 14** | **Layout 15** | Layout 16 | **Layout 18** | **Layout 20** | **Layout 21** | **Layout 22** | **Layout 23** | Layout 24 | **Layout 26** | Layout 28 | **Layout 29** | **Layout 30** | **Layout 31** | Layout 32 | Layout 37 | Layout 39 | Layout 40 |
| :---------------------------------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: |
| $\mid\textit{exitSeqs}_\omega \mid$ | **1061400**  |  **952826**  | **1181608**  | **1811594**  |  **972222**  |  473292  |  **573888**  |  **869010**  |  **201876**  |  **198552**   |  **2250000**  |  794664   | **11214231**  |  **2316420**  |  2234592  |  **1668018**  |  **1117338**  |  **149328**   |  **1152484**  |  **610536**   |   99888   |  **645738**   |   21968   | **390100**    | **733830** | **49128** | 610914 | 6696 | 4676 | 7476 | 

</div>

## Parking allocations

<div class="table-wrapper" markdown="block">

| Operation order $\pi$         | Layout 1 | Layout 2 | Layout 3 | Layout 4 | Layout 5 | Layout 7 | Layout 8 | Layout 9 | Layout 10 | Layout 12 | Layout 14 | Layout 15 | Layout 18 | Layout 20 | Layout 21 | Layout 22 | Layout 23 | Layout 26 | Layout 29 | Layout 30 | Layout 31 |
| :---------------------------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: |
| $[0,1,2,3,4,5,6,7,8,9,10,11]$ | 0        | 0        | 0        | 0        | 0        | 0        | 0        | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0 |
| $[1,2,3,4,5,6,7,8,9,10,11,0]$ | 0        | 16        | 0        | 72       | 0        | 0        | 0        | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0 |
| $[2,3,4,5,6,7,8,9,10,11,0,1]$ | 0        | 28        | 0        | 112      | 0        | 0        | 40       | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0 |
| $[3,4,5,6,7,8,9,10,11,0,1,2]$ | 0        | 0        | 0        | 132      | 132       | 0        | 108      | 0         | 108       | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0 |
| $[4,5,6,7,8,9,10,11,0,1,2,3]$ | 0        | 0        | 0        | 0        | 0        | 384        | 384      | 0         | 48        | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0 |
| $[5,6,7,8,9,10,11,0,1,2,3,4]$ | 0        | 0        | 0        | 0        | 0        | 0        | 0        | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0         | 0 |
| $[6,7,8,9,10,11,0,1,2,3,4,5]$ | 0        | 0        | 16       | 2880     | 0        | 0        | 0        | 0         | 0         | 2880      | 518400    | 8640         | 0         | 0         | 48        | 0         | 0         | 120         | 0         | 0         | 0 |
| $[7,8,9,10,11,0,1,2,3,4,5,6]$ | 0        | 2016     | 32       | 1120      | 0        | 0        | 0        | 0         | 0         | 5760      | 604800    | 16320        | 0         | 2880      | 24        | 1008         | 336         | 0         | 0         | 0         | 0 |
| $[8,9,10,11,0,1,2,3,4,5,6,7]$ | 1536      | 672      | 512      | 8960     | 0        | 48       | 4352      | 48         | 0         | 4512      | 370944    | 12672       | 4608         | 288        | 96         | 2784         | 768         | 0         | 0         | 0         | 0 |
| $[9,10,11,0,1,2,3,4,5,6,7,8]$ | 2232      | 2672      | 3628     | 49400    | 0        | 48       | 5832      | 36         | 0         | 2016      | 156384    | 6840      | 4896         | 360       | 120       | 7932      | 2064         | 0         | 144         | 5184         | 72    |
| $[10,11,0,1,2,3,4,5,6,7,8,9]$ | 1200      | 1156       | 560      | 14400     | 0        | 176      | 4864      | 56         | 0         | 336      | 48672     | 2784       | 1984         | 160        | 40         | 2004      | 264         | 0         | 132        | 2304         | 8 |
| $[11,0,1,2,3,4,5,6,7,8,9,10]$ | 480        | 392       | 64        | 2816      | 0        | 10       | 510      | 4         | 0         | 0       | 10096     | 792        | 252         | 42        | 12         | 280      | 42         | 0         | 16         | 722         |   4      |

</div>