# XML Parser

An exercise I completed as part of the *Advanced Practical Programming for Scientists* module at the Technische Universität Berlin in 2017.

Documentation generation requires [doxygen](https://www.doxygen.nl/).

* compile: `g++ -std=c++11 -O3 xml_parser.cxx -o xml_parser -lxerces-c`
* run: `./xml_parser <xml filepath> [-V]`
* include `[-V]` flag to enable schema validation
* **xml_parser.cxx** uses the Xerces-C library for XML parsing. Accepts XML filepath as argument. Prints output to csv.txt. `[-V]` flag determines if XML file is to be validated. Namespace-location pair of external schema is fixed as `"http://gaslab.zib.de/kwpt/measured ./measured-1-1-0.xsd"`.
* Validation errors for given xml-xsd:
    * `line #2 column #1081: value '1.0.0' does not match regular expression facet '1\.1\.0'.`
    * `line #2 column #1081: attribute 'validity' is not declared for element 'measured'.` 

---

Available make commands:
* `make all`
* `make doc`
* `make coverage`
* `make check`
* `make clean`
