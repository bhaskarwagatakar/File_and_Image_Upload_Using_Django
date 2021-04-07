# File_and_Image_Uploading_Using_Django
This project is about how to implement file and then image uploading with Django.

# Project and App:
django-admin startproject config
cd config
django-admin startapp posts

# config/settings.py

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'posts', # new
]

# Models

# posts/models.py
from django.db import models


class Post(models.Model):
    title = models.TextField()
    cover = models.ImageField(upload_to='images/')

    def __str__(self):
        return self.title
# MEDIA_ROOT

# config/settings.py
MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')

python manage.py createsuperuser
python manage.py runserver

# created media file to store file(images)
mkdir media
mkdir media/images

# Admin
# posts/admin.py
from django.contrib import admin

from .models import Post

admin.site.register(Post)

