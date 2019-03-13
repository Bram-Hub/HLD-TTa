# Handy Logic Doodahs-Truth Tables
[![Build Status](https://travis-ci.org/MasterOdin/TruthTables.svg?branch=master)](https://travis-ci.org/MasterOdin/TruthTables) [![Coverage Status](https://coveralls.io/repos/github/MasterOdin/TruthTables/badge.svg?branch=master)](https://coveralls.io/github/MasterOdin/TruthTables?branch=master)
## Authors
2016:
Matt Peveler

## About
This is a flask app (with a python module backing it) that can be used to generate Truth Tables for any number of given logical formulas. This is part of the handy logic doodahs series of Automated Theorem Provers.

![Flask App](https://raw.githubusercontent.com/MasterOdin/TruthTables/master/static/screenshot.png)

It uses a functional format for inputting logical formulas. This is the base identity for inputs:
```
A
not(A)
and(A, B)
or(A, B)
if(A, B)
iff(A, B)
```
where `A` and `B` can either be atomic statements or a functional operator. All operators are either unary (not) or binary (and, or, if, iff) and there is no support for a generalized notation. This means that ```and(A, B, C)``` will thrown an error.

## Running
In order to run the server, you will need to have flask installed.
```sh
pip3 install flask
```
You can then run the server with
```sh
python3 server.py
```
The url to navigate to will be displayed as part of the output from running that command.

To run the test suite you need to install nose and nose_parameterized
```sh
pip3 install nose
pip3 install nose_parameterized
```
and you can run the tests with
```sh
python3 tests.py
```
