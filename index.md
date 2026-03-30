---
<<<<<<< HEAD
layout: default
title: Featured Projects
=======
layout: post 
title: Portfolio Home 
hide: true
show_reading_time: false
>>>>>>> upstream/main
---

<style>
body {
  background-color: #1a1a1a;
  color: #f0f0f0;
  font-family: 'Segoe UI', sans-serif;
  line-height: 1.6;
  margin: 0;
  padding: 0;
}

.page-wrapper {
  max-width: 1000px;
  margin: 0 auto;
  padding: 40px 20px;
}

h2 {
  color: #f0f0f0;
  border-bottom: 3px solid #667eea;
  padding-bottom: 10px;
  margin-bottom: 25px;
  font-size: 2rem;
  text-align: center;
}

<<<<<<< HEAD
.featured-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  max-width: 900px;
  margin: 0 auto 40px auto;
}

@media (max-width: 800px) {
  .featured-grid {
    grid-template-columns: 1fr;
    justify-items: center;
  }
}

.project-card {
  text-decoration: none;
  transform: translateY(0);
  transition: transform 0.3s ease;
}

.project-card:hover {
  transform: translateY(-5px);
}

.project-content {
  padding: 25px;
  border-radius: 12px;
  color: white;
  text-align: center;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
}
</style>

<div class="page-wrapper">
  <!-- Featured Projects Section -->
  <h2>Featured Projects</h2>

  <div class="featured-grid">
    <a href="{{site.baseurl}}/skills-portfolio" class="project-card">
      <div class="project-content" style="background: linear-gradient(135deg, #667eea, #764ba2);">
        <h3 style="margin: 0 0 10px 0; font-size: 1.3rem;">Skills Portfolio</h3>
        <p style="margin: 0; opacity: 0.9; font-size: 0.95rem;">Showcase of my coding abilities and projects</p>
      </div>
    </a>
    
    <a href="{{site.baseurl}}/trireview" class="project-card">
      <div class="project-content" style="background: linear-gradient(135deg, #ff9a9e, #fad0c4);">
        <h3 style="margin: 0 0 10px 0; font-size: 1.3rem;">Trimester 1 Review</h3>
        <p style="margin: 0; opacity: 0.9; font-size: 0.95rem;">Reflection, highlights, and analytics from the first trimester</p>
      </div>
    </a>

    <a href="{{site.baseurl}}/experience" class="project-card">
      <div class="project-content" style="background: linear-gradient(135deg, #f093fb, #f5576c);">
        <h3 style="margin: 0 0 10px 0; font-size: 1.3rem;">Frontend and Backend Experience</h3>
        <p style="margin: 0; opacity: 0.9; font-size: 0.95rem;">My experience in different coding environments</p>
      </div>
=======
<div style="display: flex; flex-wrap: wrap; gap: 10px;">
    <a href="https://opencodingsociety.com" style="text-decoration: none; display: inline-flex; align-items: center; gap: 8px; padding: 10px 14px; border: 1px solid #FA8072; border-radius: 6px; font-weight: 700;">
        <img src="{{ '/favicon.ico' | relative_url }}" alt="OCS logo" style="width: 16px; height: 16px;">
        OCS
    </a>
    <a href="https://github.com/Open-Coding-Society/portfolio" style=" text-decoration: none; display: inline-flex; align-items: center; gap: 8px; padding: 10px 14px; border: 1px solid #FFF; border-radius: 6px; font-weight: 700;">
        <img src="https://github.githubassets.com/favicons/favicon.svg" alt="GitHub logo" style="width: 16px; height: 16px;">
        GitHub
    </a>
    <a href="https://vscode.dev/" style="text-decoration: none; display: inline-flex; align-items: center; gap: 8px; padding: 10px 14px; border: 1px solid #007ACC; border-radius: 6px; font-weight: 700;">
        <img src="https://vscode.dev/favicon.ico" alt="VSCode logo" style="width: 16px; height: 16px;">
        VSCode.dev
>>>>>>> upstream/main
    </a>
  </div>
</div>
<<<<<<< HEAD
=======

<br>

### Class Progress

> Here is my progress through coding, click to see these online

<div style="display: flex; flex-wrap: wrap; gap: 10px;">
    <a href="{{site.baseurl}}/snake" style="text-decoration: none;">
        <div style="background-color: #00FF00; color: black; padding: 10px 20px; border-radius: 5px; font-weight: bold;">
            Snake
        </div>
    </a>
    <a href="{{site.baseurl}}/gamify/parallax" style="text-decoration: none;">
        <div style="background-color: #3c1de8; color: white; padding: 10px 20px; border-radius: 5px; font-weight: bold;">
           Fish
        </div>
    </a>
    <a href="{{site.baseurl}}/gamify/water" style="text-decoration: none;">
        <div style="background-color: #b71dc5; color: white; padding: 10px 20px; border-radius: 5px; font-weight: bold;">
           Squid
        </div>
    </a>
</div>

<br>
>>>>>>> upstream/main
