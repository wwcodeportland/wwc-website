# DJANGO
## "The web framework for perfectionists with deadlines"

Django is a web development framework built in Python. Of all the popular Python web frameworks, it takes the most "batteries included" approach -- that is, it's easiest to get up and running with minimal work, and a lot of choices are made for you.

This document will provide resources to get up and running with Django quickly, as well as some guidelines on how it should be used in this particular project.

If you don't understand what anything in this document means, ask a fellow contributor for help, and feel free to submit pull requests with any changes you think would make it clearer.
## Project Guidelines
> NOTE: these are my (emcain's) opinions on how we should approach Django development to make it as friendly as possible for beginners. I welcome disagreement and feedback on these; I think we should agree on some basic standards so that contributors to the project can have a clear path forward, but I'm not attached to the particular details as I'm writing them here.

* Use function-based views, not class-based views.
* Use the built-in frameworks for testing and template rendering--they work fine and there's no need to replace them.
* Keep app names consistent with the URL roots for those apps--so if I have an app called `blog`, URLs in that app should start with `/blog`.
* Don't write custom template tags unless you have a really good reason, and if you do, document how to use them thoroughly.
* Create one base template to use for most pages and use it consistently.
* Don't use more than one level of template inheritance in most cases, and if you do, document it thoroughly.
* Use the [pep-8](https://www.python.org/dev/peps/pep-0008/) style guide for Python.
  * Extra bonus points for adding git hooks that enforce pep-8.
  * You can check that your code conforms to pep-8 with the [pycodestyle](https://pypi.python.org/pypi/pycodestyle/) package.
  * Exception: migrations files are automatically generated and won't conform to the line length limits. This is ok.
* Use Django 1.11. Make sure any documentation you read is for this version.
* Use `pip` for package management, and store the packages used in a `requirements.txt` file. This will be much easier to manage if you create a virtualenv for the project.
* Put template files for a given app in a folder named `templates` in that app. Put shared template files in a folder called `templates` in the Django project root.

## Django basics

The following sections are intended for people who have some familiarity with web development and want to get started on contributing quickly. If you're new to web development, the following tutorials will get you up to speed quickly.

* [Django Girls Tutorial](https://tutorial.djangogirls.org/) - available in many languages, easy for complete beginners to use.
* [Django First Steps](https://docs.djangoproject.com/en/1.11/#first-steps) - more detailed introductory materials on the Django website.

If you've gone through one of these tutorials and want to review the basics for adding a page to a site, see the [Django Page Checklist](https://emcain.github.io/django-page-checklist/).

### MVC framework

While Django's architecture fits pretty well into the [Model-View-Controller](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller) concept, people who are used to other web frameworks may be confused by its naming convention. The concept of the "view" layer is represented by two parts, the `views.py`  and any template files. `views.py` generates the data that is used to render a template, and the template files outline the structure of the HTML that will be rendered and passed to the client.

> NOTE: templates don't have to be HTML -- they can theoretically be used to create XML, JSON, or any other format -- but in most use cases they will be HTML.

[This section of the Django FAQ](https://docs.djangoproject.com/en/1.11/faq/general/#django-appears-to-be-a-mvc-framework-but-you-call-the-controller-the-view-and-the-view-the-template-how-come-you-don-t-use-the-standard-names) goes into more detail. If this is confusing to you, just remember that in Django, the word "view" refers to a specific part of the framework that is related to the "view" layer in MVC, but it does not correspond perfectly.

### Templates

Please see these resources to learn how Templates work in Django.

* [Django Girls](https://tutorial.djangogirls.org/en/django_templates/) - templates
* [Django Project](https://docs.djangoproject.com/en/1.11/intro/tutorial03/) - views and templates

### URLs

The `urls.py` file in a given app routes requests to views within that app. It matches the request URL to an URL pattern (expressed as a [regular expression](https://docs.python.org/3/howto/regex.html)), extracts any parameters, and calls the corresponding function in `views.py`. See [this article](https://docs.djangoproject.com/en/1.11/topics/http/urls/) for more info.
