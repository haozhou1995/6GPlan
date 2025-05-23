# 6GPlan

This repo includes the 6GPlan dataset, which is used for evaluating LLM's capabilities in handling complicated 6G network management problems.
It contains 110 complicated planning/management tasks distributed across 11 core 6G themes (e.g., RIS, semantic communications, mmWave/Terahertz networks). Each question is paired with a set of gold-standard technical keywords (around 5000 total) that serve as our reference for evaluation. 

The following figure shows the main procedures of creating the dataset:

<p align="center">
<img src=Asset/fig-dataset2.jpg width=60%  />
</p>

Firstly, we selected 11 topics regarding 6G networks, e.g., integrated sensing and communication, mmWave and Terahertz Communications, non-terrestrial networks, cell-free massive MIMO, etc. 
For each category, we asked an LLM to generate related questions, focusing on complex network management and optimization tasks. 

After that, we consider a multi-LLM question-answering approach: asking multiple LLMs to generate solutions for a given question, and then extracting related technical keywords from their replies.

Here we use these keywords to represent the key elements that should be covered in a high-quality solution. 
At the end, we will merge the keywords from these LLMs, and implement human verification and correction, guaranteeing the dataset quality. 
