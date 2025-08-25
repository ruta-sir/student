---
layout: base
title: Daily Life
hide: true
permalink: /mermaid/
---

<div class="mermaid">
flowchart TD
    %% Stage 1: Inspiration
    A[Talk to CSP and CSSE<br/>for suggestions] --> |empathy| B[Research previous<br/>solitaire games]
    B --> |research| C[Brainstorm ideas<br/>and possible mechanics]

    %% Stage 2: Planning
    C --> |conceptualize| D[Develop UI wireframes]
    C --> |conceptualize| E[Outline lesson objectives]
    D --> |draft| F[Create design mockups]
    E --> |draft| G[Draft teaching materials]
    F --> |align| H[Match game mechanics<br/>with lesson goals]
    G --> |align| H

    %% Stage 3: Development
    H --> |prototype| I[Build initial game prototype]
    I --> |iteration| J[Internal playtest<br/>by team]
    J --> |feedback| K[Record issues and bugs]
    K --> |fix| L[Refine UI/UX]
    L --> |improve| M[Update prototype version 2]
    M --> |expand| N[Add scoring system<br/>and difficulty levels]

    %% Stage 4: Testing
    N --> |beta test| O[Invite CSP/CSSE<br/>for user testing]
    O --> |observe| P[Collect data on engagement]
    P --> |analyze| Q[Adjust lesson plan<br/>and tutorial]
    Q --> |update| R[Refine mechanics<br/>and visuals]

    %% Stage 5: Polishing
    R --> |integrate| S[Polish final build]
    S --> |final draft| T[Prepare documentation<br/>and teacher notes]
    T --> |package| U[Bundle lesson + game]

    %% Stage 6: Presentation
    U --> |publish| V[Present to target audience]
    V --> |review| W[Gather external evaluation]
    W --> |reflect| X[Write final reflection report]
    X --> |complete| Y[Submit & Conclude<br/>Solitaire Project]

    %% Parallel Enhancements
    B --> |parallel research| Z[Explore accessibility features]
    Z --> |apply| L
    F --> |parallel idea| AA[Design alternate UI themes]
    AA --> |apply| S
    O --> |parallel check| AB[Survey audience<br/>about clarity]
    AB --> |apply| Q

    %% Styling
    style A fill:#ffd1dc,stroke:#333,stroke-width:2px
    style B fill:#d1e0ff,stroke:#333,stroke-width:2px
    style C fill:#c1f0c1,stroke:#333,stroke-width:2px
    style D,E,F,G fill:#f9f9b5,stroke:#333,stroke-width:2px
    style H,I,J,K,L,M,N fill:#e0c1f0,stroke:#333,stroke-width:2px
    style O,P,Q,R fill:#c1f0e9,stroke:#333,stroke-width:2px
    style S,T,U fill:#f9d1a7,stroke:#333,stroke-width:2px
    style V,W,X,Y fill:#d9c1f0,stroke:#333,stroke-width:2px
    style Z,AA,AB fill:#fff0f0,stroke:#333,stroke-width:1.5px,stroke-dasharray: 5 5
</div>

