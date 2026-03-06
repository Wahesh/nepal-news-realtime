
Nepal News Realtime is a live data-archiving project capturing the digital news output of Nepal. This repository serves as a raw corpus for training Large Language Models (LLMs) and conducting Natural Language Processing (NLP) research in the Nepali language. By aggregating content from the entire news space, the project provides a contextually aware dataset that reflects the linguistic, political, and cultural landscape of the country.

Research and Educational Purpose Only
This project is strictly for non-commercial research. The goal is to provide a high-quality dataset for:

Training and fine-tuning Nepali-specific language models.

Sentiment analysis and entity recognition within the Nepali context.

Archiving contemporary Nepali literature and journalism for linguistic study.

Data Architecture
The project utilizes automated scraping to pull content from major national and regional portals. Data is organized chronologically to maintain a manageable repository structure and allow for time-series analysis.

Storage Format
Files are stored as JSON batches organized by date:

Year / Month / Day / [source_name].json

Data Schema
Each entry includes the following fields:

title: The headline of the article.

body: The full text content, stripped of HTML and advertisements.

url: Source attribution for verification.

timestamp: Date and time of publication.

Ethics and Compliance
The project adheres to the following principles:

Respect for Robots.txt: Scrapers follow the exclusion and delay rules of each publisher.

Rate Limiting: Requests are throttled to ensure no impact on the performance of host websites.

Ownership: All intellectual property rights belong to the original publishers. This repository acts as a structured index for academic and research purposes only.

Usage
To use this data for training, users can clone the repository and use standard JSON parsing libraries.

Example:

Python
import json
import os

# Example of loading a specific news file
with open('path_to_file.json', 'r', encoding='utf-8') as f:
    news_data = json.load(f)
License
Code: MIT License

Data: Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International
