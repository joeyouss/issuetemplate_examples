howdoi
======

instant coding answers via the command line
-------------------------------------------

.. image:: https://img.shields.io/github/workflow/status/gleitz/howdoi/Python%20CI?style=plastic&color=78dce8
        :target: https://github.com/gleitz/howdoi/actions?query=workflow%3A%22Python+CI%22

.. image:: https://img.shields.io/badge/dynamic/json?style=plastic&color=ab9df2&maxAge=86400&label=downloads&query=%24.total_downloads&url=https%3A%2F%2Fapi.pepy.tech%2Fapi%2Fprojects%2Fhowdoi
        :target: https://pepy.tech/project/howdoi

.. image:: https://img.shields.io/pypi/pyversions/howdoi.svg?style=plastic&color=ff6188
        :target: https://pypi.python.org/pypi/howdoi

|

.. image:: http://sublimate.org/flyers/HowDoIcolor512.png
        :target: https://pypi.python.org/pypi/howdoi
        :alt: Sherlock, your neighborhood command-line sloth sleuth

Sherlock, your neighborhood command-line sloth sleuth.

----

Table of Contents
~~~~~~~~~~~~~~~~~

-  Introduction to howdoi
-  Getting started with howdoi

   -  Installation
   -  Learning how to use howdoi
   -  Howdoi documentation
   -  Howdoi extension

-  Howdoi documentation
-  Contributors
-  Contributing to howdoi
-  Notes and important points

Are you a hack programmer? Do you find yourself constantly Googling for
how to do basic programming tasks?

Suppose you want to know how to format a date in bash. Why open your browser
and read through blogs (risking major distraction) when you can simply stay
in the console and ask howdoi:

::

    $ howdoi format date bash
    > DATE=`date +%Y-%m-%d`

howdoi will answer all sorts of queries:

::

    $ howdoi print stack trace python
    > import traceback
    >
    > try:
    >     1/0
    > except:
    >     print '>>> traceback <<<'
    >     traceback.print_exc()
    >     print '>>> end of traceback <<<'
    > traceback.print_exc()

    $ howdoi convert mp4 to animated gif
    > video=/path/to/video.avi
    > outdir=/path/to/output.gif
    > mplayer "$video" \
    >         -ao null \
    >         -ss "00:01:00" \  # starting point
    >         -endpos 10 \ # duration in second
    >         -vo gif89a:fps=13:output=$outdir \
    >         -vf scale=240:180

    $ howdoi create tar archive
    > tar -cf backup.tar --exclude "www/subf3" www

.. image:: http://imgs.xkcd.com/comics/tar.png
        :target: https://xkcd.com/1168/

Installation
------------

::

    pip install howdoi

or

::

    pip install git+https://github.com/gleitz/howdoi.git#egg=howdoi

or

::

    python setup.py install

New to howdoi?
--------------

::

    howdoi howdoi

Usage
-----

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

Using the howdoi stashing feature (for more advanced features view the `keep documentation <https://github.com/OrkoHunter/keep>`_).

::

    stashing: howdoi --save QUERY
    viewing:  howdoi --view
    removing: howdoi --remove (will be prompted which answer to delete)
    emptying: howdoi --empty (empties entire stash, will be prompted to confirm)

As a shortcut, if you commonly use the same parameters each time and don't want to type them, add something similar to your .bash_profile (or otherwise). This example gives you 5 colored results each time.

::

    alias h='function hdi(){ howdoi $* -c -n 5; }; hdi'

And then to run it from the command line simply type:

::

    $ h format date bash

You can also search other `StackExchange properties <https://stackexchange.com/sites#traffic>`_ for answers:

::

    HOWDOI_URL=cooking.stackexchange.com howdoi make pesto

or as an alias:

::

    alias hcook='function hcook(){ HOWDOI_URL=cooking.stackexchange.com howdoi $* ; }; hcook'
    hcook make pesto

Other useful aliases:

::

    alias hless='function hdi(){ howdoi $* -c | less --raw-control-chars --quit-if-one-screen --no-init; }; hdi'

Contributors
------------

