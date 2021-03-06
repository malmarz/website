---
# Page title
title: ISOM 350 - Business Application Development

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: Improved Admin

# Page summary for search engines.
summary: Second programming course for MIS majors utilizing Python to build data-driven business applications.

# Date page published
date: 2021-03-23

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 4

draft: False


---

{{% callout note %}}
Switch to branch **4-improved admin** from **malmarz/isom350-blog** github repo to see this step's implementation
{{% /callout %}}

In the previous step, we created a very simple default admin page. Django allows us to configure how the admin works by defining an ModelAdmin class in blog/admin.py.

We started with the following:

```python
from django.contrib import admin

from .models import Post

admin.site.register(Post)
```

Let's modify it to have a configurable admin interface by creating a PostAdmin class that inherits from the ModelAdmin class:

```python
from django.contrib import admin
from .models import Post

class PostAdmin(admin.ModelAdmin):
  pass

admin.site.register(Post, PostAdmin) # Notice this line changed
```

Notice how we defined `class PostAdmin(admin.ModelAdmin)` which is empty. This means that inherits everything the ModelAdmin has to offer. If you test it you will notice nothing changed about our admin interface and that what we just did is just a longer version of what we did earlier. However, the new version is more flexible and allows as to configure the admin.

So let's first modify what is shown in the list view of the Post admin, so modify the code to look like this:
```python
from django.contrib import admin
from .models import Post

class PostAdmin(admin.ModelAdmin):
    list_display = ('title', 'slug', 'status','created_on') # This line was added

admin.site.register(Post, PostAdmin)
```

Here we requested that the table displaying the Posts should display a column showing the title, slug, status, and created_on fields. Our list of Post in admin now look like this:

{{< figure src="courses/350/admin-list.png" caption="Improved Admin Post List" >}}

Next let's add the ability yo filter this list by status:

```python
from django.contrib import admin
from .models import Post

class PostAdmin(admin.ModelAdmin):
    list_display = ('title', 'slug', 'status','created_on')
    list_filter = ("status",) # This line was added


admin.site.register(Post, PostAdmin)
```

Now we have the option to list all posts, the draft posts only, or published posts only:

{{< figure src="courses/350/list-filter.png" caption="Admin Post Filter" >}}

As you can see, whenever we want to configure the admin, we add an attribute (a line) that configures the features of the ModelAdmin for our posts and these configurations are reflected on our model admin.

Let's look at two more configurations, first, lets add the ability to search posts. Here we are adding the ability to search posts in the admin interface using their title and content fields:


```python
from django.contrib import admin
from .models import Post

class PostAdmin(admin.ModelAdmin):
    list_display = ('title', 'slug', 'status','created_on')
    list_filter = ("status",) # This line was added
    search_fields = ['title', 'content']

admin.site.register(Post, PostAdmin)
```

Finally, when creating a post, we would like to pre-populate the slug field with information from the title. A slug is usually constructed by replacing spaces in the title with hyphens (-). Since this is a very common operation in web development, django provides it out of the box for us:

```python
from django.contrib import admin
from .models import Post

class PostAdmin(admin.ModelAdmin):
    list_display = ('title', 'slug', 'status','created_on')
    list_filter = ("status",) # This line was added
    search_fields = ['title', 'content']
    prepopulated_fields = {'slug': ('title',)}
admin.site.register(Post, PostAdmin)
```

There is certainly much more abot the Admin interface that we cannot cover in this course. The way to learn what is available is to keep reading the [Django admin documentation](https://docs.djangoproject.com/en/3.1/ref/contrib/admin/) and experimenting with new features.


