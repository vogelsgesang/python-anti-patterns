Comparison to ``None`` should be ``if cond is None``
====================================================

Summary
-------

The preferred way of comparing something to ``None`` is the pattern ``if cond is None``. Statements that use the pattern ``if cond == None`` should be converted to the preferred style.

Description
-----------

Per the PEP 8 Style Guide, the preferred way to compare something to ``None`` is the pattern ``if Cond is None``. This is only a guideline. It can be ignored if needed. But the purpose of the PEP 8 style guidelines is to improve the readability of code. 

Examples
----------

Statement compares value to ``None`` using ``==``
....................

The statement below uses the equality operator to compare a variable to ``None``. This is not the PEP 8 preferred approach to comparing values to ``None``.

.. warning:: WARNING! The code below is an example of an error. Using this code will create bugs in your programs!

.. code:: python

    number = None

    if number == None:
        print "This works, but is not the preferred PEP 8 pattern for comparing values to None"


Solutions
---------

Compare values to ``None`` using the pattern ``if cond is None``
.................................................................

The code below refactors the comparison to ``None`` to use the PEP 8 preferred pattern of ``if cond is None``.

.. code:: python

    number = None

    if number is None:
        print "PEP 8 Style Guide prefers this pattern"

    
References
----------
- `PEP 8 Style Guide - Progrmaming Recommendations <http://legacy.python.org/dev/peps/pep-0008/#programming-recommendations>`_