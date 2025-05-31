# Computer Science

## Python

### Useful links

- [Python Glossary](https://docs.python.org/3/glossary.html)

### CPython interpreter 
- canonical implementation of Python
- uses GIL to assure that only 1 thread executes Python bytecode at a time
- thus, object models (e.g. dict) are *implicitly* safe against concurrent access
- GIL is released by some modules, or when doing I/O.
- GIL can be disabled to improve multi-threading performance OR use multi-core CPUs:
- How? --disable-gil, then run with -X gil=0 or PYTHON_GIL=0 (see PEP 703)

### Paralellization
- Functions implemented in C may use multiple threads internally. For example, Intel’s NumPy distribution, PyTorch, and TensorFlow all use this technique to internally parallelize individual operations. ([source](https://peps.python.org/pep-0703/#internal-parallelization))

