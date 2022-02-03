
# MaterialsAtlas Documentation

This is a place for all documentation relating to the
[MaterialsAtlas](http://materialsatlas.org) (MAtalas):

- Foundations: concepts in materials and data science for materials discovery
- Algorithms: key materials informatics algorithms
- Case Studies: Examples of materials discovery using our web apps
- Tutorial: Using our web apps, application programming interface (API), and open source code.
- Contribution: Developer guides and design specifications

If you notice an error or omission, please post an [issue](https://github.com/usccolumbia/materialsatlas/issues/new) or suggest an
edit to us via a Pull Request.

Thanks,
MaterialsAtlas Team

# Contributing

We use [MkDocs](https://www.mkdocs.org/), a static site generator for project documentation. We also use the
[mkdocs-material](https://squidfunk.github.io/mkdocs-material/) theme for styling.

## Up and running

Fork this repository and then clone it to your computer.

Create a Python 3 environment for this project and activate it. Example flow using `conda`:

```
$ conda create -n madocs python=3
$ conda activate madocs
```

Navigate to the folder of your cloned repository, and install dependencies:

```
(madocs)$ pip install -r requirements.txt
```

Start the development server:

```
(madocs)$ mkdocs serve
```

Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/) to preview the site and see changes as you make them.

Create a new git branch to record any changes. When you push your branch to GitHub, you can then initiate a Pull
Request against the `master` branch of this repo.


### Declaration

Some of the documentation sentences and structures are adapted from Materials Project documentation https://docs.materialsproject.org/. They are our role model -:)
