---
title: Setup
---

## Preparations

Data Carpentry's teaching is hands-on, and to follow this lesson
learners must have R and RStudio installed on their computers. They also need
to install a number of R packages, create directories, and download
files.

To avoid troubleshooting during the lesson, learners should follow the
instructions below to download and install everything beforehand.

## Install R and RStudio

R and RStudio are two separate pieces of software:

- **R** is a programming language that is especially powerful for data
  exploration, visualization, and statistical analysis
- **RStudio** is an integrated development environment (IDE) that makes using
  R easier. In this course we use RStudio to interact with R.

::::::::::::: discussion

### Installation Instructions

If you don't already have R and RStudio installed, follow the appropriate instructions below. You have to install R before you install RStudio.

:::::::::::::::::::::::::

::::::: solution

### University of Auckland machines

- Install R from Software Center (Windows) or Self Service (Mac).
- Once complete, install RStudio from Software Center (Windows) or Self Service (Mac).

::::::::::::::::

::::::: solution

### Personal machines

**Windows**
- Download R from the
  [CRAN website](https://cran.r-project.org/bin/windows/base/release.htm).
- Run the `.exe` file that was just downloaded
- Go to the [RStudio download page](https://posit.co/download/rstudio-desktop/#download)
- Under *All Installers*, download the RStudio Installer for Windows.
- Double click the file to install it
- Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.

**Mac**
- Download R from
  the [CRAN website](https://cran.r-project.org/bin/macosx/).
- Select the `.pkg` file for the latest R version
- Double click on the downloaded file to install R
- It is also a good idea to install [XQuartz](https://www.xquartz.org/) (needed
  by some packages)
- Go to the [RStudio download page](https://posit.co/download/rstudio-desktop/#download)
- Under *All Installers*, download the RStudio Installer for MacOS.
- Double click the file to install RStudio
- Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.

::::::::::::::::

::::::: solution


### Linux

- Follow the instructions for your distribution
  from [CRAN](https://cloud.r-project.org/bin/linux), they provide information
  to get the most recent version of R for common distributions. For most
  distributions, you could use your package manager (e.g., for Debian/Ubuntu run
  `sudo apt-get install r-base`, and for Fedora `sudo yum install R`), but we
  don't recommend this approach as the versions provided by this are
  usually out of date. In any case, make sure you have at least R 3.3.1.
- Go to the
  [RStudio download page](https://posit.co/download/rstudio-desktop/#download)
- Under *All Installers*, select the version that matches your distribution and
  install it with your preferred method (e.g., with Debian/Ubuntu `sudo dpkg -i rstudio-YYYY.MM.X-ZZZ-amd64.deb` at the terminal).
- Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.

::::::::::::::::

## Update R and RStudio

Once you have R and RStudio installed, it's a good idea to keep both up to date:

- For University of Auckland machines: Check Software Center or Self Service to see if there is an update for R or RStudio.
- For personal machines: Get the latest version of R from CRAN and install over the current version. To update RStudio to the latest version, open RStudio and click on
`Help > Check for Updates`. If a new version is available follow the
instruction on screen. By default, RStudio will also automatically notify you
of new versions every once in a while.
- After installing a new version of R, you will have to reinstall all your packages
  with the new version. For Windows, there is a package called `installr` that can
  help you with upgrading your R version and migrate your package library.

## Install required R packages

During the course we will need a number of R packages. Packages contain useful
R code written by other people. We will use the
`tidyverse` package.

To install these packages, open RStudio and copy and paste the following
command into the console window (look for a blinking cursor on the bottom left),
then press <kbd>Enter</kbd> (Windows and Linux) or <kbd>Return</kbd> (MacOS)
to execute the command.

```r
install.packages("tidyverse")
```

Alternatively, you can install packages using RStudio's graphical user
interface by going to `Tools > Install Packages` and typing the names of the
packages separated by a comma.

R tries to download and install the package on your machine.
When the installation has finished, you can try to load the
package by pasting the following code into the console:

```r
library(tidyverse)
```

If you do not see an error like `there is no package called ‘...'` you are good
to go!

## Updating R packages

To update the packages that you have installed, click `Update` in the
`Packages` tab in the bottom right panel of RStudio, or go to
`Tools > Check for Package Updates...`.

Sometimes, package updates introduce changes that break your old code,
which can be very frustrating. To avoid this problem, you can use a package
called `renv`. It locks the package versions you have used for a given project
and makes it straightforward to reinstall those exact package version in a
new environment, for example after updating your R version or on another
computer. However, the details are outside of the scope of this lesson.

## Download the data

We will download the data directly from R during the lessons. However, if you
are expecting problems with the network, it may be better to download the data
beforehand and store it on your machine.

The data files for the lesson can be downloaded manually here: [https://doi.org/10.6084/m9.figshare.1314459](https://doi.org/10.6084/m9.figshare.1314459)
