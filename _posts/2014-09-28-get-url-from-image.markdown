---
layout: post
title: "Get url from image"
date: 2014-09-28 22:27:33 -0500
comments: true
categories: coding
---
A group chart shared a couple of good blogs that I can RSS, unfortunately, he send it by a image:  
![image](http://i.imgur.com/yv39Zlq.jpg )  
I'm too lazy to manually type them all, so find a free online [OCR(Optical Character Recognition)](http://www.free-ocr.com/). Only select the word I want to recognize, and then I can get raw text. Because the image is very clear, so the accuracy is good. But this one it can't read, which I think is also quite clean.  
![image](http://i.imgur.com/aAiRBJ5.png)

Then using google API automaticlly get URL:
Download google package for python:



```
# Read in the file contain websites' name
import os
os.getcwd()  #Return the current working directory
os.chdir('./documents')   # Change current working directory
f=open('Webname.txt','r')
lines = f.read().split('\n')
```
```
# create a function calls json and urllib, return the website 
import json
import urllib
def geturl(searchfor):
  query = urllib.urlencode({'q': searchfor})
  url = 'http://ajax.googleapis.com/ajax/services/search/web?v=1.0&%s' % query
  search_response = urllib.urlopen(url)
  search_results = search_response.read()
  results = json.loads(search_results)
  data = results['responseData']
  hits = data['results']
  return hits[0]['url']
``` 
```
# Export to a new text file
import time
output=open("website.txt","w")
for i in range(len(lines)):
    time.sleep(0.5)
	output.write(geturl(lines[i]))
	output.write(geturl("\n") # doesn't work sometimes
output.close()
```
Other Method:  
	
	pip install google   #very simple, but slow, have to show 20 search result
	
	from google import search
    	    for url in search('"Breaking Code" WordPress blog', stop=20):
    	        print(url)
 