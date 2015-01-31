---
layout: post
title:  "Automated testing on cloud using BrowserStack"
date:   2015-01-23
categories: Testing
---

BrowserStack is a cross-browser testing webpage, they also support automated testing on cloud. You can run your test locally from your computer to their cloud server.

The good: Local testing supported. Automated Screenshots on your automated testing. Live preview of automated testing. Responsive testing. Developer tools. Good API support. Good security. Cross-browser. Cross-system. On Cloud.

The bad: Quite pricy. Kinda slow.

In order to use browserStack you need an account(Free account get 100 minutes automated testing.) Once you have an account you need the access key (Can be found under Your account > Automated)

In Ruby:

``` ruby

require 'selenium-webdriver' #Require to run selenium #Below here are the data that you can use caps = Selenium::WebDriver::Remote::Capabilities.new caps["browser"] = "Firefox" #Browser caps["browser_version"] = "33.0" #Browser version caps["os"] = "Windows" #OS caps["os_version"] = "XP" #OS version caps["browserstack.debug"] = "true" # caps["name"] = "Testing on browserstack" #Name of the test

web_driver = Selenium::WebDriver.for(:remote, :url => "Your Access Key", :desired_capabilities => caps)

#...Your Code...

web_driver.get "http://www.google.com"

element = web_driver.find_element(:name, 'q') element.send_keys ("BrowserStack") element.web_driver.find_element(:name, "btnG") element.click

driver.quit

```

You can try to run it on CMD: Ruby nameofthefile.rb But, before this we need to set up the local testing.[Download here](https://www.browserstack.com/browserstack-local/BrowserStackLocal-win32.zip), download the file and unzip it. Put it in the same folder where you store your testing script. Open up CMD, enter: BrowserStackLocal.exe "replace with your access key (get rid of the double quote)" localhost,3000,0 And then run the script using: Ruby nameofthefile.rb. It should connect you with browserstack and you can view your result in [here](https://www.browserstack.com/automate)here.
