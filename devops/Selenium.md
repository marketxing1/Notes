Selenium可用于跨平台的不同浏览器的自动化测试。

Selenium测试环境web驱动，地址：
Chrome:	https://sites.google.com/a/chromium.org/chromedriver/downloads  
Edge:	https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/  
Firefox:	https://github.com/mozilla/geckodriver/releases  
Safari:	https://webkit.org/blog/6900/webdriver-support-in-safari-10/  

web驱动相当于一个服务器，相应的还有selenium客户端。客户端将测试命令发给服务器，然后服务器启动网页进行相应的操作。  
这里主要用python来做测试脚本。安装客户端：
```python
pip install -U selenium
```

## start
```python
from selenium import webdriver
from selenium.webdriver.common.keys import Keys

browser = webdriver.Chrome()

browser.get('http://www.yahoo.com')
assert 'Yahoo!' in browser.title

elem = browser.find_element_by_name('p')  # Find the search box
elem.send_keys('seleniumhq' + Keys.RETURN)

browser.quit()
```
[ref](http://selenium-python.readthedocs.io/api.html)

## capabilities
web driver在构造浏览器的时候可以加入相应的参数，修改浏览器的特定参数，满足某些情况下的测试环境要求。
```python
from selenium.webdriver.common.desired_capabilities import DesiredCapabilities
desired_capabilities = DesiredCapabilities.CHROME.copy()
desired_capabilities['chromeOptions'] = {
    "args": ["--flag-switches-begin","--start-maximized", "--flag-switches-end"]
}
browser = webdriver.Chrome(desired_capabilities=desired_capabilities)
```

## 切换页面
```python
for handle in browser.window_handles: 
    browser.switch_to_window(handle)
```
## 等待
当点击页面上面某个按钮之后，新元素和页面的加载需要等待，可以直接用sleep或者用
```python
try:
    WebDriverWait(browser, 3, 0.5).until(
        lambda x: x.find_element_by_id('remoteVideo').is_displayed())
except TimeoutException, e:
    print '------------'
    print e.message
else:
    video = browser.find_element_by_id('remoteVideo')
    print 
```

[ref](http://blog.csdn.net/ping523/article/details/53419622)

