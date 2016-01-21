Kiron CodeSchool Website
=======

The Kiron CodeSchool website, http://codeschool.kiron.university, is programmed with simplicity and speed in mind. The scope of the site is relatively small, allowing this to be done. The site uses HTML/CSS as well as javascript and a little PHP. Bootstrap is used to make the site responsive. Additionally, a Google Form is integrated into the site using an iframe.

Getting Started
----------------
To begin with, clone the repository:

    git clone git@github.com:kironuniversity/kironventures

In this directory you will see the public directory, which houses the website.

Setting up your local environment
-------
The Kiron Ventures website uses PHP for including files. This means that you will have to use a mock server on your computer in order to view changes. The easiest way is usually MAMP (https://www.mamp.info) - the free version suffices.

In preferences, change the document root to be the *public* folder of the repository locally. You should be able to then click on start servers and see the page at http://localhost:8888/ in the browser. Changes made to documents in *public* will show up there on refresh.


Code Structure
-------
The code itself is relatively straight forward.

**CSS**
There is lots of extra css in the css forlder but only few files are actually in use.

**PHP**


**JS**

The little JS used here is loaded at the very end, since it is not needed for the DOM. We use the script *head.load.min.js* to manage our JS. This script allows us to load our JS as non-render blocking but still in a specific order. All of the JS (except for head.load itself) will load asynchronously but in the specified ordered. Quicker rendering times but no screwups.

**iframes**

The form for application was made with google forms and embedded here using an iframe. The google forms code is ours.

Making Updates to the Site
-------
The standard procedure for committing to GitHub should be used. There is at the moment only one branch, the master branch. If you aren't yet familiar with Git, have a quick look. For this simple project, you will probably only need clone, pull, add, status, commit and push.

sThere is no auto-deploy for this site currently. Accordingly, the way to update the site is to push your changes and tell Adam or Juan that you would like to make an update. What one of us will do is the following:

    ssh forge@46.101.223.64
    cd kironventures.com/kironventures
    git pull
    rsync -av public/ ../public/.

This is the procedure to login to the server, go to the proper directory, pull the changes from git, and copy the changes to the public directory (which is what the site runs off of).
