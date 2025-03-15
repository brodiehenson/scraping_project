# Scraping Project Description

## Aim of the project
For this project, I scraped the U.S. National Parks page and each state and territory page listed under the main parks page. For each park listed on the U.S. National Parks page, I wanted to get its name, partial url, designation, city and state. For example, the code I have written will scrape this information for Yosemite National Park following what I have just described: Yosemite, /yose/, National Park, the Sierra Nevada, CA, California.

The code used to write to the csv file is under the tab 'web_scraping_project.ipynb'.

## Steps in scraping
The steps I took in scraping the U.S. National Parks page are listed below:

First, the loop function writing to the csv file opens each state and territory page in BeautifulSoup by appending the partial url to the main page url (which is the same for every state and territory).

Then, a variable is written to receive the state or territory of the page containing the parks the program is currently scraping. 

Two more variables are written to find all the 'ul' and 'li' elements containing the needed information.

Then, another loop is written that gets the park name, partial url, designation and city from within the 'li' elements and writes them into the csv file. The function includes a 'try/except' statement to account for missing elements used to find the information within the 'li' tags. 

Finally, the csv file is closed.

## Pitfalls of the process
One unexpected problem that occured was the missing elements in the 'li' tags. This issue was resolved by using a 'try/except' statement.
