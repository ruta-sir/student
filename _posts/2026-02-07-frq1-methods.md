---
layout: post
title: AP CSA 2024 FRQ 1 - Methods
permalink: /csa/frqs/2024/1
comments: True
author: Ruta Sirdeshmukh
---

# Screenshots of Working Coderunner

## Part A

![FRQ Coderunner Working](/student/assets/images/2024frq1_a1.png)

![FRQ Coderunner Working](/student/assets/images/2024frq1_a2.png)

![FRQ Coderunner Working](/student/assets/images/2024frq1_a3.png)

![FRQ Coderunner Working](/student/assets/images/2024frq1_a4.png)

![FRQ Coderunner Working](/student/assets/images/2024frq1_a5.png)

## Part B

![FRQ Coderunner Working](/student/assets/images/2024frq1_b1.png)

![FRQ Coderunner Working](/student/assets/images/2024frq1_b2.png)

![FRQ Coderunner Working](/student/assets/images/2024frq1_b3.png)

![FRQ Coderunner Working](/student/assets/images/2024frq1_b4.png)

---

# Actual Code
```java
/**
 * Returns the number of days birds or a bear found food to eat at the feeder
 * in this simulation, as described in part (b)
 * Preconditions: numBirds > 0, numDays > 0
 */
class Feeder
{
    int currentFood;  // instance variable
    
    // Minimal simulateOneDay so code compiles and runs
    public void simulateOneDay(int numBirds)
    {
        int foodEaten = numBirds * 10;
        currentFood = Math.max(0, currentFood - foodEaten);
    }
    
    public int simulateManyDays(int numBirds, int numDays)
    {
        int daysWithFood = 0;
        
        for (int day = 0; day < numDays; day++)
        {
            if (currentFood == 0)
            {
                break;
            }
            daysWithFood++;
            simulateOneDay(numBirds);
        }
        
        return daysWithFood;
    }
    /* There may be instance variables, constructors, and methods that are not shown. */
}

public class Main
{
    public static void main(String[] args)
    {
        Feeder feeder = new Feeder();
        feeder.currentFood = 50;   // starting food
        int result = feeder.simulateManyDays(2, 10);
        System.out.println(result); // Expected output: 3
    }
}
```

---

# Lesson Takeaways

## What I learned overall

I learned that simulating multiple days requires careful attention to when conditions are checked versus when actions are taken. The key insight was understanding that we count a day only if food is available at the START of that day, before any birds or bears arrive.

## Challenges I faced

The main challenge was understanding the correct order of operations in the loop. Should we check for food, then simulate, then count? Or check, count, then simulate? The specification clarified that we count days where "birds or a bear found food," meaning food must exist before the day begins.

## What I did

I broke down the requirements into three core steps:
1. **Initialize a counter** - `daysWithFood = 0` to track successful days
2. **Loop through potential days** - Use a for loop up to `numDays`
3. **Check-Count-Simulate pattern** - Before each day, check if food exists (`currentFood > 0`). If yes, count the day and call `simulateOneDay(numBirds)`. If no, break early.

The key logic:
* If `currentFood == 0` at the start of a day → break (no food means simulation ends)
* Otherwise → increment counter, then simulate the day
* After the loop → return the total count

## How my approach helped me

* Started by understanding what "days with food" meant - days where visitors could find food at arrival
* Recognized that `simulateOneDay()` must be called as specified to receive full credit
* Used early termination (`break`) to avoid unnecessary iterations once the feeder is empty
* Traced through the example manually (50 grams, 2 birds, 10g each) to verify the logic produces the expected output of 3 days