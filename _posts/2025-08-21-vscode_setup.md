---
layout: post
title: "VSCode-Setup.md"
permalink: "/skills/vscode_setup"
---
## 2. `VSCode-Setup.md`

```markdown
# VSCode Setup & Usage

```js
const vscodeSetup = {
  mastered: false,
  rank: 0,
  masteryScore: "0%",
  notesEvidence: `
    Show iterative improvement from basic setup 
    to advanced debugging workflows.
    --> INSERT YOUR LINKS/EVIDENCE HERE <--
  `
};

function updateSkill(skill, mastered, rank, notes) {
  skill.mastered = mastered;
  skill.rank = rank;
  skill.masteryScore = `${(rank / 5) * 100}%`;
  skill.notesEvidence = notes;
}

console.log(vscodeSetup);

flowchart TD
    A[Install VSCode] --> B[Configure settings + extensions]
    B --> C[Test simple program]
    C --> D[Add debugging workflow]
    D --> E[Insert Evidence: repo link, screenshots]
    E --> F[Skill Mastered?]
    F -->|Yes| G[Mark Mastered ✅]
    F -->|No| H[Improve setup 🔄]
