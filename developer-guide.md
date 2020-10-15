# Developer guide

## Table of content
- [Install requirements](#install-requirements)
- [Install nlp-profiler](#install-nlp-profiler)
- [Tests](#tests)
- [CI/CD](#ci-cd)
- [Contribution steps](#contribution-steps)

### Install requirements

```bash
pip install -r requirements-dev.txt
pip install -r requirements.txt

```

**Linux/macOS**

Install `line-profiler` for Linux or macOS environments:

```
pip install -r requirements-linux-dev.txt
```

**Windows**

Install `line-profiler` for Windows depending on the Python version:

```bash
# Python 3.6
python -m pip install line-profiler@https://download.lfd.uci.edu/pythonlibs/x2tqcw5k/line_profiler-3.0.2-cp36-cp36m-win_amd64.whl

# Python 3.7
python -m pip install line-profiler@https://download.lfd.uci.edu/pythonlibs/x2tqcw5k/line_profiler-3.0.2-cp37-cp37m-win_amd64.whl

# Python 3.8
python -m pip install line-profiler@https://download.lfd.uci.edu/pythonlibs/x2tqcw5k/line_profiler-3.0.2-cp38-cp38-win_amd64.whl
```

### Install nlp-profiler

Do the below to start getting reading to work in the developer mode.

```bash
git clone https://github.com/neomatrix369/nlp_profiler
cd nlp_profiler
```

```
python setup.py install
```
or 

```
pip install -e .
```

or 

```
pip install --prefix .
```


### Tests

Run all the tests with coverage information using the below command after all packages have been successfully installed:

```bash
./test-coverage tests slow-tests
```

On the tests passing (or partially passing), these folders will be created:

```
.coverage-reports
.cprofile
.test-run-reports
```

Also files with the name `.coverage*` will be created. The shell script will give enough guidance to be able to know where to find the respective reports.

### CI/CD

We are using GitHub actions to enable this feature. See [.github/workflows](.github/workflows) to find out about the different actions configured to achieve this. See [GitHub Actions docs](https://docs.github.com/en/free-pro-team@latest/actions) for further help.

At the moment we have only implemented the CI part of CI/CD. This is work in progress as of the writing of this doc.

### Contribution steps

In addition to have read the [Contribution guide](#CONTRIBUTING.md), please also follow the steps in the [Table of Contents](#table-of-content) above.

Creating a Pull request will also result in these steps to be executed on Windows and Linux instances via the GitHub action(s).

Any failures on the PR would need to be addressed. More details on specific changes will be addressed at a later time, but the failures in tests or at any othe aspect should more or less indicate the reason for failure. If not, please look for past reported issues under [GitHub issues](https://github.com/neomatrix369/nlp_profiler/issues) or report a new one with the specifics of the issue in hand.

Additional to help the process please also feel free to the amend/improve the GitHub actions under [.github/workflows](.github/workflows).

---

Return to [Developer guide section in the README.md](README.md#developer-guide) <br>
Return to [README.md](README.md)