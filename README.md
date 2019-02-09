ffprev
======

Preview HTML file with Firefox.

Usage
-----

```
usage:
  ffprev [--] [<url>]  # open the url or reload
  ffprev -q            # close the web-browser
  ffprev -h            # print usage

environment-variables:
  FFPREVPID    # the path of the pid-file (default: /tmp/$USER.ffprev.pid)
  FFPREVSID    # the path of the sid-file (default: /tmp/$USER.ffprev.sid)
  FFPREVBIN    # the firefox-binary used by geckodriver (default: default firefox)
  FFPREVPORT   # the port used by geckodriver (default: 4444)
```

Requirements
------------

- Perl (5.14.0 or later)
- Firefox
- geckodriver

Installation
------------

1. Copy `ffprev` into your `$PATH`.
2. Make `ffprev` executable.

### Example

```
$ curl -L https://raw.githubusercontent.com/kusabashira/ffprev/master/ffprev > ~/bin/ffprev
$ chmod +x ~/bin/ffprev
```

Note: In this example, `$HOME/bin` must be included in `$PATH`.

Commands
--------

### ffprev \[--\] \[\<url\>\]

Open the url or reload.
(Launch the web-browser if it hasn't been launched yet)

```
$ ffprev
(Reload current tab)

$ ffprev file:///$HOME/Document/test.html
(Open file:///$HOME/Documents/test.html or reload)
```

### ffprev -q

Close the web-browser.

```
$ ffprev -q
(Close the web-browser)
```

### ffprev -h

Print usage.

```
$ ffprev -h
(Print usage)
```

Variables
---------

### FFPREVPID

The path of the file to save daemon's pid.
Default value is `/tmp/$USER.ffprev.pid`.

### FFPREVSID

The path of the file to save session-id.
Default value is `/tmp/$USER.ffprev.sid`.

### FFPREVBIN

The firefox-binary used by geckodriver.
Default value is `(default firefox)`.

### FFPREVPORT

The port used by geckodriver.
Default value is `4444`.

License
-------

MIT License

Author
------

nil2 <nil2@nil2.org>
