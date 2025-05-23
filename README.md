# 6GPlan

This repo includes the 6GPlan dataset. 

Firstly, we selected 11 topics regarding 6G networks, e.g., integrated sensing and communication, mmWave and Terahertz Communications, non-terrestrial networks, cell-free massive MIMO, etc. 
For each category, we asked an LLM to generate related questions, focusing on complex network management and optimization tasks. 

After that, we consider a multi-LLM question-answering approach: asking multiple LLMs to generate solutions for a given question, and then extracting related technical keywords from their replies.

Here we use these keywords to represent the key elements that should be covered in a high-quality solution. 
At the end, we will merge the keywords from these LLMs, and implement human verification and correction, guaranteeing the dataset quality. 
