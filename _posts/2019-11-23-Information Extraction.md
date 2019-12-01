---
layout: post
title: Information Extraction
tags:
- NLP
- Information Extraction
- Named Entity Recognition
- Unstructured Data
mathjax: true
---



What comes to your mind when you think about data? Numbers? Fancy graphs? Nicely organized Excel tables and spreadsheets? The first thing that appears in my head is a messy table with lots of missing values and unstructured texts. The big data that media and people are talking about mostly refers to **unstructured  data**; Approximately, 75-85% of data is unstructured, primarily text.<sup>1</sup> Although the figures may have variations, the takeaway here is that most of what we call "the big data" is a raw material; we have to mine and extract it to make it useful.

<br>

## Unstructured Data

We see unstructured data everyday. Our emails, text messages, comments, audio files, video, etc. Although there are useful information in those data, it is difficult to process or gain insights from them. This is because they are ambiguous and have different contexts. Unlike structured data which has **metadata** like pre-defined fields (columns), unstructured data doesn't have a fixed format or "description data of the data". This makes the data searchable for machines and put them into algorithms or models. 

Let's look at the example below:

<br>

<figure>
  <img src="https://www.researchgate.net/profile/Jorge_Cardoso4/publication/236860222/figure/fig4/AS:669293989593114@1536583530877/Unstructured-semi-structured-and-structured-data.png" width="700" height="300">
  <figcaption style="font-size: 8pt; text-align: center;">source: https://www.researchgate.net/figure/Unstructured-semi-structured-and-structured-data_fig4_236860222</figcaption>
</figure>

<br>

The unstructured data is just a plain text. We can read it and process the information in our head. There are  4 people described in this text and this contains information about their age, id and pursuing degree. However, we cannot search through this data using our computers. Computer needs index and column to retrieve search results. If we want to search for Robert's age, we just have to run SQL queries to fetch his name like this `SELECT Age FROM TABLE_NAME WHERE Name="Robert;"`

This is what makes unstructured data and structured data different. In short, we have to extract information from the unstructured data and convert it to structured data. 

This is the field in Natural Language Process, **Information extraction**.

<br>

## Information Extraction

**Information Extraction** (**IE**) refers to the process of automatically retrieving structured information from unstructured data. It can be regarded as a pre-requisite step for analyzing unstructured data. This term is distinct from **Information Retrieval** (**IR**), which is more relevant to the "querying" or "searching" documents based on some set of keywords. 

<br>

### General Architecture, Process, Subtasks of Information Extraction

Information Extraction includes following subtasks according to its nature of problem:
&nbsp;

- **Named Entity Recognition (NER)** 

  >Recognizing known entity names such as people, places, numerical expression. The task focuses on identifying the entity and extracting it. For example, "Jake lives in Canada" can be processed into  extracting "Jake" as a person and "Canada" as a location.

&nbsp;&nbsp;

- **Named Entity Linking (NEL);Named Entity Disambiguation (NED)**

  >Named Entity Linking is getting entities from NER and matching it to the knowledge that you already have in the database. It is a task of finding what the entity actually means in terms of the context. For example, from the sentence "Tom is one of the best actors in history. He showed excellent performance  on Mission Impossible series", NER system will recognize Tom as a person. However, it doesn't know whether this is Tom Cruise or Tom Hanks. Named Entity Linking will retrieve knowledge from the existing database to find answer to this problem using the context.

  &nbsp;

- **Temporal Information Extraction (Event Extraction)**

  >The purpose of Temporal Information Extraction is to identify events. Detecting certain frequency, dates, recognizing who is involved and what is happening. For example from the sentence, "Yesterday Jake hurt his leg so he won't play soccer tomorrow ", Yesterday and tomorrow is the temporal information and we can structure our data by putting these information into date and matching description according to the date: Yesterday : hurt his leg , tomorrow : won't play soccer.

&nbsp;

- **Relation Extraction (RE)**

  >This task is pretty much self-explanatory; it is about figuring out relationship between entities. For example, from the sentence, "Jake studies in UBC"  information such as PERSON studies in LOCATION can be extracted.

&nbsp;

- **Coreference Resolution (CR)**

  >This is a task specifically for detecting entities called in different names. For example, "Microsoft" and "MS" refers to the same entity but in different ways. CR tries to find all expression that respective entities have.

<br>

<div>
  <center><img src="https://www.researchgate.net/publication/326264437/figure/fig1/AS:646327264374784@1531107836947/General-Information-Extraction-Architecture-Adapted-from-Costantino-et-al-1997.png" width="600" height="450" ></center>
  <figcaption style="font-size:8pt; text-align:center;">Fig.1 General Information Extraction Architecture. Adapted from (Costantino et al., 1997)
  </figcaption>
</div>



<br>

### Methodologies/Approaches

Also, there are several types of approaches and methodologies to Information Extraction<sup>2</sup>:

- **Rule Learning** based Extraction Method
- **Classification based** Extraction Method
- **Sequential Labeling** based Extraction Method
- **Non-linear CRF** (Conditional Random Fields) based Extraction Method

(I will discuss each approaches on individual posts)



___



#### References & Citations:

<sup>1 http://breakthroughanalysis.com/2008/08/01/unstructured-data-and-the-80-percent-rule/</sup> 

<sup>2 Tang, Jie, et al. "Information extraction: Methodologies and applications." *Emerging Technologies of Text Mining: Techniques and Applications*. IGI Global, 2008. 1-33.</sup>