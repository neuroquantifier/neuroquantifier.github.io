---
layout: post
title: Jupyter Lab & PyTorch Snippets
---

## [Matplotlib](https://matplotlib.org/contents.html)

**Retina + Dark Mode**

```python
import matplotlib.pyplot as plt
%config InlineBackend.figure_format = 'retina'
plt.style.use('seaborn-dark')
```

## Email

Keep in mind that this is an insecure method and therefore it is extremely strongly advised that you don't use your personal or work email. Instead, make a dedicated 'throwaway' email address.

```python
import smtplib
from email.message import EmailMessage

def email(title,body):
    username = 'SENDER@gmail.com'
    password = 'enter password'
    sent_from = username
    to = ['neuroquantifier@gmail.com']
    email_text = f"""From: Vectorized Love <SENDER@gmail.com>
To: Jason Sohn <neuroquantifier@gmail.com>
Subject: {title}

{body}
```
