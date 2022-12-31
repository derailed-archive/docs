# Introduction

Welcome! This is the documentation for Derailed's API.

This includes everything from our Gateway, to API.

## Field Identifiers

- ! - This field is nullable
- ? - This field can be undefined
- !? - This field can be nullable or undefined

## Identification Standard

The entire Derailed API uses Twitter's Snowflake ID,
which consists of multiple fields.

The fields themselves will be detailed here soon but for now we'll be detailing only the Derailed Epoch.

The Epoch for Discoursy is the first second of the first of January 2023 or `1672534801000`.

## API Versioning & Routing

Derailed's API & Gateway are interconnected, allowing you to use them both at once.
Take note though: **this will eventually be disconnected and they'll be separated**.

For now the only version is 1 for both the API and Gateway.
