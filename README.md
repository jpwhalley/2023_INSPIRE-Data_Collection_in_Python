# 2023_INSPIRE-Data_Collection_in_Python
## Python code for the 2023 INSPIRE featured presentation on data collection in python.


Ideally the data we wish to work on can be downloaded in an easy to use format. Otherwise when we want only a small subset of a very big dataset, or the data is being constantly updated, hopefully the owner will provide an application programming interface (API) to automate the collection of the relevant data. However quite often the data cannot be downloaded and there is no API, but the data is publicly available, just dispersed across a website. When it would be too tedious and time consuming to navigate page by page to collect the data manually; we can use Selenium Webdriver and Beautiful Soup to automate navigating across the website and collecting of the relevant data. In this code clinic, I will go through the best practices (and what not to do!) when web scraping; using Selenium Webdriver to navigate around a website and then using Beautiful Soup to extract the data from the HTML.

Prerequisites
-------------
### Please install the following suggested software:

1. (Python3)[https://www.python.org/downloads/].  
  
2. All the needed packages are in requirements.txt, you can install individually or:

`pip install -r requirements.txt`

3. Gecko drivers for my web browser [https://selenium-python.readthedocs.io/installation.html#drivers](https://selenium-python.readthedocs.io/installation.html)
    *   You have to put the geckodriverbinary in a path Python can see. If this does not work, I have found that putting it in your working directory (the same as the python notebook), should work.  
  
*   Once you have done that, hopefully running the following code snippet:
```
from selenium import webdriver  
browser = webdriver.Chrome() # Or which ever web browser you are using  
browser.get("[https://www.literaryclock.com](https://www.literaryclock.com/)/“)
```
you should get a pop-up window of the [Literary Clock website](http://www.literaryclock.com/).

Recommended tutorial and reading
--------------------------------
*    Experience in Python will be a bonus. For those new to Python, I recommend them running through the Learn Python “Learn the Basics” and “Data Science Tutorials” chapters, before the module: https://www.learnpython.org/ 
*   A good example of scientific work based on web scraping can be found here: [Soft Drinks Industry Levy paper.](https://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.1003025)
*   Another good example of web scraping is the COVID-19 cumulative trackers, for example [Jon Hopkins COVID-19 Dashboard](https://www.arcgis.com/apps/dashboards/bda7594740fd40299423467b48e9ecf6), as published [here](https://www.thelancet.com/journals/laninf/article/PIIS1473-3099(20)30120-1/fulltext), with [Github repository.](https://github.com/CSSEGISandData/COVID-19)
