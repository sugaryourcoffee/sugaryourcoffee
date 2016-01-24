#Introduction
This document describes the setup of a 1&1 web space hosting and creation. The
steps we will take are listed below

* Create a file structure on the development machine
* Describe the intent and content of the internet presentation
* Develop the web pages
* Deploy the application

#Create the file structure on the development machine
We will have different types of files that we want to organize in our project
directory. Following tree shows the final directory structure

    secondhand.de
    |- bower_components/
    |- doc/
    |- web/
    |  |- assets/
    |  |  | - css
    |  |  | - fonts
    |  |  | - js
    |  |- images/
    |  |- shared/
    |  |- index.shtml

    $ mkdir -p web/{assets,images,shared}
    $ mkdir doc

The web directory contains the files that will be deployed.  The `shared` 
directory will contain files that are used in several pages, as header and 
footer. The directory `bower_components` will be created later when we install 
Bootstrap.

We will host our source code at Github. We create a Github repository at
Github and then we add our source to the repository

    $ git init
    $ git add .
    $ git commit -am "initial commit"
    $ git remote add origin git@github.com:sugaryourcoffee/sugaryourcoffee.git
    $ git push -u origin master

# Intent and content
The internet presentation will contain static pages that provide information
about our mission and the projects we are working on.

# Design
The pages of our application will be

* Home
* About us
* Projects
* Ressources

All pages will contain a header and a footer with server side includes. The CSS
will be based on Bootstrap.

## Document structure
The `<head></head>` part of the websites will stay the same over all pages. So
we extract the head part into a file that has to be included into each of the
web pages. The skeleton of a web page looks like this

    <!--include file="head.shtml">

      <body>
        <!-- content of the web page -->
      </body>
    </html>

The `head.shtml` skeleton looks like this

    <!DOCTYPE html>
      <head>
        <!-- content -->
      </head>

## Install Bootstrap
To install Bootstrap we use Bower. To install Bower we first need to install
nodejs which comes with a package `npm` which in turn lets us install `Bower 

    $ sudo apt-get install nodejs
    $ sudo npm install -g bower

With this setup we are ready to install Bootstrap. Bower installs Bootstrap to
`bower_components`. 

    $ bower install bootstrap

# Deploy the application
In order to deploy the application we need a _sftp_ access to the 1&1 server. We
can connect via Nautilus by clicking _Connect to Server_ and enter the URI 

    sftp://user@server:port

Then click _Connect_.

This will create a directory access point within Nautilus and we can use it as
a regular directory. So deploying the application is copying the 
_secondhand.de/web/_ directory to the sftp directory.

We can also connect from the shell with

    $ sftp user@server
    user's password:
    sftp>

