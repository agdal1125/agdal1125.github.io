---
layout: post
title: Web Crawling with BeautifulSoup
comments: true
tags: 
- web crawling
- python3
- beautifulsoup
---
## Webcrawling

Web crawling allows users to gather data directly from the internet. Web crawling is an act of software that explores world wide web (www) is an autonomous way to gather data. Portal's search engines are based on these web crawlers that visits a myriad of web pages and collect data.

&nbsp;
&nbsp;

### How it works

The internet is a collection of web pages formed by HTML (Hyper Text Markup Language). We navigate these HTML pages through browser (*Chrome, Firefox, Safari, Internet Explorer, etc..)* which facilitates exploration of web through Graphic User Interfaces (GUI) and various plugins. Web crawling is done by parsing the HTML, filtering necessary parts and saving them into files. 

### Cautions

- There may be legal penalties depending on the website that you wish to crawl
- Some websites has policies against web crawling (*e.g. robots.txt* contains information about data collection policy)
- Web crawling may cause traffic overload and this is pertinent to security issues

&nbsp;
&nbsp;

## Basic Web Crawling with Python3

Required libaries: bs4, requests,

&nbsp;
&nbsp;

### Simple Web Crawling

&nbsp;

Simple web crawling can be achieved by using bs4 and requests libraries. The tricky part is in understanding structure of html and finding tags where the desired information  belongs.

&nbsp;

    import requests
    from bs4 import BeautifulSoup
    
    # Connect to website via requests module
    url = requests.get("your url that you wish to access")
    
    # Retrieve html
    html = url.text
    
    # Parse the html data with BeautifulSoup
    soup = BeautifulSoup(html, 'html.parser')
    
    # You can see the HTML Raw Source code from the website that you have accessed
    print(soup)
    
    
    # Retrieving specific information, using html tags
    
    ### This retrieves the first html tag that has "div" tag and its class name "itemname"
    print(soup.find("div",{"class":"itemname"))
    
    ### find_all function retrieves all tags that has "a" tag in the raw source codes
    ### shown as a list form
    print(soup.find_all("a"))
    
    ### get_text() function retrieves only text information from the specified tags
    soup.find("div",{"id":"item_number").get_text()
    
