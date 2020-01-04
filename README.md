# Iterm2 SSH

## Overview

Wrapper around ssh to do some various enhancements around iTerm2.  Currently
this will just change the tab color based on the ssh target

## Configuration

Make sure you have a config file at `~/.iterm2_ssh.yaml`.  It should look
something like:

```
---
tab_colors:
  regexes:
      '.*(-dev-|-test-).*': 'green'
      '.*-prod-': 'red'
  default: 'blue'
```

The colors can be either human readable or hex.  As long as it can be parsed by
[webcolors](https://github.com/ubernostrum/webcolors), it should work
