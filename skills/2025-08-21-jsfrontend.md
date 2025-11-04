---
layout: post
title: "Javascript Frontend Basics"
permalink: "/skills/js_frontend"
---

# Skill: Hacks – JavaScript Frontend Basics

## Overview

My JavaScript frontend basics journey demonstrates **comprehensive learning process documentation, new understanding development, and challenge resolution**. This skill showcases **my ability to master fundamental JavaScript concepts, implement frontend functionality, and overcome technical challenges**. Through this process, I learned to **write functional JavaScript code, manipulate DOM elements, handle user interactions, and debug frontend applications**. The progression includes basic syntax mastery, concept application, challenge identification, problem-solving implementation, and advanced technique development.

## Evidence of Completion

Below are screenshots and documentation proving my JavaScript frontend learning process:

### Initial Learning & Concept Exploration
![JS Learning Start](/student/assets/images/learnjs.png)

(This screenshot shows initial JavaScript learning resources and basic concept exploration)

### Code Implementation & Practice
![JS Implementation](/student/assets/images/jsbasic.png)

(I started out by doing extremely basic JS which was using the JS mermaid library to create a flowchart for our process in creating our game and implementing it)

### Challenge Documentation & Problem Solving
![JS Challenges](/student/assets/images/jekyllerror.png)

(This shows documented challenges encountered and problem-solving approaches used)

### Advanced Understanding & Application
```
    class Controller {
        constructor(game, ui) {
            this.game = game;
            this.ui = ui;
        }
        startNewGame() { this.game.newGame(); }
        restart() { this.game.newGame(); }
        handleStockClick() {
            this.game.drawFromStock();
        }
        handleCardClick(cardId) {
            // Try automove from waste/tableau to foundation
            if (this.game.autoMoveToFoundation(cardId)) return;
            // Otherwise no-op (students can extend to smart hints here)
        }
        handleDrop(cardId, targetKind, targetIndex) {
            this.game.tryMoveCardById(cardId, targetKind, targetIndex);
        }
        showMenu() { this.ui.showMenu(); }
        showOver() {
            this.ui.showOver(this.game.score, this.ui.currentTimeStr());
        }
        hint() {
            // Simple hint: tell player the obvious strategies (students can improve)
            alert("Hint: Move Aces to foundations. Uncover face-down tableau cards. Build alternating colors down.");
        }
        undo() {
            // Placeholder for students: push/pop from game.moves and revert
            alert("Undo feature: implement by pushing moves to a stack and reversing them.");
        }
        handleWin() {
            // Called by Game via UI.showWin already; could add fireworks, etc.
        }
    }
```

(This is evidence of advanced JavaScript understanding and sophisticated implementation)

---

**Skill Status:** Completed  

**Mastery Level:** [Update with your self-assessment 1-5]  

**Date Completed:** [Insert completion date]
