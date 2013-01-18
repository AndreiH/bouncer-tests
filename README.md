<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<HTML>
<HEAD>
	<META HTTP-EQUIV="CONTENT-TYPE" CONTENT="text/html; charset=windows-1252">
	<TITLE></TITLE>
	<META NAME="GENERATOR" CONTENT="OpenOffice.org 3.4.1  (Win32)">
	<META NAME="CREATED" CONTENT="0;0">
	<META NAME="CHANGED" CONTENT="20130118;18295714">
	<STYLE TYPE="text/css">
	<!--
		H2.cjk { font-family: "SimSun" }
		H2.ctl { font-family: "Mangal" }
		H3.cjk { font-family: "SimSun" }
		H3.ctl { font-family: "Mangal" }
		PRE.cjk { font-family: "NSimSun", monospace }
		CODE.cjk { font-family: "NSimSun", monospace }
	-->
	</STYLE>
</HEAD>
<BODY LANG="en-US" DIR="LTR">
<H1 STYLE="border-top: none; border-bottom: 1.10pt double #000000; border-left: none; border-right: none; padding-top: 0in; padding-bottom: 0.03in; padding-left: 0in; padding-right: 0in">
<CODE CLASS="western"><FONT FACE="Thorndale, serif"><FONT SIZE=5>Selenium
Tests for Mozilla's Bounce</FONT></FONT></CODE><CODE CLASS="western"><FONT FACE="Thorndale, serif"><FONT SIZE=5>r</FONT></FONT></CODE></H1>
<P>Thank you for checking out Mozilla's Bouncer test suite. Mozilla
and the Mozwebqa team are grateful for the help and hard work of many
contributors like yourself. The following contributors have submitted
pull requests to bouncer-tests:</P>
<P><A HREF="https://github.com/mozilla/bouncer-tests/graphs/contributors">https://github.com/mozilla/bouncer-tests/graphs/contributors</A></P>
<H1 STYLE="border-top: none; border-bottom: 1px solid #000000; border-left: none; border-right: none; padding-top: 0in; padding-bottom: 0.03in; padding-left: 0in; padding-right: 0in">
<FONT SIZE=5>Getting involved as a contributor</FONT></H1>
<P>We love working with contributors to fill out the Selenium test
coverage for Bouncer-Tests, but it does require a few skills. You
will need to know some Python, some Selenium and you will need some
basic familiarity with Github. 
</P>
<P>If you know some Python, it's worth having a look at the Selenium
framework to understand the basic concepts of browser based testing
and especially page objects. Our suite uses Selenium WebDriver. 
</P>
<P>If you need to brush up on programming but are eager to start
contributing immediately, please consider helping us find bugs in
Mozilla Firefox or in the Mozilla web-sites tested by the WebQA team.
</P>
<P>To brush up on Python skills before engaging with us, Dive Into
Python is an excellent resource. MIT also has lecture notes on Python
available through their open courseware. The programming concepts you
will need to know include functions, working with classes, and some
object oriented programming basics. 
</P>
<H1 STYLE="border-top: none; border-bottom: 1px solid #000000; border-left: none; border-right: none; padding-top: 0in; padding-bottom: 0.03in; padding-left: 0in; padding-right: 0in">
<FONT SIZE=5>Questions are always welcome</FONT></H1>
<P>While we take pains to keep our documentation updated, the best
source of information is those of us who work on the project. Don't
be afraid to join us in irc.mozilla.org #mozwebqa to ask questions
about our Selenium tests. Mozilla also hosts the #mozillians chat
room to answer your general questions about contributing to Mozilla. 
</P>
<H2 CLASS="western" STYLE="border-top: none; border-bottom: 1px solid #000000; border-left: none; border-right: none; padding-top: 0in; padding-bottom: 0.03in; padding-left: 0in; padding-right: 0in">
<CODE CLASS="western"><FONT FACE="Thorndale, serif">Running Tests</FONT></CODE></H2>
<H3 CLASS="western">Python</H3>
<P>Before you will be able to run these tests you will need to have
Python 2.6(2.6+) installed.</P>
<P><STRONG>note</STRONG></P>
<P>The below instructions will install the required Python libraries
into your global Python installation. If you work on multiple Python
projects that might end up needing different versions of the same
libraries, you might want to follow <CODE CLASS="western">&lt;code&gt;sudo
easy_install pip&lt;/code&gt;</CODE> with <CODE CLASS="western">&lt;code&gt;sudo
pip install virtualenv&lt;/code&gt;</CODE>, and then create and
activate a <A HREF="http://www.virtualenv.org/">virtualenv</A> (e.g.
<CODE CLASS="western">&lt;code&gt;virtualenv
bouncer-tests-env&lt;/code&gt;; &lt;code&gt;source
bouncer-tests-env/bin/activate&lt;/code&gt;</CODE>) to create a clean
&quot;virtual environment&quot; for just this project. Then you can
<CODE CLASS="western">&lt;code&gt;pip install -r
requiremenst/mozwebqa.txt&lt;/code&gt;</CODE> in your virtual
environment without needing to use <CODE CLASS="western">&lt;code&gt;sudo&lt;/code&gt;.</CODE></P>
<P>If you don't mind installing globally, just run</P>
<PRE CLASS="western" STYLE="margin-bottom: 0.2in"><CODE CLASS="western">&lt;code&gt;sudo easy_install pip</CODE><CODE CLASS="western">&lt;/code&gt;</CODE></PRE><P>
followed by</P>
<PRE CLASS="western" STYLE="margin-bottom: 0.2in"><CODE CLASS="western">&lt;code&gt;sudo pip install -r requirements.txt&lt;/code&gt;</CODE></PRE><P>
<STRONG>note</STRONG></P>
<P>If you are running on Ubuntu/Debian you will need to first do</P>
<PRE CLASS="western" STYLE="margin-bottom: 0.2in"><CODE CLASS="western">&lt;code&gt;sudo apt-get install python-setuptools&lt;/code&gt;</CODE></PRE><P>
to install the required Python libraries.</P>
<H3 CLASS="western">Running tests locally</H3>
<P>To run tests locally it's a simple case of calling py.test from
the root directory.</P>
<PRE CLASS="western" STYLE="margin-bottom: 0.2in"><CODE CLASS="western">&lt;code&gt;py.test &ndash;driver=firefox&lt;/code&gt;</CODE></PRE><P>
For more command line options see
<A HREF="https://github.com/davehunt/pytest-mozwebqa">https://github.com/davehunt/pytest-mozwebqa</A></P>
<H2 CLASS="western" STYLE="border-top: none; border-bottom: 1px solid #000000; border-left: none; border-right: none; padding-top: 0in; padding-bottom: 0.03in; padding-left: 0in; padding-right: 0in">
Writing Tests</H2>
<P>If you want to get involved and add more tests then there's just a
few things we'd like to ask you to do:</P>
<OL>
	<LI><P STYLE="margin-bottom: 0in">Use the <A HREF="https://github.com/mozilla/mozwebqa-test-templates">template
	files</A> for all new tests and page objects 
	</P>
	<LI><P STYLE="margin-bottom: 0in">Follow our simple <A HREF="https://wiki.mozilla.org/QA/Execution/Web_Testing/Docs/Automation/StyleGuide">style
	guide</A> 
	</P>
	<LI><P STYLE="margin-bottom: 0in">Fork this project with your own
	GitHub account 
	</P>
	<LI><P>Make sure all tests are passing, and submit a pull request
	with your changes 
	</P>
</OL>
<H2 CLASS="western" STYLE="border-top: none; border-bottom: 1px solid #000000; border-left: none; border-right: none; padding-top: 0in; padding-bottom: 0.03in; padding-left: 0in; padding-right: 0in">
License</H2>
<P>This software is licensed under the <A HREF="http://www.mozilla.org/MPL/2.0/">MPL</A>
2.0:</P>
<PRE CLASS="western"><CODE CLASS="western">&lt;code&gt;</CODE><CODE CLASS="western">This Source Code Form is subject to the terms of the Mozilla Public</CODE>
<CODE CLASS="western">License, v. 2.0. If a copy of the MPL was not distributed with this</CODE>
<CODE CLASS="western">file, You can obtain one at http://mozilla.org/MPL/2.0/.</CODE><CODE CLASS="western">&lt;/code&gt;</CODE></PRE><P>
<BR><BR>
</P>
</BODY>
</HTML>