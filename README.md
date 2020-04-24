# adding-cookies-with-Selenium-in-python
hey, me and my buddy are working on a program to try and add cookies to certain webpage so that we won't have to put in our username and password here is the code we have so far, but having error message "local variable 'profiles_ini_path' referenced before assignment" come up. anyways here is our code to deal with cookies so far, if anyone with examples could possibly show us on a different website that requires a login that would be great.
from selenium import webdriver 
from SeleniumCookies import cookie_injector 
from selenium.webdriver.chrome.options import Options    
cookies = cookie_injector.inject_cookie()    
chrome_options = Options() 
chrome_options.add_argument("--user-data-dir=chrome-data") 
driver = webdriver.Chrome('/Users/lucianfairbrother/PycharmProjects/Seleniumsession/drivers/chromedriver 4', options=chrome_options) chrome_options.add_argument("user-data-dir=chrome-data") 
url = 'https://www.easports.com/fifa/ultimate-team/web-app/' driver.get(url) for cookie in cookies: 	
  try: 		
      driver.add_cookie(cookie) 	
  except: 		
    pass
