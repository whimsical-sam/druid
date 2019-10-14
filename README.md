# druid

A basic REPL for crow with some utilities

## Setup

Requirements:
- Python 3.5+
  - Windows & OS X: https://www.python.org/downloads/
  - Linux: `sudo apt-get install python3 python3-pip` or equivalent
- `pip` and `setuptools`
- `pyserial` and `prompt_toolkit`

Note: you might need to use `python` and `pip` instead of `python3` and `pip3` depending on your platform. If `python3` is not found, check that you have python >= 3.5 with `python --version`.

Install and run:
```bash
# Ensure setuptools is up to date
pip3 install --upgrade setuptools
# Install druid
pip3 install monome-druid
# Run druid :)
druid
```

## Druid

Start by running `druid`

- type q (enter) to quit.
- type h (enter) for a list of special commands.

- input values are printed on the top line
- will reconnect to crow after a disconnect / restart
- scrollable console history

Example:

```
druid
//// druid. q to quit. h for help

> x=6

> print(x)
6

> output[1].volts = 0

> q
```

Diagnostic logs are written to `druid.log`.

## Command Line Interface

Sometimes you don't need the repl, but just want to upload/download scripts to/from crow. You can do so directly from the command line with the `upload` and `download` commands.

### Upload

```
druid upload tensor.lua
```

Uploads the provided lua file, `cool_script.lua`, to crow & stores it in flash to be executed on boot.

### Download

```
druid download > feathers.lua
```

Grabs the script currently stored on crow, and pastes the result into a new file `feathers.lua`.

## Bowery

If you're looking for some existing scripts to play with, or just want some known-good scripts to start modifying, check out the [Bowery](https://github.com/monome/bowery) collection. We'd love to have you contribute your own finished scripts!
