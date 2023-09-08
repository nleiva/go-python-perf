# Simple performance tests

## Install PyPy

[Download a pre-built PyPy](https://doc.pypy.org/en/latest/install.html#download-a-pre-built-pypy)

```bash
dnf install bzip2
wget https://downloads.python.org/pypy/pypy3.10-v7.3.12-linux64.tar.bz2
tar -xvf pypy3.10-v7.3.12-linux64.tar.bz2
```

## Tests

### CPython

```bash
⇨  time python performance.py
Done

real	0m47.680s
user	0m47.615s
sys	    0m0.006s
```

### PyPy

```bash
⇨  time ./pypy3.10-v7.3.12-linux64/bin/pypy performance.py
Done

real	0m0.462s
user	0m0.449s
sys 	0m0.012s
```

### Go

```bash
⇨  time go run performance.go
Done

real	0m0.281s
user	0m0.288s
sys	    0m0.065s
```

### Compiled Go

```bash
⇨  time ./perf
Done

real	0m0.216s
user	0m0.213s
sys	    0m0.003s
```
