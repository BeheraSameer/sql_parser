C++ SQL Parser for Hyrise
=========================

This is a SQL Parser for C++. It parses the given SQL query into C++ objects.
It is developed for integration in hyrise (https://github.com/hyrise/hyrise), but can be used in other environments as well.


### Usage

To use the SQL parser in your own projects you simply have to follow these few steps. The only requirement for is GCC 4.8+. Older versions of GCC probably also work, but are untested.

 1. Download the [latest release here](https://github.com/hyrise/sql-parser/releases)
 2. Compile the library `make` to create `libsqlparser.so`
 3. Run the tests `make test` to make sure everything worked
 4. Take a look at the example project for reference.
 5. Include the `SQLParser.h` from `src/` and link the library in your project


### Development

**Prerequisites:**
* [bison](https://www.gnu.org/software/bison/) (tested with v3.0.2)
* [flex](http://flex.sourceforge.net/) (tested with v2.5.5)

First step to extending this parser is cloning the repository `git clone git@github.com:hyrise/sql-parser.git` and making sure everything works by running the following steps:

``` 
make parser   # builds the bison parser and flex lexer
make library  # builds the libsqlparser.so
make test     # runs the tests with the library
```

Rerun these steps whenever you change part of the parse. To execute the entire pipeline automatically you can run:

```
make cleanall  # cleans the parser build and library build
make test      # build parser, library and runs the tests
```

### License

HYRISE sql-parser is licensed as open source after the OpenSource "Licence of the Hasso-Plattner Institute" declared in the LICENSE file of this project.