---
layout: default
title: Tools
permalink: /tools/
---

## Here are some tools I use, available through these links.

<!-- Wakatime -->
<figure>
  <button id="toggle-wakatime" style="display: flex; align-items: center; border: none; background: none; cursor: pointer;">
    <img src="{{ site.baseurl }}/assets/icons/Logo.svg" alt="Wakatime Logo" class="logo" style="width: 40px; height: 40px; margin-right: 10px;">
    <span>Programming Languages - Show Wakatime</span>
  </button>
  <div id="wakatime-container" style="display: none; margin-top: 20px;">
    <embed src="https://wakatime.com/share/@6b618539-0e05-404e-949c-e4bd225c514b/41af378e-9a1c-4675-937b-6ba3d0330fa5.svg">
  </div>
</figure>

<!-- Libraries -->
<figure>
  <button id="toggle-libraries" style="display: flex; align-items: center; border: none; background: none; cursor: pointer;">
    <img src="{{ site.baseurl }}/assets/icons/library.svg" alt="Library Logo" class="logo" style="width: 40px; height: 40px; margin-right: 10px;">
    <span>Libraries</span>
  </button>
  <div id="library-container" style="display: none; margin-top: 20px;">
    <ul>
      <li>Pandas</li>
      <li>NumPy</li>
      <li>Scikit-learn</li>
      <li>TensorFlow</li>
    </ul>
  </div>
</figure>

<!-- Databases -->
<figure>
  <button id="toggle-databases" style="display: flex; align-items: center; border: none; background: none; cursor: pointer;">
    <img src="{{ site.baseurl }}/assets/icons/database.svg" alt="Database Logo" class="logo" style="width: 40px; height: 40px; margin-right: 10px;">
    <span>Databases</span>
  </button>
  <div id="database-container" style="display: none; margin-top: 20px;">
    <ul>
      <li>MySQL</li>
      <li>SQLite</li>
      <li>DuckDB</li>
    </ul>
  </div>
</figure>

<!-- Visualization and Reporting -->
<figure>
  <button id="toggle-visualization" style="display: flex; align-items: center; border: none; background: none; cursor: pointer;">
    <img src="{{ site.baseurl }}/assets/icons/visual.svg" alt="Visualization Logo" class="logo" style="width: 40px; height: 40px; margin-right: 10px;">
    <span>Visualization and Reporting</span>
  </button>
  <div id="visualization-container" style="display: none; margin-top: 20px;">
    <ul>
      <li>Streamlit</li>
      <li>Evidence</li>
    </ul>
  </div>
</figure>

<!-- Tools -->
<figure>
  <button id="toggle-tools" style="display: flex; align-items: center; border: none; background: none; cursor: pointer;">
    <img src="{{ site.baseurl }}/assets/icons/tools.svg" alt="Tools Logo" class="logo" style="width: 40px; height: 40px; margin-right: 10px;">
    <span>Tools</span>
  </button>
  <div id="tools-container" style="display: none; margin-top: 20px;">
    <ul>
      <li>Git</li>
      <li>Docker</li>
      <li>Jupyter Notebook</li>
      <li>VS Code</li>
    </ul>
  </div>
</figure>

<script>
  // Wakatime toggle
  document.getElementById("toggle-wakatime").addEventListener("click", function() {
    const container = document.getElementById("wakatime-container");
    const logo = this.querySelector(".logo");
    const text = this.querySelector("span");

    if (container.style.display === "none") {
      container.style.display = "block";
      text.textContent = "Hide Wakatime";
      logo.style.transform = "rotate(360deg)";
    } else {
      container.style.display = "none";
      text.textContent = "Show Wakatime";
      logo.style.transform = "rotate(0deg)";
    }
  });

  // Libraries toggle
  document.getElementById("toggle-libraries").addEventListener("click", function() {
    const container = document.getElementById("library-container");
    const logo = this.querySelector("img");
    const text = this.querySelector("span");

    if (container.style.display === "none") {
      container.style.display = "block";
      text.textContent = "Hide Libraries";
      logo.style.transform = "rotate(360deg)";
    } else {
      container.style.display = "none";
      text.textContent = "Libraries";
      logo.style.transform = "rotate(0deg)";
    }
  });

  // Databases toggle
  document.getElementById("toggle-databases").addEventListener("click", function() {
    const container = document.getElementById("database-container");
    const logo = this.querySelector("img");
    const text = this.querySelector("span");

    if (container.style.display === "none") {
      container.style.display = "block";
      text.textContent = "Hide Databases";
      logo.style.transform = "rotate(360deg)";
    } else {
      container.style.display = "none";
      text.textContent = "Databases";
      logo.style.transform = "rotate(0deg)";
    }
  });

  // Visualization and Reporting toggle
  document.getElementById("toggle-visualization").addEventListener("click", function() {
    const container = document.getElementById("visualization-container");
    const logo = this.querySelector("img");
    const text = this.querySelector("span");

    if (container.style.display === "none") {
      container.style.display = "block";
      text.textContent = "Hide Visualization and Reporting";
      logo.style.transform = "rotate(360deg)";
    } else {
      container.style.display = "none";
      text.textContent = "Visualization and Reporting";
      logo.style.transform = "rotate(0deg)";
    }
  });

  // Tools toggle
  document.getElementById("toggle-tools").addEventListener("click", function() {
    const container = document.getElementById("tools-container");
    const logo = this.querySelector("img");
    const text = this.querySelector("span");

    if (container.style.display === "none") {
      container.style.display = "block";
      text.textContent = "Hide Tools";
      logo.style.transform = "rotate(360deg)";
    } else {
      container.style.display = "none";
      text.textContent = "Tools";
      logo.style.transform = "rotate(0deg)";
    }
  });
</script>