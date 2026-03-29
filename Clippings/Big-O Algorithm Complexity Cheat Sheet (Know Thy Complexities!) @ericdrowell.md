---
title: "Big-O Algorithm Complexity Cheat Sheet (Know Thy Complexities!) @ericdrowell"
source: "https://www.bigocheatsheet.com/"
author:
published:
created: 2026-03-28
description:
tags:
  - "clippings"
---
## Know Thy Complexities!

Hi there! This webpage covers the space and time Big-O complexities of common algorithms used in Computer Science. When preparing for technical interviews in the past, I found myself spending hours crawling the internet putting together the best, average, and worst case complexities for search and sorting algorithms so that I wouldn't be stumped when asked about them. Over the last few years, I've interviewed at several Silicon Valley startups, and also some bigger companies, like Google, Facebook, Yahoo, LinkedIn, and Uber, and each time that I prepared for an interview, I thought to myself "Why hasn't someone created a nice Big-O cheat sheet?". So, to save all of you fine folks a ton of time, I went ahead and created one. Enjoy! - [Eric](https://twitter.com/ericdrowell)

## Big-O Complexity Chart

| `Horrible` | `Bad` | `Fair` | `Good` | `Excellent` |
| --- | --- | --- | --- | --- |

<svg id="chart" width="800" height="500" xmlns="http://www.w3.org/2000/svg"><path d="M50 450 L 50 0 L 800 0 L 800 450 Z" fill="#ff8989"></path><path d="M50 450 L 800 0 L 800 450 Z" fill="#FFC543"></path><path d="M50 450 L 800 450 L 800 330 Z" fill="yellow"></path><path d="M50 450 L 800 450 L 800 410 Z" fill="#C8EA00"></path><path d="M50 450 L 800 450 L 800 440 Z" fill="#53d000"></path><path d="M50 0 L 50 450 L 800 450" fill="transparent" stroke="black" stroke-width="2"></path><path d="M50 448 L 800 448" fill="transparent" stroke="black" stroke-width="2"></path><text x="700" y="438" fill="black">O(log n), O(1)</text> <path d="M50 450 L 800 400" fill="transparent" stroke="black" stroke-width="2"></path><text x="760" y="390" fill="black">O(n)</text> <path d="M50 450 Q 400 350, 800 150" fill="transparent" stroke="black" stroke-width="2"></path><text x="630" y="190" fill="black">O(n log n)</text> <path d="M50 450 Q 180 380, 250 0" fill="transparent" stroke="black" stroke-width="2"></path><text x="260" y="30" fill="black">O(n^2)</text> <path d="M50 450 C 100 430, 120 350, 120 0" fill="transparent" stroke="black" stroke-width="2"></path><text x="125" y="20" fill="black">O(2^n)</text> <path d="M50 450 C 80 450, 80 350, 80 0" fill="transparent" stroke="black" stroke-width="2"></path><text x="80" y="20" fill="black">O(n!)</text> <text x="0" y="0" transform="translate(30 230) rotate(-90)" style="dominant-baseline: middle; text-anchor: middle; font-size:20px; color: #555; font-size:20px; color: #555; font-style: italic;" fill="black">Operations</text> <text x="0" y="0" transform="translate(420 470)" style="dominant-baseline: middle; text-anchor: middle; font-size:20px; color: #555; font-style: italic;" fill="black">Elements</text></svg>

## Common Data Structure Operations

<table><tbody><tr><th>Data Structure</th><th colspan="8">Time Complexity</th><th>Space Complexity</th></tr><tr><th></th><th colspan="4">Average</th><th colspan="4">Worst</th><th>Worst</th></tr><tr><th></th><th>Access</th><th>Search</th><th>Insertion</th><th>Deletion</th><th>Access</th><th>Search</th><th>Insertion</th><th>Deletion</th><th></th></tr><tr><td><a href="http://en.wikipedia.org/wiki/Array_data_structure">Array</a></td><td><code>Θ(1)</code></td><td><code>Θ(n)</code></td><td><code>Θ(n)</code></td><td><code>Θ(n)</code></td><td><code>O(1)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Stack_(abstract_data_type)">Stack</a></td><td><code>Θ(n)</code></td><td><code>Θ(n)</code></td><td><code>Θ(1)</code></td><td><code>Θ(1)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(1)</code></td><td><code>O(1)</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Queue_(abstract_data_type)">Queue</a></td><td><code>Θ(n)</code></td><td><code>Θ(n)</code></td><td><code>Θ(1)</code></td><td><code>Θ(1)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(1)</code></td><td><code>O(1)</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Singly_linked_list#Singly_linked_lists">Singly-Linked List</a></td><td><code>Θ(n)</code></td><td><code>Θ(n)</code></td><td><code>Θ(1)</code></td><td><code>Θ(1)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(1)</code></td><td><code>O(1)</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Doubly_linked_list">Doubly-Linked List</a></td><td><code>Θ(n)</code></td><td><code>Θ(n)</code></td><td><code>Θ(1)</code></td><td><code>Θ(1)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(1)</code></td><td><code>O(1)</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Skip_list">Skip List</a></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n log(n))</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Hash_table">Hash Table</a></td><td><code>N/A</code></td><td><code>Θ(1)</code></td><td><code>Θ(1)</code></td><td><code>Θ(1)</code></td><td><code>N/A</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Binary_search_tree">Binary Search Tree</a></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td></tr><tr><td><a href="https://en.wikipedia.org/wiki/Cartesian_tree">Cartesian Tree</a></td><td><code>N/A</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>N/A</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/B_tree">B-Tree</a></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Red-black_tree">Red-Black Tree</a></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(n)</code></td></tr><tr><td><a href="https://en.wikipedia.org/wiki/Splay_tree">Splay Tree</a></td><td><code>N/A</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>N/A</code></td><td><code>O(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/AVL_tree">AVL Tree</a></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(log(n))</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/K-d_tree">KD Tree</a></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>Θ(log(n))</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td><td><code>O(n)</code></td></tr></tbody></table>

## Array Sorting Algorithms

<table><tbody><tr><th>Algorithm</th><th colspan="3">Time Complexity</th><th>Space Complexity</th></tr><tr><th></th><th>Best</th><th>Average</th><th>Worst</th><th>Worst</th></tr><tr><td><a href="http://en.wikipedia.org/wiki/Quicksort">Quicksort</a></td><td><code>Ω(n log(n))</code></td><td><code>Θ(n log(n))</code></td><td><code>O(n^2)</code></td><td><code>O(log(n))</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Merge_sort">Mergesort</a></td><td><code>Ω(n log(n))</code></td><td><code>Θ(n log(n))</code></td><td><code>O(n log(n))</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Timsort">Timsort</a></td><td><code>Ω(n)</code></td><td><code>Θ(n log(n))</code></td><td><code>O(n log(n))</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Heapsort">Heapsort</a></td><td><code>Ω(n log(n))</code></td><td><code>Θ(n log(n))</code></td><td><code>O(n log(n))</code></td><td><code>O(1)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Bubble_sort">Bubble Sort</a></td><td><code>Ω(n)</code></td><td><code>Θ(n^2)</code></td><td><code>O(n^2)</code></td><td><code>O(1)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Insertion_sort">Insertion Sort</a></td><td><code>Ω(n)</code></td><td><code>Θ(n^2)</code></td><td><code>O(n^2)</code></td><td><code>O(1)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Selection_sort">Selection Sort</a></td><td><code>Ω(n^2)</code></td><td><code>Θ(n^2)</code></td><td><code>O(n^2)</code></td><td><code>O(1)</code></td></tr><tr><td><a href="https://en.wikipedia.org/wiki/Tree_sort">Tree Sort</a></td><td><code>Ω(n log(n))</code></td><td><code>Θ(n log(n))</code></td><td><code>O(n^2)</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Shellsort">Shell Sort</a></td><td><code>Ω(n log(n))</code></td><td><code>Θ(n(log(n))^2)</code></td><td><code>O(n(log(n))^2)</code></td><td><code>O(1)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Bucket_sort">Bucket Sort</a></td><td><code>Ω(n+k)</code></td><td><code>Θ(n+k)</code></td><td><code>O(n^2)</code></td><td><code>O(n)</code></td></tr><tr><td><a href="http://en.wikipedia.org/wiki/Radix_sort">Radix Sort</a></td><td><code>Ω(nk)</code></td><td><code>Θ(nk)</code></td><td><code>O(nk)</code></td><td><code>O(n+k)</code></td></tr><tr><td><a href="https://en.wikipedia.org/wiki/Counting_sort">Counting Sort</a></td><td><code>Ω(n+k)</code></td><td><code>Θ(n+k)</code></td><td><code>O(n+k)</code></td><td><code>O(k)</code></td></tr><tr><td><a href="https://en.wikipedia.org/wiki/Cubesort">Cubesort</a></td><td><code>Ω(n)</code></td><td><code>Θ(n log(n))</code></td><td><code>O(n log(n))</code></td><td><code>O(n)</code></td></tr></tbody></table>

## Learn More

- [Cracking the Coding Interview: 150 Programming Questions and Solutions](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X/ref=as_li_ss_tl?ie=UTF8&redirect=true&ref_=as_li_tl&linkCode=ll1&tag=bigocheatsheet-1-20&linkId=52f670296578886d22cacce6c054edff)
- [Introduction to Algorithms, 3rd Edition](https://www.amazon.com/Introduction-Algorithms-3rd-MIT-Press/dp/0262033844/ref=as_li_ss_tl?ie=UTF8&redirect=true&ref_=as_li_tl&linkCode=ll1&tag=bigocheatsheet-1-20&linkId=105e776075c7c7a38c9b0581586d1fa5)
- [Data Structures and Algorithms in Java (2nd Edition)](https://www.amazon.com/Data-Structures-Algorithms-Java-2nd/dp/0672324539/ref=as_li_ss_tl?ie=UTF8&redirect=true&ref_=as_li_tl&linkCode=ll1&tag=bigocheatsheet-1-20&linkId=2b0ec7f4eca859cce10f98824db5a73d)
- [High Performance JavaScript (Build Faster Web Application Interfaces)](https://www.amazon.com/Performance-JavaScript-Faster-Application-Interfaces/dp/059680279X/ref=as_li_ss_tl?ie=UTF8&redirect=true&ref_=as_li_tl&linkCode=ll1&tag=bigocheatsheet-1-20&linkId=fbbcd88ba96f0e3341687c8170e31cc2)

## Get the Official Big-O Cheat Sheet Poster

[![](https://www.bigocheatsheet.com/img/big-o-cheat-sheet-poster.png)](http://www.redbubble.com/people/immortalloom/works/22929408-official-big-o-cheat-sheet-poster?p=poster&finish=semi_gloss&size=large "Big-O Cheat Sheet Poster")

## Contributors

1. [Eric Rowell](https://github.com/ericdrowell)
2. [Quentin Pleple](https://github.com/qpleple)
3. [Michael Abed](https://github.com/vault)
4. [Nick Dizazzo](https://github.com/ndizazzo)
5. [Adam Forsyth](https://github.com/agfor)
6. [Felix Zhu](https://github.com/felixzhuologist)
7. [Jay Engineer](https://github.com/jay754)
8. [Josh Davis](https://github.com/jdavis)
9. [Nodir Turakulov](https://github.com/nodirt)
10. [Jennifer Hamon](https://github.com/jhamon)
11. [David Dorfman](https://github.com/d3dave)
12. [Bart Massey](https://github.com/BartMassey)
13. [Ray Pereda](https://github.com/raypereda)
14. [Si Pham](https://github.com/phamtrisi)
15. [Mike Davis](https://github.com/dodgymike)
16. [mcverry](https://github.com/mcverry)
17. [Max Hoffmann](https://github.com/mhoffman)
18. [Bahador Saket](https://github.com/BahadorSaket)
19. [Damon Davison](https://github.com/allolex)
20. [Alvin Wan](https://github.com/alvinwan)
21. [Alan Briolat](https://github.com/alanbriolat)
22. [Drew Hannay](https://github.com/drewhannay)
23. [Andrew Rasmussen](https://github.com/andyras)
24. [Dennis Tsang](https://github.com/DennisTT)
25. [Vinnie Magro](https://github.com/vmagro)
26. [Adam Arold](https://github.com/adam-arold)
27. [Alejandro Ramirez](https://github.com/j4n0)
28. [Aneel Nazareth](https://github.com/WanderingStar)
29. [Rahul Chowdhury](https://github.com/rahulc93)
30. [Jonathan McElroy](https://github.com/jonathanmcelroy)
31. [steven41292](https://github.com/steven41292)
32. [Brandon Amos](https://github.com/bamos)
33. [Joel Friedly](https://github.com/jfriedly)
34. [Casper Van Gheluwe](https://github.com/caspervg)
35. [Eric Lefevre-Ardant](https://github.com/elefevre)
36. [Oleg](https://github.com/cristaloleg)
37. [Renfred Harper](https://github.com/renfredxh)
38. [Piper Chester](https://github.com/piperchester)
39. [Miguel Amigot](https://github.com/mamigot)
40. [Apurva K](https://github.com/paxocap)
41. [Matthew Daronco](https://github.com/mdaronco)
42. [Yun-Cheng Lin](https://github.com/yunchenglin)
43. [Clay Tyler](https://github.com/TylerNakamura)
44. [Orhan Can Ozalp](https://github.com/ocozalp)
45. [Ayman Singh](https://github.com/aymanim)
46. [David Morton](https://github.com/damorton)
47. [Aurelien Ooms](https://github.com/aureooms)
48. [Sebastian Paaske Torholm](https://github.com/Eckankar)
49. [Koushik Krishnan](https://github.com/koek67)
50. [Drew Bailey](https://github.com/makosblade)
51. [Robert Burke](https://github.com/sharpobject)

## Make this Page Better

[Edit these tables!](https://github.com/ericdrowell/BigOCheatSheet/blob/master/Tables.html)