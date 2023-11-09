---
title: About Me
---

## What do I do?
I like to work with data and learn about data based skills and tools.  Currently focused on language modeling and application development around custom conversational tools.

---

## Education

<b> B.S. in Statistics and Data Science, Dec 2022 </b>

- University of Texas at San Antonio

---

## Work experience

<b> Business Intelligence Developer - iGrad </b>

<i> Python, SQL, Spark, Azure, Databricks </i>
- Complete end to end data projects with Python, from data acquisition, preprocessing, analysis, modeling, and developing tools with both custom and pretrained models
- Deployed open source NLP machine learning models to create systems for projects including sentiment analysis and machine translation
- Employ Azure products including Azure Data Factory, Pipelines, Cognitive Services, and Azure OpenAI
- Utlize Microsoft Power BI for creating reports and dashboards to present key data and analysis
- Orchestrate Spark jobs and notebooks for automated data processing and migration

---

## Open source experience

<b> Chroma </b>

<i> Chroma is an open source vector database that can be used for storing embeddings and offers semantic search functionality </i>
- After using several vector DB options I enjoyed using Chroma the most as I liked the dev experience the most, so I also contributed in a few ways
- After using Chroma for some time I had a number of collections within my hosted client and needed a way to quickly work with them
- I developed a Chroma Client CLI with commands for connecting to a client, checking client details, checking for all of the collections within, getting colleciton details, and basic querying
- I also have made a number of documentation fixes
- I also regularly assist in question answering within the community channel
- As well as regularly speaking with the cofounders for feature planning and recommendations

<b> Flyte </b>

<i> Flyte is a workflow orchestration platform that unifies data, ML, and analytics </i>
- During SciPy 2023 I was introduced to and met with a key maintainer of Flyte
- I worked alongside maintainers by reviewing repo issues to decide how I could best contribute
- One of the top feature requests was a new plugin for integrating a model analyzing tool called Weight Watchers
- Wrote the plugin as well as the necessary tests per their contributing guide

<b> Huggingface </b>

<i> Huggingface is an open source machine learning platform for sharing pretrained models, datasets, as well as various model training libraries </i>
- As my first open source contributions, I both contributed new datasets, task documentation, and documentation fixes
- I uploaded several of the top public datasets used for SOTA models at the time and wrote the documentation explaining them and their usage
- I also wrote several task documents explaining different tasks like text summarization, zero shot classification, and zero shot image classification


---

## Project experience


<b> Chatbot: KungFu Case Studies Assistant</b>

<i> GPT API, Langchain, Pinecone, RAG </i>
- KungFu is a boutique ML consulting firm with a wide range of past clients and case studies
- It can be time consuming to have to read through 20+ different case studies each being their own article, to get an idea of what kind of work KungFu has done
- Migrated all case study pages to a Pinecone vector database as a source of context 
- Similarity search is performed against a users prompt 
- GPT is then provided the necessary context to be able to answer any question on who KungFu has worked with and what kind of work they have done, with reference links to the particular case study URL 



<b> Drive </b>
- Given 5 driving videos and the respective frame by frame labels of the camera positional pitch and yaw, develop a system to estimate the pitch and yaw of unseen driving videos
- Conduct initial analysis of data at hand, research pretrained models for camera positional estimation, determine candidate systems with and without DL
- Develop and tested non DL approach with a combination of OpenCV tools including Canny edge detection and Hough line transform to calculate pitch and yaw with the vanishing point to extrinsic and intrinsic matrix conversions
- Train a CNNLSTM on labeled videos, reaching less than 0.1 on MSE for the validation set
- Perform CNNLSTM training on an A600 Lambda Labs Cloud GPU due to local device limitations


<b> Google TPU Research Program </b>

<i> GCP/TPU, PyTorch, HuggingFace </i>
- Having limited compute resources, and wanting to experiment with the GCP platform, applied for and was granted access to the Google TPU Research Program 
- Deployed Google VM instances for downloading large data to Goolge Storage including the >100GB ImageNet dataset
- Experimented with training various large computer vision models with both TPUs and GPUs
- Collaborated with other HuggingFace contributors on HuggingFace Trainer and Accelerate integration for Google TPUs 

