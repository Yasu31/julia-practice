# Conda
It's not exactly about Julia, but since this topic pops up everywhere might as well learn it...

## [Getting started with conda](https://conda.io/docs/user-guide/getting-started.html)
First [install Anaconda](https://www.anaconda.com/download/#macos)
>Conda is an open source package management system and environment management system that runs on Windows, macOS and Linux. Conda quickly installs, runs and updates packages and their dependencies. Conda easily creates, saves, loads and switches between environments on your local computer. It was created for Python programs, but it can package and distribute software for any language.

### Anaconda and Conda


### creating separate environments
To create environment *snowflakes* and install package BioPython, `$ conda create --name snowflakes biopython`. To use (activate) that, `source activate snowflakes`

### managing Packages
`conda search beautifulsoup4` to search in Anaconda repository, `conda install beautifulsoup4` to install. Check list of installed programs with `conda list`

## Installation
>You do not need to uninstall other Python installations or packages in order to use conda. Even if you already have a system Python, another Python installation from a source such as the macOS Homebrew package manager and globally installed packages from pip such as pandas and NumPy, you do not need to uninstall, remove, or change any of them before using conda.
Install Anaconda or Miniconda normally, and let the installer add the conda installation of Python to your PATH environment variable. There is no need to set the PYTHONPATH environment variable.

`Yasunoris-MacBook-Pro:~ yasu$ which python
/Users/yasu/anaconda3/bin/python`

## Configuration
`.condarc` configuration file. Use `conda config` command to edit it. `conda config --help` for list of commands

can change channel locations. What are "channels"??
### Channels
>The locations of the repositories where conda looks for packages. Channels may point to a Cloud repository or a private location on a remote or local repository that you or your organization created. The conda channel command has a default set of channels to search, beginning with https://repo.continuum.io/pkgs/, which you may override, for example, to maintain a private or internal channel. These default channels are referred to in conda commands and in the .condarc file by the channel name “defaults.”

# Resources
* [What is the difference between pip and conda?](https://stackoverflow.com/questions/20994716/what-is-the-difference-between-pip-and-conda)
* [Conda cheat sheet](https://conda.io/docs/_downloads/conda-cheatsheet.pdf)
* [Glossary](https://conda.io/docs/glossary.html#channels)
