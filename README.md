# Design a `NewsletterSubscriber` model with email and subscribed_on. Ensure email is unique and auto-track the subscription time.
# admin.py:
```
from django.contrib import admin
from .models import NewsletterSubscriber

admin.site.register(NewsletterSubscriber)
```
# models.py:
```
from django.db import models

class NewsletterSubscriber(models.Model):
    email = models.EmailField(unique=True)
    subscribed_on = models.DateTimeField(auto_now_add=True)

    def __str__(self):
        return self.email
```
# output:

![Screenshot 2025-07-09 111500](https://github.com/user-attachments/assets/7a1c4da9-4196-49e2-bcc7-859e8e645328)


