-  Benjamin Gleitzman (`@gleitz <http://twitter.com/gleitz>`_)
-  Yanlam Ko (`@YKo20010 <https://github.com/YKo20010>`_)
-  Diana Arreola (`@diarreola <https://github.com/diarreola>`_)
-  Eyitayo Ogunbiyi (`@tayoogunbiyi <https://github.com/tayoogunbiyi>`_)
-  Chris Nguyen (`@chrisngyn <https://github.com/chrisngyn>`_)
-  Shageldi Ovezov (`@ovezovs <https://github.com/chrisngyn>`_)
-  Mwiza Simbeye (`@mwizasimbeye11 <https://github.com/mwizasimbeye11>`_)
-  Shantanu Verma (`@SaurusXI <https://github.com/SaurusXI>`_)
-  And `more! <https://github.com/gleitz/howdoi/graphs/contributors>`_

Notes
-----

-  Works with Python 3.5 and newer. Unfortunately Python 2.7 support has been discontinued :(
-  There is a `GUI that wraps howdoi <https://pypi.org/project/pysimplegui-howdoi/>`_.
-  There is a `Flask webapp that wraps howdoi <https://howdoi.maxbridgland.com>`_.
-  An Alfred Workflow for howdoi can be found at `http://blog.gleitzman.com/post/48539944559/howdoi-alfred-even-more-instant-answers <http://blog.gleitzman.com/post/48539944559/howdoi-alfred-even-more-instant-answers>`_.
-  Slack integration available through `slack-howdoi <https://github.com/ellisonleao/slack-howdoi>`_.
-  Telegram integration available through `howdoi-telegram <https://github.com/aahnik/howdoi-telegram>`_.
-  Howdoi uses a cache for faster access to previous questions. Caching functionality can be disabled by setting the HOWDOI_DISABLE_CACHE environment variable. The cache is stored in `~/.cache/howdoi`.
-  You can set the HOWDOI_URL environment variable to change the source url for answers (default: `stackoverflow.com`, also supported: `serverfault.com`, `pt.stackoverflow.com`, `full list <http://stackexchange.com/sites?view=list#traffic>`_).
-  You can set the HOWDOI_SEARCH_ENGINE environment variable to change the underlying search engine for StackOverflow links (default: `google`, also supported: `bing`, `duckduckgo`). The -e flag will switch the underlying engine for a single query.
-  Setting the HOWDOI_COLORIZE environment variable will colorize the output by default.
-  Special thanks to Rich Jones (`@miserlou <https://github.com/miserlou>`_) for the idea.
-  More thanks to `Ben Bronstein <https://benbronstein.com/>`_ for the logo.

Development
-----------

-  Checkout the repo
-  Run ``python -m howdoi QUERY`` (if you try running ``python howdoi/howdoi.py`` you might get ``ValueError: Attempted relative import in non-package``).
-  When you're ready to open a PR be sure to run ``python setup.py lint`` to make sure your code passes the checks.

If you would like to use howdoi from within a python script, just pass your query to `howdoi.howdoi()`:
::

    from howdoi import howdoi

    query = "for loop python"
    output = howdoi.howdoi(query)


Or parse it yourself (either work):

::

    from howdoi import howdoi

    query = "for loop python"
    parser = howdoi.get_parser()
    args = vars(parser.parse_args(query.split(' ')))

    output = howdoi.howdoi(args)

Or get the results as JSON:

::

    from howdoi import howdoi
    import json

    query = "for loop python"

    output_json = json.loads(howdoi.howdoi(f'{query} -j'))
Howdoi documentation
^^^^^^^^^^^^^^^^^^^^

The howdoi documentation lies `here <https://gleitz.github.io/howdoi/>`__ and is hosted in the form of mkdocs. It contains each and every detail about howdoi and its related things. The mkdocs also reside in the folder ``howdoi/docs/`` 
Contents of Howdoi Documentation : 

- Introduction and Installing 
- Usage of howdoi 
- Setting up the development environment 
- How to contribute 
- Contributing documentation 
- Developing extension 
- Troubleshooting

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
