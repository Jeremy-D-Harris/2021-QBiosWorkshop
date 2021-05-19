2021 QBios Workshop - Building interactive dashboards
================
Aroon T. ChandeLavanya Rishishwar

## Getting started

To get started, clone this repository in the command line or download
the ZIP file and open the **`GaTech-QBiosWorkshop-20210518.Rproj`** file
with RStudio

``` bash
# clone the repo
git clone git@github.com:appliedbinf/2021-QBiosWorkshop.git
cd 2021-QBiosWorkshop
```

We will also be using RStudio Connect and the
[ShinyApps.io](https://www.shinyapps.io/ "shinyapps.io") platform.
Please make a free account before the session. You will need your
[token](https://www.shinyapps.io/admin/#/tokens) to link RStudio with
the ShinyApps.io platform.

## Setting up your environment

### Installing the R dependencies

There are a number of R packages that we will need today to build our
dashboards. Please run the below code in your Rstudio console window.

``` r
packages <- c("shiny", "deSolve")
install.packages(packages)
```

### Linking ShinyApps

To link your [ShinyApps.io](https://www.shinyapps.io/ "shinyapps.io")
profile with RStudio, visit your
[tokens](https://www.shinyapps.io/admin/#/tokens) page and run the
provided code snippet (example below) in your RStudio console.

``` r
rsconnect::setAccountInfo(name = 'appliedbinf',
                          token = 'alongtokenstringhere',
                          secret = 'supersecretsecretstringhere')
```

## Example code

We’ve provided a series of Shiny code samples in the **`examples`**
folder:

``` bash
examples/
├── 00_HelloWorld.R
├── 01_HelloSliders.R
├── 02_HelloPlots.R
├── 03_HelloInteractions.R
├── 04_MoreInteractions.R
├── 05_OrganizingUI.R
├── 06_HelloNavbar.R
├── 07_NavBarApp.R
└── 08_SIRModel.R
```

As the file numbers increase, so does the complexity of the application.
**`00_HelloWorld.R`** is the simplest Shiny application and prints a
simple “Hello World!” example. **`08_SIRModel.R`** is a full fledged
SIRD application, but not much has been done to make it pretty or user
friendly.
