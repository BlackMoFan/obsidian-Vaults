1. # Trendy
Solution:
```python
import re
def hashtag(post):
	regex = r'#\S+'
	hashtag_list = re.findall(regex, post)
	return hashtag_list
 ```



2. 

