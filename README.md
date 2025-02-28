# deloop
_a command-line delooper_


[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

## Presentation

`deloop` is a command-line tool that takes two .wav files with _strictly_ identical parameters (sampling rate, number of frames), and returns a .wav file by substracting the two signals.

The targetted usecase is to separate stems from loops generated by a looper. For instance :

* loop 1: contains a drum loop
* loop 2: contains the same drum loop and a bass line

`deloop` allows to get the dry bass line back by removing the drums from the second loop (but we need the first loop to do that, of course...).

🚨 Attention: the performances will be altered if the drum loop has been modified in the overdub process...

## Usage

Intended to be used as a command-line tool:

```bash
$> deloop /path/to/file_a.wav /path/to/file_b.wav -o /path/to/output_file.wav
```

## References used to build this package

https://packaging.python.org/en/latest/guides/creating-command-line-tools/
https://packaging.python.org/en/latest/tutorials/packaging-projects/
https://packaging.python.org/en/latest/guides/distributing-packages-using-setuptools

# Note for packaging testing

```bash
$> pip install --index-url https://test.pypi.org/simple/ --extra-index-url https://pypi.org/simple deloop
```