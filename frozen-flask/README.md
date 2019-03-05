`dnf install python-flask python-frozen-flask python-flask-assets python-rjsmin python-cssmin python-flask-babel`

The templates are almost unchanged from https://pagure.io/fedora-websites-jinja-poc/ except for adding in the code for asset bundling.

The site can be run in two ways:

* Dynamically with `flask run --reload --debugger`
* Statically with `python main.py` and loading the 'build' directory.

To test the static generation and make sure it does what you expect, build it as per above, and then from the new `build` directory, run `python -mSimpleHTTPServer` and go to localhost:8000 in a browser.