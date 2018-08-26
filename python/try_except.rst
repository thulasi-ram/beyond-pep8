============================
How to try .. except
============================

EAFP https://docs.python.org/3.5/glossary.html#term-eafp

https://blogs.msdn.microsoft.com/pythonengineering/2016/06/29/idiomatic-python-eafp-versus-lbyl/

#. Exception handling base exceptions and logging - https://realpython.com/the-most-diabolical-python-antipattern/

#. Always have returns within try. Example

    Prefer::

        try:
            do xx
            return
        except:
            do yy
            return

    than::

        try:
            do xx
        except:
            do yy
        return