<b> [Useful Score](https://github.com/cdreetz/jobs23) </b> 

<i> Python, BS4, Selenium, Flask, Postgresql, Heroku </i>
- A straightforward and non opinionated way for indivuduals to gauge their own set of skills or the curriculum of a univerity program they may be interested in.  The scores merely being the importance and relevance of these skills compared directly to the typical requirements in the current job market
- Starting with a Selenium webscraper that is the backbone of the application and is how data is collected to be able to measure scores.  It was developed due to Google job posts not being easily parsed with things like BeautifulSoup.  The scraper searches certain roles and companies on Google while collecting a number of the posts on Google including the jobs id, role, company, and full description.
- All of which initially kept in a MySQL db, then a Mongo db, and finally a Postgresql db due to its integration with Heroku
- Both the API and front end were developed with Flask
- Initially deployed with Heroku
- TODO: Convert the Flask app to something that can be deployed with Vercel, Nextjs maybe

<b> [Lightning](https://github.com/cdreetz/Lightning-ResNet) </b> 

<i> PyTorch Lightning, HuggingFace Hub </i>
- Learning project on Lightning AI or PyTorch Lightning, a ML framework that speeds up typical ML workflows by eliminating the need to write the typical boiler plate ML code
- Done in parallel while learning common deep learning vision models, including ResNet, VGG, and DeepNet
- Monitored model training times and loss with Tensorboard
- Uploaded all trained models and tensorboard logs to my HuggingFace Hub

<b> [DataSci GPT](https://github.com/cdreetz/datasci-gpt) </b> 

<i> Huggingface Accelerate, Tokenizer, Trainer, Hub; Lambda Labs for GPU </i>
- Language model trained specifically on data science related code
- The dataset was a subset of The Stack, one of the largest and best code datasets for language models, filtered for key words down to about 6% its original size
- Done with various HuggingFace libraries including Transformers, and their Auto Tokenizer and Dataloader.
- Trained on A6000 GPU provided by Lambda Labs




## Recent project work
(July 2023) Over the past few months I have focused on developing LLM based tools both for myself while exploring developing for broad use.  I have also spend some time on widening my ML skills which meant doing some CV learning and projects.  One project consisted of a self driving challenge where I trained a model to predict the pitch and yaw of the camera of an unlabeled video.  Another was a project that consisted of a hand tracking tool where using my laptops camera I could show my hand and 20 different points of my hand were tracked and labeled.  I also trained a 120M parameter GPT-2 model with A100s hosted by Lambda Labs which cost $20 and 20 hours to train (A100's on Lambda are about $1.10 an hour)


(Feb 2023) The most recent work I have been doing is from my UsefulScore repository.  Initirally it was an attempt to learn and apply NLP methods, specifically with Python's Spacy package.  Over time it became more of a learning experience for me on using Selenium, on object oriented code, on HTML/CSS and XPATH direction, and on how to best organize a Github repository for a end to end data pipeline that creates a usable interface from the scraped data.



## Skills acquired over time and applied during projects or work

- <b>Programs and Languages</b> Python, R, SQL, SAS, SPSS, Javascript, Bash, 
- <b>Packages</b> Pandas, Numpy, SciPy, Selenium, Ggplot, Caret, Tidyverse
- <b>DS Concepts </b> Linear/logistic regression, time series
- <b>DA Concepts </b> Data preprocessing, missing values, repeated values, converting variable types, column/row subsetting, visualizations
- <b>DA Tools </b> Automated data collection via webdriver
- <b> ML Tools</b> TensorFlow, PyTorch, Lightning, Transformers, Weights and Biases
- <b> NLP/LLM Tools</b> HuggingFace Transformers, Mosaic Composer, Langchain
- <b> NLP/LLM Concepts</b> Sentiment Analysis, Conversational Agents, Agent Tools, Custom Bots
- <b> CV Concepts</b> Object detection, object classification, object tracking
- <b> Cloud Services</b> GCP, TPUs, VertexAI; Azure products; Lambda Labs GPU Clusters 
- <b> Web Development </b> Flask, Vue, Next.js, Hosted Cloud Servers

## Skills in progress

- ~~<b> ML Concepts</b> Production ML data pipeline~~
- <b> Web Dev </b> Next.js app router, Web design with Figma
----
