[![Build Status](https://travis-ci.org/michaelowens/AutoModerator.svg?branch=master)](https://travis-ci.org/michaelowens/AutoModerator)
[![Test Coverage](https://codeclimate.com/github/michaelowens/AutoModerator/badges/coverage.svg)](https://codeclimate.com/github/michaelowens/AutoModerator/coverage)


# AutoModerator

A discord bot, configurable via a channel with YAML. Heavily inspired by AutoModerator for Reddit. Or a direct copy, you decide.

## Currently implemented

Conditions are put in the config channel configured in the `config.yml` file (#amconfig by default). Currently conditions accept the following keys:

- action
- channels
- dm
- domains
- message
- modifiers
- reply
- user
 - role

Currently the following modifiers are implemented:

- case-sensitive
- regex
- inverse

Currently the following match modifiers are implemented, only 1 of those can be used per condition:

- full-exact: `/^{0}$/`
- full-text: `/^\W*{0}\W*$/`
- includes: `/{0}/` *(default)*
- includes-word: `/(?:^|\W|\b){0}(?:$|\W|\b)/`
- starts-with: `/^{0}/`
- ends-with: `/{0}$/`
