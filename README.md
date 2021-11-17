# Melon Tasting Reservation Scheduler

**Objective:** build a simple service to help useres make reservations

## Table of Contents
1. [Tech Stack](#tech-stack)
2. [Assignment Info](#assignment-info)
    - [User Flow](#user-flow)
    - [Service Requirements](#service-requirements)
    - [Frontend Info](#frontend-info)
3. [Data Model](#data-model)
4. [Considerations](#considerations)
5. [Decisions Explained](#decisions-explained)

## Tech Stack

Python, Flask, SQLAlchemy, PostgreSQL, SQL (SQLite?)

## Assignment Info

### User Flow

1. A user should be able to:
    - log in (by entering their username)
    - pick a date
    - choose an optional time range
    - be shown all available reservations that meet the criteria
2. The user can book an appointment of their choice.
    - if no reservations are available, a message should be displayed to inform the user
3. There should be a page which shows all reservations for a given user.

### Service Requirements
- all reservations must start and end on the hour or half hour
- all reservations are exactly 30 minutes long
- a user can only have 1 reservation on a calendar date

### Frontend Info
1. simple login screen
2. page to search for appointments
3. results page to view results of appointment search
4. page to view all scheduled appointments for the current user

*[Click here](#melon-tasting-reservation-scheduler) to go back to the top.*

## Data Model

Work in progress!

*[Click here](#melon-tasting-reservation-scheduler) to go back to the top.*

## Considerations

Work in progress!

*[Click here](#melon-tasting-reservation-scheduler) to go back to the top.*

## Decisions Explained

1. Flask is lightweight, so it's great for building application prototypes.
    - pro: able to build features quickly
    - con: not as structured as larger frameworks like Django
2. Melon data is encoded using CSV-like syntax and stored as a text file
    - pro: acts like a database, can update file to expand inventory, info is persistent
    - con: not as efficient or scalable as a database
        - but we don't need to write to the file efficiently (not updating melon inventory)
3. Created Python module called `melons` which has a devloper-friendly API for retrieving data from file
    - generic API, so we can use this for other databases with a couple of edits
    - pros: API makes it easier for other developers to join the project because code is more readable and easier to work with
    - cons: needs documentation to be truly developer-friendly; may consider how we are retrieving data
        - can we design a modular way to retrieve data from any data source?

*[Click here](#melon-tasting-reservation-scheduler) to go back to the top.*
