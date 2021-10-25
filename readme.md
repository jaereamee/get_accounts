# Stock price tracker
<mark>Using the unofficial yfinance API
this just requests the quote in the format yahoofinance gives, and runs a web crawler
https://algotrading101.com/learn/yfinance-guide/ 
https://pypi.org/project/yfinance/ 
https://algotrading101.com/learn/yfinance-guide/ 
https://github.com/ranaroussi/yfinance 
	**SUCCESS!**</mark>
1. `conda activate finance_tracker`
2. `python holdings.py`
https://towardsdatascience.com/the-unofficial-yahoo-finance-api-32dcf5d53df –> alternatively the yahooquery api which can more reliably extract financial statements. (income_statement, balance_sheet and cash_flow)
	https://stackoverflow.com/questions/22086116/how-do-you-filter-pandas-dataframes-by-multiple-columns –> I will probably want to filter out the results by using pandas dataframe manipulation. If not they return me a long table.

# Modifying excel with python
<mark>**openpyxl**</mark>
# Managing data with a RDBMS instead.
## notes on ideal db structure:

1. historical
https://softwareengineering.stackexchange.com/questions/276395/two-database-architecture-operational-and-historical 
https://stackoverflow.com/questions/3874199/how-to-store-historical-data 
## import excel to RDB 
<mark>https://medium.com/@AviGoom/how-to-import-a-csv-file-into-a-mysql-database-ef8860878a68 
**DONE**</mark>

1. How to batch edit data in some columns? Try this
   1. first use if else statements and save in a new column 
   2. learn to splice string from back
   3. then after replace original column with new column and delete new column 
## Modifying with MySQL via Python

# Googlemaps
https://github.com/googlemaps/google-maps-services-python 

# Web scraper
Web page extractor
https://urllib3.readthedocs.io/en/latest/reference/urllib3.request.html
https://docs.python.org/3/library/urllib.parse.html#module-urllib.parse 
https://docs.python.org/3/howto/urllib2.html
[regular Web Scraper (maybe for financials and news feed)](https://realpython.com/beautiful-soup-web-scraper-python/)

[some app you can make 250,000 requests for free.](https://aroussi.com/post/tradologics-the-future-of-trading)

[webscraping login websites with python](https://towardsdatascience.com/scraping-data-behind-site-logins-with-python-ee0676f523ee)

## form filling
https://learn.onemonth.com/automate-web-forms-with-python/ 

# pull financial statements
[some free tools this ex banker uses.](https://www.toptal.com/finance/freelance/bloomberg-terminal-alternative) 

# automate reading PDFs
[PDF to excel API](http://pdfextractoronline.com/pdf-to-excel-api/) 
https://towardsdatascience.com/extracting-data-from-financial-pdfs-dc2fa0b73169 
1. first an algo attempts to create bounding boxes around things it thinks is text
2. then another algo does OCR to detect characters
3. lastly an algo tries to understand if the detected text is organised as a table or free-form text.

# machine learning
[running tensorflow with your GPU. Tensorflow-gpu](https://towardsdatascience.com/how-to-traine-tensorflow-models-79426dabd304)
Machine learn on market 
machine learning and RDBs 
[data preperation using MySQL](https://blog.bigml.com/2013/10/30/data-preparation-for-machine-learning-using-mysql/)
https://docs.mindsdb.com/tutorials/microsoft-sql-server/?utm_medium=display&utm_source=google&utm_campaign=mssql&gclid=CjwKCAiAkJKCBhAyEiwAKQBCkhbaqhiXBgoa7_O7fPiJES4dxmix3pb-RsOoba1IcQd60l_KYOWUfBoClIMQAvD_BwE 

# ai analyst
An ai which knows NLP, can be trained on market data and I can discuss stock ideas with it.
1. Pull historical financials 
2. translate to fcf
3. Project segments
	1. knows market growth and market share
	2. It should be able to do SOTP. Each segment it can try DCF, asset-based, or multiple approach.
4. obtain appropriate multiple for industry. You should be using the exit multiple approach, perpetuity just doesn’t make sense.
5. Obtain target price
6. Probabilistic outcome (report actionables: buy this now, do nothing, sell)
	1. “there will be quite a few stocks that will be up 100% by end of the year, you just need to pick a few of them”
	2. 25% below target price and more, buy. Target price, sell half. 25% above target price, sell all.
7. I can say “lets try fining the company”, “lets say a disruptor happens”
https://www.business-science.io/finance/2020/02/21/tidy-discounted-cash-flow.html –> DCF using R
1. lets do this but with Python
	1. Step 1: tabula-py, extracts table from pdf to python dataframe
	2. not only that but also would be good to have macro data (interest rates are particularly useful as it helps determine cost of debt)