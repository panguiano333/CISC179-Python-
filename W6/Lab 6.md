# Text Parsing
## Using a List
```python
story='[input story]'
char_count=len(story)
print(char_count)

words=story.split()
word_count=len(words)
print(word_count)
word_frequency={}
for word in words:
    if word in frequency:
        frequency[word]+=1
    else:
        frequency[word]=1
