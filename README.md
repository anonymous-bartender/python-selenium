# python-selenium
Reusable methods for Python and selenium bindings

### Efficient way to wait for a element till it appear on screen

````
def wait(element):
 return polling.poll(
    lambda: selector if (element.is_displayed()==True) else None,
    ignore_exceptions=(StaleElementReferenceException,),
    step=1,
    timeout=30)
````

Sameple usage:
````
elements = driver.find_elements_by_css_selector('.navigation-links a')
for ele in elements:
    print(wait(ele).text)
````
