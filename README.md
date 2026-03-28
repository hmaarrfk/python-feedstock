About python-feedstock
======================

Feedstock license: [BSD-3-Clause](https://github.com/conda-forge/python-feedstock/blob/main/LICENSE.txt)

Home: https://www.python.org/

Package license: Python-2.0

Summary: General purpose programming language

Development: https://docs.python.org/devguide/

Documentation: https://www.python.org/doc/versions/

Python is a widely used high-level, general-purpose, interpreted, dynamic
programming language. Its design philosophy emphasizes code
readability, and its syntax allows programmers to express concepts in
fewer lines of code than would be possible in languages such as C++ or
Java. The language provides constructs intended to enable clear programs
on both a small and large scale.

We provide some meta packages for convenience.
To get a CPython flavour, use:

    conda install cpython

To get the freethreading build (i.e. without the Global Interpreter Lock - GIL):

    conda install python-freethreading

To get the default build (i.e. with the GIL):

    conda install python-gil

To enable the use of the experimental JIT compiler in CPython:

    conda install python-jit

or set the environment variable PYTHON_JIT=1. Note that the JIT support
is available for x86_64 builds only.


Current build status
====================


<table>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-cpython-green.svg)](https://anaconda.org/mark.harfouche/cpython) | [![Conda Downloads](https://img.shields.io/conda/dn/mark.harfouche/cpython.svg)](https://anaconda.org/mark.harfouche/cpython) | [![Conda Version](https://img.shields.io/conda/vn/mark.harfouche/cpython.svg)](https://anaconda.org/mark.harfouche/cpython) | [![Conda Platforms](https://img.shields.io/conda/pn/mark.harfouche/cpython.svg)](https://anaconda.org/mark.harfouche/cpython) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-libpython--static-green.svg)](https://anaconda.org/mark.harfouche/libpython-static) | [![Conda Downloads](https://img.shields.io/conda/dn/mark.harfouche/libpython-static.svg)](https://anaconda.org/mark.harfouche/libpython-static) | [![Conda Version](https://img.shields.io/conda/vn/mark.harfouche/libpython-static.svg)](https://anaconda.org/mark.harfouche/libpython-static) | [![Conda Platforms](https://img.shields.io/conda/pn/mark.harfouche/libpython-static.svg)](https://anaconda.org/mark.harfouche/libpython-static) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-python-green.svg)](https://anaconda.org/mark.harfouche/python) | [![Conda Downloads](https://img.shields.io/conda/dn/mark.harfouche/python.svg)](https://anaconda.org/mark.harfouche/python) | [![Conda Version](https://img.shields.io/conda/vn/mark.harfouche/python.svg)](https://anaconda.org/mark.harfouche/python) | [![Conda Platforms](https://img.shields.io/conda/pn/mark.harfouche/python.svg)](https://anaconda.org/mark.harfouche/python) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-python--freethreading-green.svg)](https://anaconda.org/mark.harfouche/python-freethreading) | [![Conda Downloads](https://img.shields.io/conda/dn/mark.harfouche/python-freethreading.svg)](https://anaconda.org/mark.harfouche/python-freethreading) | [![Conda Version](https://img.shields.io/conda/vn/mark.harfouche/python-freethreading.svg)](https://anaconda.org/mark.harfouche/python-freethreading) | [![Conda Platforms](https://img.shields.io/conda/pn/mark.harfouche/python-freethreading.svg)](https://anaconda.org/mark.harfouche/python-freethreading) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-python--gil-green.svg)](https://anaconda.org/mark.harfouche/python-gil) | [![Conda Downloads](https://img.shields.io/conda/dn/mark.harfouche/python-gil.svg)](https://anaconda.org/mark.harfouche/python-gil) | [![Conda Version](https://img.shields.io/conda/vn/mark.harfouche/python-gil.svg)](https://anaconda.org/mark.harfouche/python-gil) | [![Conda Platforms](https://img.shields.io/conda/pn/mark.harfouche/python-gil.svg)](https://anaconda.org/mark.harfouche/python-gil) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-python--jit-green.svg)](https://anaconda.org/mark.harfouche/python-jit) | [![Conda Downloads](https://img.shields.io/conda/dn/mark.harfouche/python-jit.svg)](https://anaconda.org/mark.harfouche/python-jit) | [![Conda Version](https://img.shields.io/conda/vn/mark.harfouche/python-jit.svg)](https://anaconda.org/mark.harfouche/python-jit) | [![Conda Platforms](https://img.shields.io/conda/pn/mark.harfouche/python-jit.svg)](https://anaconda.org/mark.harfouche/python-jit) |

Installing python
=================

Installing `python` from the `mark.harfouche/label/python_debug` channel can be achieved by adding `mark.harfouche/label/python_debug` to your channels with:

```
conda config --add channels mark.harfouche/label/python_debug
conda config --set channel_priority strict
```

Once the `mark.harfouche/label/python_debug` channel has been enabled, `cpython, libpython-static, python, python-freethreading, python-gil, python-jit` can be installed with `conda`:

```
conda install cpython libpython-static python python-freethreading python-gil python-jit
```

or with `mamba`:

```
mamba install cpython libpython-static python python-freethreading python-gil python-jit
```

It is possible to list all of the versions of `cpython` available on your platform with `conda`:

```
conda search cpython --channel mark.harfouche/label/python_debug
```

or with `mamba`:

```
mamba search cpython --channel mark.harfouche/label/python_debug
```

Alternatively, `mamba repoquery` may provide more information:

```
# Search all versions available on your platform:
mamba repoquery search cpython --channel mark.harfouche/label/python_debug

# List packages depending on `cpython`:
mamba repoquery whoneeds cpython --channel mark.harfouche/label/python_debug

# List dependencies of `cpython`:
mamba repoquery depends cpython --channel mark.harfouche/label/python_debug
```




Updating python-feedstock
=========================

If you would like to improve the python recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`mark.harfouche` channel, whereupon the built conda packages will be available for
everybody to install and use from the `mark.harfouche` channel.
Note that all branches in the conda-forge/python-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks, and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@chrisburr](https://github.com/chrisburr/)
* [@isuruf](https://github.com/isuruf/)
* [@jakirkham](https://github.com/jakirkham/)
* [@katietz](https://github.com/katietz/)
* [@mbargull](https://github.com/mbargull/)
* [@msarahan](https://github.com/msarahan/)
* [@ocefpaf](https://github.com/ocefpaf/)
* [@pelson](https://github.com/pelson/)
* [@scopatz](https://github.com/scopatz/)
* [@xhochy](https://github.com/xhochy/)

