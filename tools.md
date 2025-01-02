---
layout: default
title: Tools
permalink: /tools/
---

## Tools and Technologies

Here are some of the tools and technologies I have worked with.

## Programming Languages

<figure>
  <button id="toggle-wakatime" style="display: flex; align-items: center; border: none; background: none; cursor: pointer;">
    <img src="/Portfolio/assets/icons/waka.svg" alt="Wakatime Logo" style="width: 40px; height: 40px; margin-right: 10px;">
    <span>Show Wakatime</span>
  </button>
  <div id="wakatime-container" style="display: none; margin-top: 20px;">
    <embed src="https://wakatime.com/share/@6b618539-0e05-404e-949c-e4bd225c514b/3893d6c8-0e15-4ad8-9f0b-3c0e19b01f3a.svg">
  </div>
</figure>

## Libraries and Frameworks

- Pandas
- NumPy
- Scikit-learn
- TensorFlow

## Databases

- MySQL
- SQLite
- DuckDB

## Visualization and Reporting

- Streamlit
- Evidence

## Tools

- Git
- Docker
- Jupyter Notebook
- VS Code



<script>
  document.getElementById("toggle-wakatime").addEventListener("click", function() {
    const container = document.getElementById("wakatime-container");
    const text = this.querySelector("span");
    if (container.style.display === "none") {
      container.style.display = "block";
      text.textContent = "Hide Wakatime";
    } else {
      container.style.display = "none";
      text.textContent = "Show Wakatime";
    }
  });
</script>