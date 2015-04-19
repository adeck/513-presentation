
# What is this?

It's a presentation written for WUSTL CSE 513T on the current state of state space complexity research, but more broadly it's a wonderful little template for generating static web slideshows.

# How do I get it working?

## What commands do I run?

Well, you'll want to install `git` and `virtualenv` (if you're on debian, you'll want to run: `sudo apt-get install git python-virtualenv`), then run (as a non-root user):

    git clone https://github.com/adeck/513-presentation.git
    cd 513-presentation
    ./setup && ./build
    ln out/main.html main.html

This should install the two dependencies (reveal.js and staticjinja) into the CWD. Now navigate to your browser to `main.html` in the current directory, and you should see the presentation.

## What technologies does this use and why?

<dl>
  <dt>reveal.js</dt>
  <dd>
  Implements the core slideshow functionality; like slidy, slideous, s5, deck.js, etc., etc. Too vague? [See for yourself.](https://lab.hakim.se/reveal-js)
  </dd>

  <dt>staticjinja</dt>
  <dd>
  Used to combine all the Jinja2 files from the separate slides into a single html file. Using staticjinja specifically because, usually, templating engines like Jinja2, haml, or Mojolicious' templating engine are part of web application frameworks and come bundled with a server. This doesn't need a server.
  </dd>

  <dt>HTML, CSS, Javascript</dt>
  <dd>
  Because it's web-based. The idea is that you write your presentation, compile it into a single html file (with a few external, static dependencies) and then simply visit that file from a normal browser.
  </dd>
</dl>







