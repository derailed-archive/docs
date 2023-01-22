# API Reference

Basic rundown of some standardized things throughout Derailed and our documentation.

## API Versioning

| version | status    | default |
| ------- | --------- | ------- |
| 1       | available |   yes   |

## Field Identifiers

- ! - This field is nullable
- ? - This field can be undefined
- !? - This field can be nullable or undefined

## Identification Standard

The entire Derailed API uses Twitter's Snowflake ID,
which consists of multiple fields.

The fields themselves will be detailed here soon but for now we'll be detailing only the Derailed Epoch.

The Epoch for Derailed is the first second of the first of January 2023 or `1672531200000`.

## Integer Reliability

In Derailed, depending on the circumstance, integers are unreliable.
If an integer goes over 32 bits, we will transform it into a string.

## Permissions

Permissions may be referred to in two fashions, "bit int" and "permissions"

When "bit int" is put, it means an integer holding the permissions itself.

When we use "permissions" though, we mean a permissions object:

| field         | type          |
|---------------|---------------|
| allow         | bit int       |
| deny          | bit int       |
