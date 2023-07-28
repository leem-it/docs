# Leemit

> start optimizing your time

## The Documentation

Leemit is a productivity app, its main feature is time tracking.

This is the documentation to the RESTful api.
\
The current api endpoint can be found at `api.leem.it`

## Conventions

The app will follow whenever possible the RESTful conventions. Requests must be sent over https at `https://api.leem.it`

### DateTime

Datetime values are expected to be encoded as ISO-8601 strings.
The user can specify a different timezone, but the returned datetime will always be in UTC

### Colors

Colors are expected to be as hex values (ex. '#ff11ff')
