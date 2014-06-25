Sample Data for generic TLD Launch Informations
===============================================

We'd like to simplify the process of announcing new launching TLDs and their individual launch phases by defining a general file format for public exchange.

## File Format

To make it easy to add and edit events the fileformat for this purpose should be a human easy readable and writeable format - like CSV [RFC4180](http://www.ietf.org/rfc/rfc4180.txt).

Each new row is delimited by a single newline (`CHR #13 / \n`). All fields are enclosed in double-quotes `"` and seperated by comma `,`.

## Fields

Following fields need to be added in every row:

| Field | Description |
| :-------- | :----------- |
| TLD | TLD to update/add an event to - written in punyencoded (to prohibited charset errors) |
| Launch Phase | Possible values: SR (Sunrise), LR (Landrush), EA (Early Access), GA (General Availability), OT (Other) |
| Start | Phase Start - written as defined in [RFC3339](http://www.ietf.org/rfc/rfc3339.txt) - 2011-01-01T12:00:00Z |
| End | Phase End. Must not be set for GA |
| Description | Additional Text to descripe this Phase - for example if Phase is only available for special region |
