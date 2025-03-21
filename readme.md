# Overview
Xeto is a data-only type system.  The name is derived from the phrase "eXtensible
Explicitly Typed Objects".  Xeto defines a simple plain text format used to
declare types and to exchange typed data.  It is designed to build and validate
[Project Haystack](https://project-haystack.org/) data models.  But Xeto is general
purpose enough to use with any structured data including CSV, JSON, or SQL data.

Core development for Xeto is under the [Haxall Repo](https://github.com/haxall/haxall).
This repo provides additional supporting tools and libraries.

# Videos
The following series of videos provide instructions on how to use this software to validate data:

- [Overview](https://youtu.be/fr-K-MVbAa8): presentation of high level concepts

- [Axon Shell](https://youtu.be/9Bu1Rtd8VWE): setting up and getting around Axon shell

- [Axon Basics](https://youtu.be/17frHt2b4Ts): brief intro to Axon language

- [Type System](https://youtu.be/y2OVyS2jfbY): nominal and structural typing via typeof, isa, and fits

- [Queries](https://youtu.be/Q7Z3F1dkdQ4): name relationship queries

- [Constrained Queries](https://youtu.be/jZcFVCxLGek): create equip types with required points

# Change Log
Important changes since videos were recorded:

## Build 3.1.7.501 (28-Apr-2023)
- Runtime uses lib/xeto zip files with xetolib file extension

- Tools all work with src or zip (src is used if available)

- Run bin/xeto env to see how given xeto lib is loaded

- New bin/xeto json-pragma command to only parse lib meta into JSON

- Dist zip file includes HTML docs for specs now

- Start re-organization and enhancing ph.points

- Major refactoring of compiler to process inheritance at compile time

- Enhance instantiate() function with new graph option

- Add unloadAll() function to Axon shell

## Build 3.1.7.500 (24-Mar-2023)
- Axon shell allows you to evaluate new specs on the fly

- Qualified names now use double colon such as `ph.points::Sensor`

- Can load database from http URIs now too

- Query slot syntax is now `Equip.points` instead of `Equip->points`

- Functions that have been renamed:
   - `isa ->  is/specIs`
   - `query ->  queryAll`
   - `lintFit ->  fitsExplain`
   - `lintFindAllFits -> fitsMatchAll`

- New xeto command line tool to compile to JSON

- Subset of docs show data type functions (data lib)

# Setup

Xeto is packaged as a simple zip file with a command line tool that
requires the Java VM to run.  Steps to download and run:

1. Make sure you have Java installed

2. Download the latest [release](https://github.com/briansfrank/xeto-misc/releases)

3. Unzip to your local machine

4. You might need to run 'chmod +x' on the bin scripts (OS X)

5. Run 'bin/axon -v' to verify the install

6. Watch the videos above to learn how to use the axon shell to validate your data

# License
Protos is licensed under the [Academic Free License 3.0](https://opensource.org/licenses/AFL-3.0).


