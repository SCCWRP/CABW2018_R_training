# Set Up

Thanks for your interest in learning R.  For the workshop, we will be using [RStudio](https://www.rstudio.com/) as our interface to R.  In order to participate in this workshop you will need to make sure you have R and RStudio installed on your laptop.

Thanks to the [USGS-R Training group](https://owi.usgs.gov/R/training.html) and [Data Carpentry](https://datacarpentry.org/R-ecology-lesson/index.html) for making their installation materials available.  The following instructions come directly from their materials, with a few minor edits to help you get all set up for the workshop.

# Install R and RStudio

**R** and **RStudio** are separate downloads and installations. R is the underlying statistical computing environment, but using R alone is no fun. RStudio is a graphical integrated development environment (IDE) that makes using R much easier and more interactive. *You need to install R before you install RStudio*.

## *Windows*: Download and install R
Go to [CRAN and download](https://cran.rstudio.com/bin/windows/base/) the R installer for Windows. Make sure to choose the latest stable version (v3.5.1 as of Sept 2018).

Once the installer downloads, Right-click on it and select "Run as administrator". 

Type in your credentials and click yes (or if you don't have administrator access have your IT rep install with Admin privileges).

![](figure/install_open_as_admin.png#inline-img "run as admin")

You can click next through the standard dialogs and accept most defaults. But at the destination
screen, please verify that it is installing it to C:\Program Files\R (version number may vary)

![](figure/install_destination.png#inline-img "install destination screen")

At the "Select Components" screen, you can accept the default and install both 32-bit and 64-bit versions.

![](figure/install_arch_window.png#inline-img "select architecture")

At this screen, uncheck 'Create a desktop icon' because non-admin users in Windows will be unable to delete it.

![](figure/install_tasks.png#inline-img "uncheck desktop icon")


## *Windows*: Download and install RStudio
[](https://www.rstudio.com/products/rstudio/download/)

Double-click the installer. It will ask for your administrator credentials to install (you might need to have your IT rep install again). 

Accept all the default options for the RStudio install.

![](figure/install_rstudio.png#inline-img "RStudio install screen")

## *macOS*: Download and install R

 - Download and install R from the CRAN website for Mac [here](https://cran.r-project.org/bin/macosx/). 
 - Select the `.pkg` file for the latest R version
 - Double click on the downloaded file to install R
 - It is also a good idea to install [XQuartz](https://www.xquartz.org/) (needed by some packages)

## *macOS*: Download and install RStudio

 - Go to the [RStudio](https://www.rstudio.com/products/rstudio/download/#download) download page
 - Under Installers select **RStudio x.yy.zzz - Mac OS X 10.6+ (64-bit)** (where x, y, and z represent version numbers)
 - Double click the file to install RStudio
 - Once it’s installed, open RStudio to make sure it works and you don’t get any error messages.


# Check Install

## Open RStudio
Once installed, RStudio should be accessible from the start menu.  Start up RStudio.  Once running it should look something like:

![](figure/rstudio.png#inline-img "RStudio window")

## Find "Console" window
By default the console window will be on the left side of RStudio.  Find that window.  It will looking something like:  

![](figure/rstudio_console.png#inline-img "RStudio console")

## Copy and paste the code
Click in the window and paste in the code from below:


```r
version$version.string
```

## Verify your installed R version

Ideally you should be running the latest stable release (`v3.5.1` as of Sept 2018). If you have an older version, please install the newest version using the instructions above.

Here is what my R version looks like.

```
## [1] "R version 3.5.1 (2018-07-02)"
```

# Add Packages

Install packages available for all R users from [CRAN](https://cran.r-project.org/) by pasting the following code and hitting `ENTER`.


```r
install.packages("tidyverse")
```

If you see 

![](figure/personal_library_dialog.png#inline-img "dialog box behind")

That's OK! There’s a dialog box hiding behind RStudio asking if you want to create a personal folder in your Documents folder.  Click *Yes*. It will look something like this when done:

![](figure/general_pkg_output.png#inline-img "console output")

# Grab the Sample Datasets

We'll be working with a chemistry dataset and metadata from the Bight for many of our examples. Please download the chemistry dataset [here](https://github.com/SCCWRP/SCCWRP_R_training/blob/master/data/B13%20Chem%20data.xlsx?raw=true) and the metadata [here](https://github.com/SCCWRP/SCCWRP_R_training/blob/master/data/Master%20Data%20-%20Station%20Info.xlsx?raw=true).  Make sure you have access to these data on the day of training.

<!-- may want to make .csv versions of these data so folks can see what it looks like and download more easily? Or is this and older version, we'll be using the calipsa/ascidat data in the CABW2018_R_training repo? -->

## Exercise 1
Just to make sure everything is working do the following:

1. Open up RStudio.
2. Find the "Console."  This is usually the left part RStudio.
3. In the "Console", find the R Prompt.
4. Type in (copy and paste from here will also work) the following commands at the R Prompt and hit return.  


```r
"tidyverse" %in% installed.packages()
```

The end result should look something like:

![](figure/install_success.jpg)


