# Web Scraping and Data Mining: A gentle introduction

**Welcome to this short tutorial on Web Scraping and Data Mining techniques!**

You can use the [Google Cloud Python Platform](https://colab.research.google.com/) to start you scraping project


### Web Scraping
Open a new notebook in Colab!

## Data Source
Open a new webpage and go to [WSJ](https://www.wsj.com/search?query=energy&mod=searchresults_viewallresults)  to inspect data to scrape

```markdown
Syntax highlighted code block

import sys
sys.path.insert(0,'/usr/lib/chromium-browser/chromedriver')
from selenium import webdriver
from selenium.webdriver.support import expected_conditions as EC
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.common.exceptions import NoSuchElementException
from webdriver_manager.chrome import ChromeDriverManager
chrome_options = webdriver.ChromeOptions()
chrome_options.add_argument('--headless')
chrome_options.add_argument('--no-sandbox')
chrome_options.add_argument('--disable-dev-shm-usage')

prefs = {
    "download.open_pdf_in_system_reader": False,
    "download.prompt_for_download": True,
    "plugins.always_open_pdf_externally": False
}
chrome_options.add_experimental_option(
    "prefs", prefs
)

driver = webdriver.Chrome('chromedriver', options=chrome_options)
driver.implicitly_wait(5)
```




### Support or Contact

Having trouble with example code? Some new questions or ideas you want to explore?
Contact me at _nuccio.ludovico@gmail.com_
