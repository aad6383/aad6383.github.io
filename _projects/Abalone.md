---
layout: page
title: Abalone Age Prediction — EDA, Modeling & RAG
description: Exploratory data analysis, interpretable modeling, and a retrieval-augmented generation (RAG) application for abalone age prediction
img: assets/img/abalone_cover.png
importance: 1
category: work
---

## 🎥 Presentation Video

The full project presentation includes problem framing, modeling decisions, the Shiny application demo, and the RAG system walkthrough.

<video
  controls
  preload="metadata"
  playsinline
  style="width: 100%; max-width: 100%; border-radius: 8px;"
>
  <source src="{{ site.baseurl }}/assets/video/GMT20251214-234616_Recording_3840x2160.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

## 🤖 Retrieval-Augmented Generation (RAG) Application

This RAG application demonstrates how a language model can answer questions about the abalone dataset and modeling results by retrieving relevant context prior to generation.

- **Google Colab Notebook (RAG Demo):**  
  <a href="https://colab.research.google.com/drive/1o3ShtNyI65zYJyPDbFMo-4yhT87WbZNV?usp=sharing" target="_blank">
    Open RAG Application in Google Colab
  </a>

> Note: Google Colab notebooks cannot be embedded due to security restrictions and will open in a new tab.

---

## 📊 Interactive R Shiny Application

The Shiny app allows users to explore predictors, visualize nonlinear relationships, and interact with the final abalone age prediction model.

<iframe
  src="https://aayushdalal2025.shinyapps.io/AbaloneAgeApp/"
  width="100%"
  height="900"
  style="border: none;"
></iframe>

---

## 📄 Full EDA & Modeling Report

The complete exploratory analysis, model development, diagnostics, and interpretation are available below as an interactive HTML report.

<iframe
  src="{{ site.baseurl }}/assets/html/Doing_Data_Science_Project_2.html"
  width="100%"
  height="1200"
  style="border: none;"
></iframe>
