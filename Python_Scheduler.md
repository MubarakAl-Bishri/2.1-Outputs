---
layout: default
fileName: Python_Scheduler
direction: "ltr"
title: "Python Scheduler"
tags:
  -
date-created: 2026-01-28
toReview: True
related_notes:
---
Main python script that runs subscripts on a specific event, I prefer to make [[Hardcoding]]ed. Make more then one [[requirements.txt]] file, one for each subscript in addition to the main script.
The main tool to run a subscript is to use the OS lib. 
If there is a small package or any additional files it is preferred to make a folder for it.
Use the path to make sure that you are in the correct place.
One thing to add, you want any subscript to be running as a main process. To make this doable every subscript needs to have this: 
```python
if __name__ == '__main__':
	mainCodeFunction()
```
if you want to save the output just use `logging` lib. To get the output just use OS commands to save the output and return it.

---
One virtualenv per subscript, and just use subprocess lib
-https://www.geeksforgeeks.org/python/python-subprocess-module/
-https://www.geeksforgeeks.org/python/logging-in-python/