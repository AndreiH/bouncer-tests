Selenium Tests for Mozilla's Bounce
=============

Thank you for checking out Mozilla's Bouncer test suite. Mozilla and the Mozwebqa team are grateful for the help and hard work of many contributors like yourself. The following contributors have submitted pull requests to bouncer-tests:

https://github.com/mozilla/bouncer-tests/graphs/contributors

Getting involved as a contributor
=============

We love working with contributors to fill out the Selenium test coverage for Bouncer-Tests, but it does require a few skills. You will need to know some Python, some Selenium and you will need some basic familiarity with Github. 

If you know some Python, it's worth having a look at the Selenium framework to understand the basic concepts of browser based testing and especially page objects. Our suite uses Selenium WebDriver. 

If you need to brush up on programming but are eager to start contributing immediately, please consider helping us find bugs in Mozilla Firefox or find bugs in the Mozilla web-sites tested by the WebQA team. 

To brush up on Python skills before engaging with us, Dive Into Python is an excellent resource. MIT also has lecture notes on Python available through their open courseware.The programming concepts you will need to know include functions, working with classes, and some object oriented programming basics. 

Questions are always welcome
=============

While we take pains to keep our documentation updated, the best source of information is those of us who work on the project. Don't be afraid to join us in irc.mozilla.org #mozwebqa to ask questions about our Selenium tests. Mozilla also hosts the #mozillians chat room to answer your general questions about contributing to Mozilla. 

Running Tests
=============
Python
Before you will be able to run these tests you will need to have Python 2.6 installed. 
note 
The below instructions will install the required Python libraries into your global Python installation. If you work on multiple Python projects that might end up needing different versions of the same libraries, you might want to follow <code>sudo easy_install pip </code> with <code>sudo pip install virtualenv </code>, and then create and activate a virtualenv  (e.g. <code>virtualenv caseconductor-tests-env; source case-conductor-tests-env/bin/activate </code> ) to create a clean "virtual environment" for just this project. Then you can <code>pip install -r requiremenst/mozwebqa.txt</code> in your virtual environment without needing to use <code>sudo</code>.
If you don't mind installing globally, just run 
<code>sudo easy_install pip</code>
followed by 
<code>sudo pip install -r requirements/mozwebqa.txt</code>
note
If you are running on Ubuntu/Debian you will need to first do 
<code>sudo apt-get install python-setuptools</code>
to install the required Python libraries.
Selenium
Once this is all set up, you will need to download and start a Selenium server. You can download the latest Selenium server from here. The filename will be something like 'selenium-server-standalone-x.x.jar (where x.x is current shipping version)' 
To start the Selenium server run the following command:
<code>java -jar ~/Downloads/selenium-server-standalone-x.x.jar (where x.x is current shipping version)</code>
Change the path/name to the downloaded Selenium server file.
Running tests locally
To run tests locally it's a simple case of calling py.test from the root directory.
<code> py.test –driver=firefox</code>
For more command line options see https://github.com/davehunt/pytest-mozwebqa 

Writing Tests
=============

If you want to get involved and add more tests then there's just a few things we'd like to ask you to do:
1. Use the template files for all new tests and page objects 
2. Follow our simple style guide 
3. Fork this project with your own GitHub account 
4. Make sure all tests are passing, and submit a pull request with your changes 

License
=============

This software is licensed under the MPL 2.0: 

<code>This Source Code Form is subject to the terms of the Mozilla Public
License, v. 2.0. If a copy of the MPL was not distributed with this
file, You can obtain one at http://mozilla.org/MPL/2.0/.</code>

