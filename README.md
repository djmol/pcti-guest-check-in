# PCTI Guest Check-In

## Description

A simple iPad app to log guests into an event with their ticket number or name.

This consists of an Xcode workspace that holds two projects

- PromNight - the iPad app
- Loader - a Mac OS X app to preload the data for the iPad app.

The common data model is is in the Common folder and is referenced by both
projects.

## Usage

### Preload the database

To create the database to be used compile and run the loader program.

Click the "Load Data" button and navigate to the csv file that hold the data
to load. There is a `test.csv` file in the Common folder.

The store is recreated each time - loading data doesn't append new objects, it
creates a new store with the new data.

This has to be in the format 'firstName', 'lastName', 'ticketNumber' and the
file is expected to have the first row be the header. (This is important, becase
the first line is ignored).

After it runs you will see the number of items that it had to process, the
number of items successfully processed, and the location of the store that you
need to import into the iOS project.

The window shows where the `PromNight.sqlite` file has been created. Copy this
into the iOS project.
