howdoi
======

instant coding answers via the command line
-------------------------------------------

(`howdoi documentation <http://gleitz.github.io/howdoi/>`_)
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

::

    usage: howdoi [-h] [-p POS] [-n NUM] [-a] [-l] [-c] [-x] [-C] [-j] [-v] [-e [ENGINE]] [--save] [--view] [--remove] [--empty] [QUERY ...]

    instant coding answers via the command line

    positional arguments:
      QUERY                 the question to answer

    optional arguments:
      -h, --help            show this help message and exit
      -p POS, --pos POS     select answer in specified position (default: 1)
      -n NUM, --num NUM     number of answers to return (default: 1)
      -a, --all             display the full text of the answer
      -l, --link            display only the answer link
      -c, --color           enable colorized output
      -x, --explain         explain how answer was chosen
      -C, --clear-cache     clear the cache
      -j, --json            return answers in raw json format
      -v, --version         displays the current version of howdoi
      -e [ENGINE], --engine [ENGINE]
                            search engine for this query (google, bing, duckduckgo)
      --save, --stash       stash a howdoi answer
      --view                view your stash
      --remove              remove an entry in your stash
      --empty               empty your stash

    environment variable examples:
      HOWDOI_COLORIZE=1
      HOWDOI_DISABLE_CACHE=1
      HOWDOI_DISABLE_SSL=1
      HOWDOI_SEARCH_ENGINE=google
      HOWDOI_URL=serverfault.com


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
