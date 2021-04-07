# File_and_Image_Uploading_Using_Django
             This project is about how to implement file and then image uploading with Django.

# pip install django

We'll need two urls.py file updates. First at the project-level config/urls.py files we need to add imports for settings , include , and static . Then define a route for the posts app. Note we also need to add the MEDIA_URL if settings are in DEBUG mode, otherwise we won't be able to view uploaded images locally.


