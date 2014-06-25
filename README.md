generic TLD Launch Informations
===============================

We would like to simplify the process of announcing new launching TLDs and their individual launch phases by defining a general file format for public exchange.

## File Format

To make it easy to add and edit events the file format for this purpose should be a human readable and writeable format - like CSV [RFC4180](http://www.ietf.org/rfc/rfc4180.txt).

Each new row is delimited by a single newline (`\n`). All fields are enclosed in double-quotes (`"`) and seperated by comma (`,`).

## Fields

Following fields need to be added in every row:

| Field | Description |
| :-------- | :----------- |
| TLD | TLD to update/add an event to - written in punyencoded (to prohibited charset errors) |
| Launch Phase | Possible values:<ul><li>SR (Sunrise),<li>LR (Landrush),<li>EA (Early Access),<li>GA (General Availability), <li>OT (Other)</ul> |
| Start | Phase Start - written as defined in [RFC3339](http://www.ietf.org/rfc/rfc3339.txt) - 2011-01-01T12:00:00Z |
| End | Phase End. Must not be set for GA |
| Description | Additional Text to descripe this Phase - for example if Phase is only available for special region |

## Sample

A simple file could be found [here](https://raw.githubusercontent.com/ntldstats/ntldstats_launch/master/sample.csv).
