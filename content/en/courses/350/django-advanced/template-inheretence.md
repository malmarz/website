---
# Page title
title: Template Inheretence

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: Template Inheretence

# Date page published
date: 22022-01-10T17:21:40Z021-12-23

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 11

draft: False


---

Template inheretence allows you to reuse templates. The idea is you create a base template that holds the main look and feel of the website. Every template you then create must inheret from that base template. The main advantage of this approach is if you want to make a change to the whole look and feel of the website, you just modify the base template.

## Creating the base.html tempalte

Under the templates directory in your app, create a `base.html` file. Create the basic html structure there but take note the blog content tag:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    {% block content %}
    {% endblock %}
</body>
</html>
```

The `{% block content %}` tag determines the area in the base template where content will go. So every template we create in our app we will do two things when using template inheretence:

1. We add `{% extends 'base.html'%}` at the top of the template
2. You include the `{% block content %}` tage in your template and put your content for the view inside it. Django will use the base.html template and put any content you wire in your template in inside the `block content` part.

Here is an example of how the `poll_list.html` template will look like:

```html
{% extends 'base.html'%}

{% block content %}
  <h1>Latest Posts</h1>

    <ul>
        {% for p in post_list %}
        <li>
            {% if p.slug %}
            <a href="{% url 'post_details_slug' p.slug %}">
                {% else %}
            <a href="{% url 'post_details' p.id %}">
            {% endif %}
            {{ p.title }}: 
            </a>
            <strong>Created {{ p.created_at|timesince }} ago </strong>, status is {{ p.get_status_display }},
            comments: {{ p.comment_set.count }}
            | <a href="{% url 'delete_post' p.id %}">delete</a>
        </li>
        {% endfor %}
    </ul>
{% endblock %}
```

Notice, everything that will show in all views, we put in `base.html`, anything that is specific to the current view, we place inside the content tag in the view template. Keep in mind, that you can have as many blocks as you want in base and can name them as you like. The block is basically a named area in your website that you want django to place HTML content in, just like the named slots in python fstrings, but for templates and to place large blocks of content instead of the content of a single variable.