# Building front-ends with PatternLab
Abstract about what we will be covering in the workshop

## Prerequisites
* Bring your own laptop
* Make sure Git is installed and available on command line. Install from [https://git-scm.com/downloads](https://git-scm.com/downloads)
* Node JS with npm must be installed and available on command line. Install from: https://nodejs.org/
* Install text editor of choice, preferrably an editor with directory browser (Sublime, Atom and WebStorm are all good alternatives)
* We will not go into the details about npm or gulp, if you are interested in how they work, please checkout the exercises from the js-infrastructure session: https://github.com/nerdschoolbergen/js-infrastructure

## Introduction
Write a short intro

## Agenda
* Pizza
* 30ish minutes introduction to front-end challenges, style guides/design systems and Pattern Lab
* Forking git repository and get it running on local computer
* Something
* Something else
* Final step

## Getting started
We will start with creating your own fork of this repository.
Make sure you're logged in and click the Fork button up right.
Clone the repository to your local computer by opening command line, navigate to the folder you wish to work from, and type `git clone <Your new repo url>`

Navigate to the repository folder and run the following commands:

Install gulp on command line:

`npm install -g gulp`

Install application dependencies:

`npm install`

Once the repository is properly downloaded, open the repository using your favorite text editor.

Explain folder structure

Explain dependencies installed?

Run Pattern lab:

`gulp serve`

This executes one of the main gulp tasks which compiles our solution. The task starts up a local web server that hosts the solution and the task will keep running and listen for changes on certain files within our solution.

The application will now open in your default browser at url: [http://localhost:3000](http://localhost:3000).

Try interracting a bit with the site
