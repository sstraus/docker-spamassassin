docker-spamassassin
===================

SpamAssassin as a Docker image. It runs `spamd` on exposed port `783` and
constantly updates its ruleset.

Usage
-----

    docker run -d -p 783:783 sstraus/spamassassin

or linked (this is how I use it)

    docker run -d --name spamassassin sstraus/spamassassin
    docker run -d --link spamassassin:spamassassin application-with-spamc-or-something
