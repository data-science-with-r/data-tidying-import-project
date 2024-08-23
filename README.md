# data-tidying-import-project

# Project instructions


> [!IMPORTANT]
>
> ### 
>
> This is the final project for course 2. This will not be graded, and is
> intended to provide you with the opportunity to test the skills you’ve
> acquired throughout the course in a less structured environment.
> This project is also structured for you to host on a webpage and link as proof of work on your resume or CV. 
>
> Rubric items can be found at the end of the README in the Self rubric section to help self-assessment of your project. Do not expand the rubric items until you have finished a draft of your project.
>
## Before you start

Please complete the following steps before getting started if you have not downloaded and configured Git. If you have already completed these steps from course 1, please clone this repo and skip to the Instructions section.

### Download Git

Note, if you are on Windows or Linux, you will need to install Git.  If you do not have git installed, please do so: 

Windows ->  https://git-scm.com/download/win

Linux   ->  https://git-scm.com/download/linux

### Configure git with RStudio 

In the console, run the following: 
```r
install.packages("usethis")

usethis::use_git_config(
  user.name = "Your name", 
  user.email = "Email associated with your GitHub account"
 )
```
Please make sure that you replace "YourName" with your actual name, and "Email associated with your GitHub account" with your email used for your GitHub account. 

### Create and authenticate your personal access token 

In the console, run the following to geneate your personal access token (PAT) 

```r
usethis::create_github_token()
```

Next, run the following and paste your PAT in:

```r
gitcreds::gitcreds_set()
```

### Getting started 

Once you restart R, you will be able to clone this project repository and get working! To clone this project: 
- Click the green code button on the repo
- Copy the HTTPS
- Open a new project in RStudio
- Click version control and then Git
- Paste the copied HTTPS in the Repository URL box.
- Name the project directory
- Browse and select where this project will be saved
- Click create project!

## Instructions

This final project consists of an exploratory data analysis and write up
of results you discover. The data sets you will be working with can be found in the data folder. Your write up, in index.qmd, will explore (at least) two questions.

## Description

**Inflation in the US**

<img align="right" src="images/inflation.png" width="300" height="180" />

The Organisation for Economic Co-operation and Development defines inflation as follows:

> Inflation is a rise in the general level of prices of goods and services that households acquire for the purpose of consumption in an economy over a period of time.
>
> The main measure of inflation is the annual inflation rate which is the movement of the Consumer Price Index (CPI) from one month/period to the same month/period of the previous year expressed as percentage over time.
>
> Source: [OECD CPI FAQ](https://www.oecd.org/sdd/prices-ppp/consumerpriceindices-frequentlyaskedquestionsfaqs.htm#1)

CPI is broken down into 12 divisions such as food, housing, health, etc.

The data you will need to explore US inflation are spread across two files:

-   `us-inflation.csv`: Annual inflation rate for the US for 12 CPI divisions. Each division is identified by an ID number.
-   `cpi-divisions.csv`: A "lookup table" of CPI division ID numbers and their descriptions.



