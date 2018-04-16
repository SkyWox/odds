# Welcome to the AWS CodeStar sample web service

This sample code helps get you started with a simple Python web service using
AWS Lambda and Amazon API Gateway.

## What's Here

This sample includes:

* README.md - this file
* buildspec.yml - this file is used by AWS CodeBuild to package your
  application for deployment to AWS Lambda
* index.py - this file contains the sample Python code for the web service
* template.yml - this file contains the AWS Serverless Application Model (AWS SAM) used
  by AWS CloudFormation to deploy your application to AWS Lambda and Amazon API
  Gateway.
* tests/ - this directory contains unit tests for your application

## What Do I Do Next?

If you have checked out a local copy of your repository you can start making changes
to the sample code. We suggest making a small change to index.py first, so you can
see how changes pushed to your project's repository are automatically picked up by your
project pipeline and deployed to AWS Lambda and Amazon API Gateway. (You can watch the pipeline
progress on your AWS CodeStar project dashboard.)Once you've seen how that works,
start developing your own code, and have fun!

To run your tests locally, go to the root directory of the
sample code and run the `python -m unittest discover tests` command, which
AWS CodeBuild also runs through your `buildspec.yml` file.

This sample code helps get you started with a simple Django web application
deployed by AWS Elastic Beanstalk.

## What's Here

This sample includes:

* README.md - this file
* ebdjango/ - this directory contains your Django project files. Note that this
  directory contains a Django config file (settings.py) that includes a pre-defined
  SECRET_KEY. Before running in a production environment, you should replace this
  application key with one you generate
  (see https://docs.djangoproject.com/en/1.11/howto/deployment/checklist/#secret-key for details)
* helloworld/ - this directory contains your Django application files
* manage.py - this Python script is used to start your Django web application
* .ebextensions/ - this directory contains the Django configuration file that
  allows AWS Elastic Beanstalk to deploy your Django application
* buildspec.yml - this file is used by AWS CodeBuild to build and test
  your application
* requirements.txt - this file is used to install Python dependencies needed by
  the Django application

## Getting Started

These directions assume you want to develop on your local computer, and not
from the Amazon EC2 instance itself. If you're on the Amazon EC2 instance, the
virtual environment is already set up for you, and you can start working on the
code.

To work on the sample code, you'll need to clone your project's repository to your
local computer. If you haven't, do that first. You can find instructions in the
AWS CodeStar user guide.

1.  Create a Python virtual environment for your Django project. This virtual
    environment allows you to isolate this project and install any packages you
    need without affecting the system Python installation. At the terminal, type
    the following command:

         $ virtualenv .venv

2.  Activate the virtual environment:

        $ activate ./venv/bin/activate

3.  Install Python dependencies for this project:

        $ pip install -r requirements.txt

4.  (Optional) Enable Django's debug mode for development:

        $ export DJANGO_DEBUG=True

5.  Start the Django development server:

        $ python manage.py runserver

6.  Open http://127.0.0.1:8000/ in a web browser to view your application.

## What Do I Do Next?

Once you have a virtual environment running, you can start making changes to
the sample Django web application. We suggest making a small change to
/helloworld/templates/index.html first, so you can see how changes pushed to
your project's repository are automatically picked up and deployed to the Amazon EC2
instance by AWS Elastic Beanstalk. (You can watch the progress on your project dashboard.)
Once you've seen how that works, start developing your own code, and have fun!

To run your tests locally, go to the root directory of the sample code and run
the `python manage.py test` command, which AWS CodeBuild also runs through
your `buildspec.yml` file.
