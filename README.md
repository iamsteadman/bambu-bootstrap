# Bambu Bootstrap

Use Twitter's [Bootstrap](http://twitter.github.com/bootstrap/) CSS framework to build your app. All the views Bambu uses all extend a base template which you create, that can be based on a skeleton Bootstrap template. Shortcut tags let you easily add breadcrumb trails and icons to your apps.

## About Bambu Bootstrap

Bambu Tools is a set of reusable Django apps and utility packages that help prototyping and building web apps
easier. To a degree, this starts with the front-end scaffolding. Bambu Bootstrap provides a base template along
with a set of useful tags and filters that make building web apps using this framework easier.

## About Bambu Tools 2.0

This is part of a toolset called Bambu Tools. It's being moved from a namespace of `bambu` to its own
'root-level' package, along with all the other tools in the set. If you're upgrading from a version prior
to 2.0, please make sure to update your code to use `bambu_bootstrap` rather than `bambu.bootstrap`.

## Installation

Install the package via Pip:

```
pip install bambu-bootstrap
```

Add it to your `INSTALLED_APPS` list and add Bootstrap and Font-Awesome to your `BOWER_INSTALLED_APPS`
list (see the [django-bower documentation](http://django-bower.readthedocs.org/en/latest/)) for details on
managing static files through Bower.

```python
INSTALLED_APPS = (
    ...
    'djangobower',
    'bambu_bootstrap'
)

BOWER_INSTALLED_APPS = (
    ...
    'bootstrap',
    'fontawesome'
)
```

Remember to run `python manage.py bower install` and `python manage.py collectstatic`.

## Basic usage

Within your project, start with a template called `base.html`. This should extend the Bootstrap base template,,
at `bootstrap/base.html`.

Use the `extra_head` block to specify stylesheets or script tags that must, by necessity live in the head of
your document.

Use the `content` block for the main content of your page.

Use the `javascript` block to specify JavaScript that can run at the very bottom of the page.

## Documentation

Full documentation can be found at [ReadTheDocs](http://bambu-bootstrap.readthedocs.org/).

## Questions or suggestions?

Find me on Twitter (@[iamsteadman](https://twitter.com/iamsteadman))
or [visit my blog](http://steadman.io/).