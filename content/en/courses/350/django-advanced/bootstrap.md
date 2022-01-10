---
# Page title
title: User Management Using Allauth

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: User Management

# Date page published
date: 22022-01-10T17:21:40Z021-12-23

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 10

draft: False


---

Django already includes some user management features that you have used when using the admin interface. I would recommend utilizing the `django-allauth` library to include user management functionality, including login, logout, signup, and social login.

To install django-allauth type the following in terminal:
```bash
pip install django-allauth
```
**Note:** Use `pip3` instead if you are on a mac.

After installation you need to configure the `settings.py` file in your project to use the library. Modify it to add the following lines:

```python

# Add the following
AUTHENTICATION_BACKENDS = [
    'django.contrib.auth.backends.ModelBackend',
    'allauth.account.auth_backends.AuthenticationBackend',
]


# Modify INSTALLED_APPS to include the following
INSTALLED_APPS = [
    # in addition to what you have add these
    'django.contrib.sites', 
    'allauth',
    'allauth.account',
    'allauth.socialaccount',
]

# add the following
SITE_ID = 1

# configure this to redirect to a screen after login
# Here we will redirect to the index page
LOGIN_REDIRECT_URL = "/"

# Disable email verification since we will not configure an email server
ACCOUNT_EMAIL_VERIFICATION = "none"

```

Then you must wire the urls for allauth. Modify the main urls.py file for your project (not the one under your app):

```python
    path('accounts/', include('allauth.urls')),
```

After configuration remember to run the following command in terminal:
```bash
python manage.py migrate
```



Now you are ready to use allauth. Test it by going to `/accounts/signup` in your browser. Then try logging in with the account you create at `/accounts/login`.

## Adding Users to your Modles

Now that you have allauth installed, you can link the Django user model to the models you defined in your `models.py`. You must import the `get_user_model()` in your 'models.py`:

```python
from django.contrib.auth import get_user_model
```

Every place you would link to the User model in your models, you would instead use `get_user_model()`.

Typically we would use relationships to link a User to our models. Depending on the type of relationship, we can use `OneToOneField` for one to one relationships, `ForeignKey` for one to many relationships, and `ManyToManyField` for many to many relationships. For example:

- User profile will likely be a onetoone relationship because every user will have a single profile. It owuld look something like this:
```python
class Profile(models.UserModel):
    bio = models.TextField()
    email = models.EmailField()
    # other fields in the profile here
    user = models.OneToOneField(
        get_user_model(),
        on_delete=models.CASCADE,
    )
```

- Blog posts from the example we used in the blog project will have a single author that can be a user. The user will have multiple posts, therefore a `ForeignKey` is used instead. We would modifu the post to look like this:

```python
  title = models.CharField(max_length=200, unique=True)
  slug = models.SlugField(max_length=200, unique=True)
  body = models.TextField()
  created_on = models.DateTimeField(auto_now_add=True)
  updated_on = models.DateTimeField(auto_now=True)
  status = models.IntegerField(choices=STATUS, default=0)
  # The change is here
  author = modes.ForeignKey(
      get_user_model(),
      on_delete=models.CASCADE,
  )
```

Adding the `author` field allows you to store which user wrote the post. The great thing about linking to the User model is that when you link to a user, then you link to all their information including email, first name, and last name. I will not show a many to many example and will leave that as an exercise to the reader.

## Accessing The User Model

You can access the user model in one of two ways:

1. The fields you link to the user model:
    In our previous example, the user profile has the field `user`, and in Post example the field `author` is the one you would access the user objects from.
2. The HTTP request:
    Django will always attache a user objects to the http request objects. So in your views, you can get the currently connected user by accessing `request.user`. Similarly, the same `request.user` variable will be available and can be accessed in the django templates.

## User Fields and Methods

The Django User model has the following [fields and methods](https://docs.djangoproject.com/en/4.0/ref/contrib/auth/) that you can use in your views or templates:
- **username**: to get the username
- **email**: to get the user's email
- **is_staff**: will be true if the user is an administrator and can use the admin interface.
- **is_authenticated**: will be true if the user that currently opened the view is logged in.

You can use these methods and fields in the view functions or templates.