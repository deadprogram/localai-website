
+++
disableToc = false
title = "Easy Request - Openai"
weight = 2
+++

Now we can make a openai request!

OpenAI Chat API Python -

```python
import os
import openai
openai.api_base = "http://localhost:8080/v1"
openai.api_key = "sx-xxx"
OPENAI_API_KEY = "sx-xxx"
os.environ['OPENAI_API_KEY'] = OPENAI_API_KEY

completion = openai.ChatCompletion.create(
  model="lunademo",
  messages=[
    {"role": "system", "content": "You are a helpful assistant."},
    {"role": "user", "content": "How are you?"}
  ]
)

print(completion.choices[0].message.content)
```

OpenAI Completion API Python -

```python
import os
import openai
openai.api_base = "http://localhost:8080/v1"
openai.api_key = "sx-xxx"
OPENAI_API_KEY = "sx-xxx"
os.environ['OPENAI_API_KEY'] = OPENAI_API_KEY

completion = openai.Completion.create(
  model="lunademo",
  prompt="function downloadFile(string url, string outputPath) ",
  max_tokens=256,
  temperature=0.5)

print(completion.choices[0].text)
```

Have fun using LocalAI!
