---
subtitle: run tests with acre
terms:
  - cmd: run
---
# acre run
> Run one or multiple tests

## Synopsis

    acre run [-f features] <options>

## Description

Run one or multiple tests using acre.

## Arguments

`-f, --feature`
:   A list of features to be tested

`-c, --config`
:   A comma-separated list of additional [configuration files](../doc/configuration.md)
    to be loaded for the test run.

    The configuration files are loaded in the given order. If multiple
    configuration files define the same value, the value is overwritten.

`options`
:   Additional options passed to the `radish` command.
