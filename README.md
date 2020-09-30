About atom-ml
=============

Home: http://github.com/tvdboom/ATOM

Package license: MIT

Feedstock license: BSD-3-Clause

Summary: A Python AutoML tool for fast exploration and experimentation of supervised machine learning pipelines.

There is no magic formula in data science that can tell us which type of machine
learning algorithm will perform best for a specific use-case. Different models
are better suited for different types of data and different problems. At best,
you can follow some rough guide on how to approach problems with regard to which
model to try on your data, but these are often more confusing than helpful. Best
practices tell us to start with a simple model (e.g. linear regression) and build
up to more complicated models (e.g. logistic regression -> random forest ->
multilayer perceptron) if you are not satisfied with the results. Unfortunately,
different models require different data cleaning steps, different type/amount of
features, tuning a new set of hyperparameters, etc. Refactoring the code for this
purpose can be quite boring and time consuming. Because of this, many data
scientists end up just using the model best known to them and fine-tuning this
particular model without ever trying different ones. This can result in poor
performance (because the model is just not the right one for the task) or in poor
time management (because you could have achieved a similar performance with a
simpler/faster model).

ATOM is here to help us solve these issues. With just a few lines of code, you
can perform basic data cleaning steps, select relevant features and compare the
performance of multiple models on a given dataset. ATOM should be able to provide
quick insights on which algorithms perform best for the task at hand and provide
an indication of the feasibility of the ML solution.

It is important to realize that ATOM is not here to replace all the work a data
scientist has to do before getting his model into production. ATOM doesn't spit
out production-ready models just by tuning some parameters in its API. After
helping you to determine the right model, you will most probably need to fine-tune
it using use-case specific features and data cleaning steps in order to achieve
maximum performance.

So, this sounds a bit like AutoML, how is ATOM different than auto-sklearn or
TPOT? Well, ATOM does AutoML in the sense that it helps you find the best model
for a specific task, but contrary to the aforementioned packages, it does not
actively search for the best model. It simply runs all of them and let you pick
the one that you think suites you best. AutoML packages are often black boxes: if
you provide data, it will magically return a working model. Although it works
great, they often produce complicated pipelines with low explainability, hard to
sell to the business. In this, ATOM excels. Every step of the pipeline is
accounted for, and using the provided plotting methods, it’s easy to demonstrate
why a model is better/worse than the other.


Current build status
====================


<table><tr><td>All platforms:</td>
    <td>
      <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=10822&branchName=master">
        <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/atom-ml-feedstock?branchName=master">
      </a>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-atom--ml-green.svg)](https://anaconda.org/conda-forge/atom-ml) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/atom-ml.svg)](https://anaconda.org/conda-forge/atom-ml) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/atom-ml.svg)](https://anaconda.org/conda-forge/atom-ml) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/atom-ml.svg)](https://anaconda.org/conda-forge/atom-ml) |

Installing atom-ml
==================

Installing `atom-ml` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
```

Once the `conda-forge` channel has been enabled, `atom-ml` can be installed with:

```
conda install atom-ml
```

It is possible to list all of the versions of `atom-ml` available on your platform with:

```
conda search atom-ml --channel conda-forge
```


About conda-forge
=================

[![Powered by NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](http://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/)
and [TravisCI](https://travis-ci.com/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](https://anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating atom-ml-feedstock
==========================

If you would like to improve the atom-ml recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/atom-ml-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@tvdboom](https://github.com/tvdboom/)

