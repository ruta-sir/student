---
layout: post
title: AP CSA 2024 FRQ 2 - Scoreboard Class
permalink: /csa/frqs/2024/2
comments: True
author: Ruta Sirdeshmukh
---

# Screenshots of Working Coderunner
![FRQ Coderunner Working](/student/assets/images/2024frq2_1.png)
![FRQ Coderunner Working](/student/assets/images/2024frq2_2.png)
![FRQ Coderunner Working](/student/assets/images/2024frq2_3.png)
![FRQ Coderunner Working](/student/assets/images/2024frq2_4.png)
![FRQ Coderunner Working](/student/assets/images/2024frq2_5.png)


```java

// CODE_RUNNER: Create Your Own Scoreboard Class

// Create the Scoreboard Class HERE

class Scoreboard {
    // Define your properties HERE
    private String team1Name;
    private String team2Name;
    private int team1Score;
    private int team2Score;
    private String activeTeam;

    public Scoreboard(String team1Name, String team2Name) {
        // This is your CONSTRUCTOR
        // Initialize your properties HERE (team names and active team)
        this.team1Name = team1Name;
        this.team2Name = team2Name;
        this.team1Score = 0;
        this.team2Score = 0;
        this.activeTeam = team1Name;
    }

    public void recordPlay(int points) {
        // Create the recordPlay Method HERE
        if (activeTeam.equals(team1Name)) {
            team1Score += points;
            activeTeam = team2Name;
        } else {
            team2Score += points;
            activeTeam = team1Name;
        }
    }

    public String getScore() {
        // Create the getScore Method HERE

        return team1Score + "-" + team2Score + "-" + activeTeam; // Modify this return statement to return the actual score with the given format
    }
}

// Testing the Scoreboard class (DO NOT MODIFY this part unless you change the class, method, or constructer names)
// DO NOT MODIFY BELOW THIS LINE
class Main {
    public static void main(String[] args) {
        String info;

        // Step 1: Create a new Scoreboard for "Red" vs "Blue"
        Scoreboard game = new Scoreboard("Red", "Blue");

        // Step 2
        info = game.getScore();                  // "0-0-Red"
        System.out.println("(Step 2) info = " + info);

        // Step 3
        game.recordPlay(1);

        // Step 4
        info = game.getScore();                  // "1-0-Red"
        System.out.println("(Step 4) info = " + info);

        // Step 5
        game.recordPlay(0);

        // Step 6
        info = game.getScore();                  // "1-0-Blue"
        System.out.println("(Step 6) info = " + info);

        // Step 7 (repeated call to show no change)
        info = game.getScore();                  // still "1-0-Blue"
        System.out.println("(Step 7) info = " + info);

        // Step 8
        game.recordPlay(3);

        // Step 9
        info = game.getScore();                  // "1-3-Blue"
        System.out.println("(Step 9) info = " + info);

        // Step 10
        game.recordPlay(1);

        // Step 11
        game.recordPlay(0);

        // Step 12
        info = game.getScore();                  // "1-4-Red"
        System.out.println("(Step 12) info = " + info);

        // Step 13
        game.recordPlay(0);

        // Step 14
        game.recordPlay(4);

        // Step 15
        game.recordPlay(0);

        // Step 16
        info = game.getScore();                  // "1-8-Red"
        System.out.println("(Step 16) info = " + info);

        // Step 17: Create an independent Scoreboard
        Scoreboard match = new Scoreboard("Lions", "Tigers");

        // Step 18
        info = match.getScore();                 // "0-0-Lions"
        System.out.println("(Step 18) match info = " + info);

        // Step 19: Verify the original game is unchanged
        info = game.getScore();                  // "1-8-Red"
        System.out.println("(Step 19) game info = " + info);
    }
}

Main.main(null);

```

# Lesson Takeaways

## What I learned overall

I learned that the most important thing was recognizing that the `points` parameter serves two purposes. It's both a score value and a control signal. Reading the specs carefully and tracing examples manually prevented any possible logical errors when implementing it.

## Challenges I faced

The main issue I faced was understanding `recordPlay` and how it does both scoring and turn management based on a single parameter. I learned that `points = 0` doesn't mean no action but it means "failed play, switch teams". This required careful attention to the problem statement.

## What I did

I broke down the requirements into basic tracking requirements. These included two team names (immutable), two scores (mutable), and the active team indicator. I found it easiest to use an integer (`activeTeam = 1` or `2`) so I could represent which team is active. Essentially it directly corresponds to team1 vs team2 when updating scores.

The specific `recordPlay` logic breaks down cleanly as shown below
* Points > 0  means add to active team's score, maintain possession
* Points = 0 means no scoring, toggle to other team

For `getScore`, I used conditional logic to map the `activeTeam` integer back to the actual team name before formatting the output string.

## How my approach helped me 

* started by implementing the constructor and `getScore()` first to make sure it was functional on a basic level
* used `this.` keyword in the constructor to distinguish parameters from any instance variables