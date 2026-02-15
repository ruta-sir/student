---
layout: post
title: AP CSA 2019 FRQ 4
permalink: /csa/frqs/2019/4
comments: True
author: Ruta Sirdeshmukh
---

# Screenshots of Working Coderunner

## Part A

![FRQ Coderunner Working](/student/assets/images/2019frq1_a1.png)

![FRQ Coderunner Working](/student/assets/images/2019frq1_a2.png)

## Part B

![FRQ Coderunner Working](/student/assets/images/2019frq1_b1.png)

![FRQ Coderunner Working](/student/assets/images/2019frq1_b2.png)

---

# Lesson Takeaways

## What I learned overall
- **Probability and randomness:** Utilized `Math.random()` to give each light a 40% probability of being illuminated.
- **Grid iteration:** Employed nested loops to visit every cell in the two-dimensional array.
- **Vertical traversal:** Iterated through a specific column by moving across rows to tally active lights.
- **Rule-based decisions:** Implemented distinct behaviors based on the light's current state (on or off).
- **Mathematical operators:** Leveraged `% 2` and `% 3` to determine evenness and divisibility by three.

---

## Personal Insights
This challenge strengthened my understanding of two-dimensional data structures and how to systematically apply conditional rules. I focused on converting verbal requirements into executable logic while managing row-column relationships and cumulative counts.

### Difficulty Points
- Understanding that column analysis requires iterating through **rows** with a fixed column index.
- Ensuring the light being evaluated was part of its own column count.
- Properly implementing separate logic branches for lights that were on versus off.
- Preventing errors when distinguishing between even numbers and multiples of three.
