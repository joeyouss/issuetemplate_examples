howdoi
======

instant coding answers via the command line
-------------------------------------------

howdoi documentation
~~~~~~~~~~~~~~~~~

-  Introduction to howdoi and installation
-  Howdoi usage
-  Setting up the development environment
-  Contributing to howdoi
-  Contributing documentation to howdoi
-  howdoi extension development
-  howdoi advanced usage


INTRODUCTION TO HOWDOI
----------------------

.. raw:: html
Howdoi is an open-source command line tool which parses the data on the
web and makes the most relevant data available to you in your command
line. 

Are you a hack programmer? Do you find yourself constantly Googling for
how to do basic programming tasks?

Suppose you want to know how to format a date in bash. Why open your browser
and read through blogs (risking major distraction) when you can simply stay
in the console and ask howdoi:

::

    $ howdoi format date bash
    > DATE=`date +%Y-%m-%d`
GETTING STARTED WITH HOWDOI
~~~~~~~~~~~~~~~~~~~~~~~~~~~

All you need is Python 3.5 and above and pip installed to run howdoi in
your local system. 

**Note : Howdoi Python 2.7 support is discontinued.**

Installing howdoi
^^^^^^^^^^^^^^^^^

To get started with howdoi, In your command line simply type :

``pip install howdoi`` 

Or

Check out howdoi docs for more ways of installation.

Learning how to use howdoi 
^^^^^^^^^^^^^^^^^^^^^^^^^^
To see all the howdoi commands which you can use, simply type: ``howdoi howdoi``
And all the present commands will be shown in front of you.

Understanding howdoi usage
^^^^^^^^^^^^^^^^^^^^^^^^^^
- **Howdoi arguments/ flags** - Howdoi comes with a set of predefined flags/arguments which can be set by you as per your choice. You can just type ``howdoi -h`` in your command line to see each argument and what they do. 
The available arguments currently are listed below: 
   - **-h, --help** : To see the help message which has all the information about every command 
   - **-p POS, --pos POS** : To select answer in any specified position. 
   - **-n NUM, --num NUM** : Defines the number of answers to return. By default, set to 1. 
   - **-a, --all**: Shows the full text of an answer 
   - **-l, --link**: Displays only the link of the answer 
   - **-j** : Displays the answer in JSON format. Useful when you are building on top of howdoi. 
   - **-c, --color**: Prints colorized output
   - **-x, --explain**: Explains why the outputted answer was shown to you 
   - **-C, --clear-cache**: Clears the cache
   - **-j, --json** : Outputs the answer in raw JSON format 
   - **-v, --version**: Displays your current version of howdoi. 
   - **-e [ENGINE], --engine [ENGINE]** : Allows to choose the search engine for the query. Currently supported google, bing, duckduckgo 
   - **--save, --stash** : Enables stashing feature for a howdoi answer 
   - **--view** : Displayed the stash
   - **--remove** : Removes an entry in your stash 
   - **--empty** : Empties the stash completely

CONTRIBUTORS
~~~~~~~~~~~~
-  Benjamin Gleitzman (`@gleitz <http://twitter.com/gleitz>`_)
-  Yanlam Ko (`@YKo20010 <https://github.com/YKo20010>`_)
-  Diana Arreola (`@diarreola <https://github.com/diarreola>`_)
-  Eyitayo Ogunbiyi (`@tayoogunbiyi <https://github.com/tayoogunbiyi>`_)
-  Chris Nguyen (`@chrisngyn <https://github.com/chrisngyn>`_)
-  Shageldi Ovezov (`@ovezovs <https://github.com/chrisngyn>`_)
-  Mwiza Simbeye (`@mwizasimbeye11 <https://github.com/mwizasimbeye11>`_)
-  Shantanu Verma (`@SaurusXI <https://github.com/SaurusXI>`_)
-  And `more! <https://github.com/gleitz/howdoi/graphs/contributors>`_

HOW TO CONTRIBUTE
~~~~~~~~~~~~~~~~~

We welcome contributions that make Howdoi better and/or improve the existing functionalities of the project. We have created a separate
guide to contributing to howdoi which resides in the howdoi documentation in mkdcos. 
The guide contains the following:

- Introduction for first time contributors 
- Getting started with howdoi 
- Making PRs and testing 
- Asking for help 
- Helpful tips for a good contribution experience.

NOTES AND IMPORTANT POINTS
~~~~~~~~~~~~~~~~~~~~~~~~~~
-  Works with Python 3.5 and newer. Unfortunately Python 2.7 support has been discontinued :(
-  There is a `GUI that wraps howdoi <https://pypi.org/project/pysimplegui-howdoi/>`_.
-  There is a `Flask webapp that wraps howdoi <https://howdoi.maxbridgland.com>`_.
-  An Alfred Workflow for howdoi can be found at `http://blog.gleitzman.com/post/48539944559/howdoi-alfred-even-more-instant-answers <http://blog.gleitzman.com/post/48539944559/howdoi-alfred-even-more-instant-answers>`_.
-  Slack integration available through `slack-howdoi <https://github.com/ellisonleao/slack-howdoi>`_.
-  Telegram integration available through `howdoi-telegram <https://github.com/aahnik/howdoi-telegram>`_.
-  Special thanks to Rich Jones (`@miserlou <https://github.com/miserlou>`_) for the idea.
-  More thanks to `Ben Bronstein <https://benbronstein.com/>`_ for the logo.
