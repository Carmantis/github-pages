---
layout: default
title: Projects
permalink: /projects/
---

<!-- Data Processing -->
<figure>
  <button id="toggle-data-processing" style="display: flex; align-items: center; border: none; background: none; cursor: pointer;">
    <img src="{{ site.baseurl }}/assets/icons/data_proces.svg" alt="Data Processing Logo" class="logo" style="width: 40px; height: 40px; margin-right: 10px;">
    <span>Data Processing</span>
  </button>
  <div id="data-processing-container" style="display: none; margin-top: 20px;">
    <p>Data processing involves cleaning, transforming, and organizing raw data to make it useful for analysis. Tools used include Python, Pandas, and SQL.</p>
  </div>
</figure>

<!-- Data Pipeline -->
<figure>
  <button id="toggle-data-pipeline" style="display: flex; align-items: center; border: none; background: none; cursor: pointer;">
    <img src="{{ site.baseurl }}/assets/icons/data_pipe.svg" alt="Data Pipeline Logo" class="logo" style="width: 40px; height: 40px; margin-right: 10px;">
    <span>Data Pipeline</span>
  </button>
  <div id="data-pipeline-container" style="display: none; margin-top: 20px;">
    <p>A data pipeline is a series of processes that automate the collection, processing, and storage of data. This project involved using Apache Kafka and Spark.</p>
  </div>
</figure>

<!-- Machine Learning -->
<figure>
  <button id="toggle-machine-learning" style="display: flex; align-items: center; border: none; background: none; cursor: pointer;">
    <img src="{{ site.baseurl }}/assets/icons/ai.svg" alt="Machine Learning Logo" class="logo" style="width: 40px; height: 40px; margin-right: 10px;">
    <span>Machine Learning</span>
  </button>
  <div id="machine-learning-container" style="display: none; margin-top: 20px;">
    <h1>Project Overview: Data Pipeline & Predictive Modeling with LSTM</h1>

    <!-- Introduction -->
    <h2>Introduction</h2>
    <p>
        This project integrates modern data engineering practices and machine learning 
        to forecast quarterly metrics using a Long Short-Term Memory (LSTM) model.
        We employed <strong>dbt</strong>, <strong>DuckDB</strong>, and 
        <strong>Streamlit</strong> to create a robust data pipeline, following the 
        <em>Medallion Architecture</em> (Bronze, Silver, and Gold layers). This all work in Docker containers.
        Key tasks included data ingestion, feature engineering, model training, and 
        interactive dashboard visualization.
    </p>

    <!-- Architecture -->
    <h2>Architecture: The Medallion Approach</h2>
    <p>
        The data flow is structured into three main layers to ensure scalability, 
        clarity, and reliability:
    </p>
    <ul>
        <li><strong>Bronze Layer:</strong> Raw data (from CSVs) is 
        loaded into DuckDB without transformations.</li>
        <li><strong>Silver Layer:</strong> Data is cleaned, validated, and normalized. 
        Missing values are addressed with <code>KNN-Imputer</code>, and features are 
        standardized with <code>MinMaxScaler</code>.</li>
        <li><strong>Gold Layer:</strong> Aggregated and enriched data is finalized 
        for machine learning tasks and analytical queries. Prediction outputs are 
        also stored here.</li>
    </ul>

    <!-- ETL Process -->
    <h2>ETL Process</h2>
    <p>
        The data transformation workflow (powered by <strong>dbt</strong>) is divided 
        into the following phases:
    </p>
    <ol>
        <li><strong>Extract:</strong> Data is pulled from source files into 
        the Bronze layer.</li>
        <li><strong>Transform:</strong> The Silver layer processes data for missing 
        values, anomalies, and feature scaling. Additionally, features like unit 
        type or quarter identifiers are one-hot encoded.</li>
        <li><strong>Load:</strong> The final Gold layer stores curated data and 
        houses predicted values. These predictions are then accessed and visualized 
        in <strong>Streamlit</strong>.</li>
    </ol>

    <!-- Key Highlights -->
    <h2>Key Highlights</h2>
    <ul>
        <li><strong>LSTM Model Development:</strong> A TensorFlow/Keras-based model 
        trained on historical data to forecast future metrics.</li>
        <li><strong>Data Quality Management:</strong> Missing data handled using 
        <code>KNN-Imputer</code> and anomalous values corrected during transformations.</li>
        <li><strong>Feature Engineering:</strong> One-hot encoding of categorical 
        variables (units, quarters) and scaling with <code>MinMaxScaler</code>.</li>
        <li><strong>Model Evaluation:</strong> Metrics such as MAE, RMSE, and R² 
        were used to gauge performance.</li>
        <li><strong>Streamlit Dashboard:</strong> Interactive interface to compare 
        historical vs. predicted values with dynamic filtering and various 
        visualizations (line, scatter, bar charts).</li>
    </ul>

    <!-- Results -->
    <h2>Results</h2>
    <p>
        By incorporating a structured pipeline with dbt and DuckDB, we achieved 
        consistent data transformations and a reliable environment for 
        machine learning. The LSTM model demonstrated a strong capability to 
        predict quarterly metrics, and the Streamlit application offered 
        a user-friendly platform for exploring both historical and forecasted data.
    </p>
  </div>
</figure>

<script>
  // Data Processing toggle
  document.getElementById("toggle-data-processing").addEventListener("click", function() {
    const container = document.getElementById("data-processing-container");
    const logo = this.querySelector("img");
    const text = this.querySelector("span");

    if (container.style.display === "none") {
      container.style.display = "block";
      text.textContent = "Hide Data Processing";
      logo.style.transform = "rotate(360deg)";
    } else {
      container.style.display = "none";
      text.textContent = "Data Processing";
      logo.style.transform = "rotate(0deg)";
    }
  });

  // Data Pipeline toggle
  document.getElementById("toggle-data-pipeline").addEventListener("click", function() {
    const container = document.getElementById("data-pipeline-container");
    const logo = this.querySelector("img");
    const text = this.querySelector("span");

    if (container.style.display === "none") {
      container.style.display = "block";
      text.textContent = "Hide Data Pipeline";
      logo.style.transform = "rotate(360deg)";
    } else {
      container.style.display = "none";
      text.textContent = "Data Pipeline";
      logo.style.transform = "rotate(0deg)";
    }
  });

  // Machine Learning toggle
  document.getElementById("toggle-machine-learning").addEventListener("click", function() {
    const container = document.getElementById("machine-learning-container");
    const logo = this.querySelector("img");
    const text = this.querySelector("span");

    if (container.style.display === "none") {
      container.style.display = "block";
      text.textContent = "Hide Machine Learning";
      logo.style.transform = "rotate(360deg)";
    } else {
      container.style.display = "none";
      text.textContent = "Machine Learning";
      logo.style.transform = "rotate(0deg)";
    }
  });
</script>
