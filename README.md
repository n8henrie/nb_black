# nb_black

## n8henrie fork notes

NB: This is a fork of https://github.com/dnanhkhoa/nb_black that has been
minimally modified to allow me to set a custom line length. Brief discussion:
https://github.com/dnanhkhoa/nb_black/issues/10#issuecomment-649744254

For this fork:

- installation: `pip install git+https://github.com/n8henrie/nb_black`
- use with default settings: `%load_ext lab_black`
- alternatively, use with custom line length:
    ```python
    import lab_black

    lab_black.load_ipython_extension(get_ipython(), line_length=79)
    ```

END n8henrie fork notes

[![PyPI](https://img.shields.io/pypi/v/nb_black.svg)](https://pypi.org/project/nb-black/)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/nb_black.svg)](https://pypi.org/project/nb-black/)

A simple extension for Jupyter Notebook and Jupyter Lab to beautify Python code automatically using **[Black](https://github.com/psf/black)**.

Please note that since the **Black** package only supports Python 3.6+, so **[YAPF](https://github.com/google/yapf)** package will
be used for the lower versions. If you edit the code while running the cell, the formatting is
not submitted to the Jupyter notebook and instead silently suppressed, so you have to stick with
the edited, but unformatted code.

## Installation

You can install this package using [pip](http://www.pip-installer.org):

```
$ [sudo] pip install nb_black
```

## Usage

For Jupyter Notebook:

```
%load_ext nb_black
```

For Jupyter Lab:

```
%load_ext lab_black
```

Just put this code into the first cell in your Notebook, and that's all. :)
