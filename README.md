# Cookie Clicker Bot


```python
from time import sleep
from selenium import webdriver

browser = webdriver.Firefox()

browser.implicitly_wait(5)

browser.get('https://orteil.dashnet.org/cookieclicker/')


cookie_click = browser.find_element_by_xpath("/html/body/div[2]/div[2]/div[15]/div[8]/div[1]")

for i in range(0,10000):
    cookie_click.click()
    cookie_click.click()
    cookie_click.click()
    cookie_click.click()
    cookie_click.click()
    cookie_click.click()
    cookie_click.click()
    cookie_click.click()
    cookie_click.click()
    cookie_click.click()


```

# Type Racer


```python
from time import sleep
from selenium import webdriver


browser = webdriver.Firefox()

browser.implicitly_wait(5)

browser.get('https://play.typeracer.com/')

# Play Button
browser.find_element_by_xpath("/html/body/div[1]/div/div[1]/div/div[1]/div[2]/table/tbody/tr[2]/td[2]/div/div[1]/div/div[1]/div/a").click()




def run_game():
    
    sleep(5)

    path1 = "/html/body/div[1]/div/div[1]/div/div[1]/div[2]/table/tbody/tr[2]/td[2]/div/div[1]/div/table/tbody/tr[2]/td[3]/table/tbody/tr[2]/td/table/tbody/tr[1]/td/table/tbody/tr[1]/td/div/div/span[1]"
    element = browser.find_element_by_xpath(path1)

    pathb = "/html/body/div[1]/div/div[1]/div/div[1]/div[2]/table/tbody/tr[2]/td[2]/div/div[1]/div/table/tbody/tr[2]/td[3]/table/tbody/tr[2]/td/table/tbody/tr[1]/td/table/tbody/tr[1]/td/div/div/span[2]"
    elementb = browser.find_element_by_xpath(pathb)

    path2 = "/html/body/div[1]/div/div[1]/div/div[1]/div[2]/table/tbody/tr[2]/td[2]/div/div[1]/div/table/tbody/tr[2]/td[3]/table/tbody/tr[2]/td/table/tbody/tr[1]/td/table/tbody/tr[1]/td/div/div/span[3]"
    element2 = browser.find_element_by_xpath(path2)


    combine = element.text + elementb.text+" "+ element2.text
    print(combine)

    inputpath = "/html/body/div[1]/div/div[1]/div/div[1]/div[2]/table/tbody/tr[2]/td[2]/div/div[1]/div/table/tbody/tr[2]/td[3]/table/tbody/tr[2]/td/table/tbody/tr[2]/td/input"

    inputthing = browser.find_element_by_xpath(inputpath)

    sleep(10)

    #Hopefully start race by now

    str_list = combine.split()
    print("LAUNCH !!!!!!")
    for e in str_list:
        new_e = e+" "
        sleep(0.4)
        inputthing.send_keys(new_e)

    sleep(5)
    play_again()
    
def play_again():
    path = "/html/body/div[1]/div/div[1]/div/div[1]/div[2]/table/tbody/tr[2]/td[2]/div/div[1]/div/table/tbody/tr[2]/td[3]/table/tbody/tr[3]/td/table/tbody/tr/td[2]/a"
    browser.find_element_by_xpath(path).click()
    run_game()




run_game()



    

```


```python

```


```python

```
