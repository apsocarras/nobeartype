# nobeartype

Disable beartype's runtime type checking for a specific function, protecting it in case global runtime checking is on.
This is needed if your functions expose return types from external libraries like flask which beartype can't inspect.

IMHO, when using beartype it's best to enable it on a per-function basis or after import in your testing suite: `beartype_package('foo')`

You *could* use `beartype_this_package()` in `foo.__init__.py.` That's pretty hardcore, though.

<!-- BEGIN:NOBEARTYPE-EXAMPLES -->
<!-- Auto-generated from NoBearType docstring. Do not edit by hand. -->
<!-- END:NOBEARTYPE-EXAMPLES -->

## Testing

`python -m doctest` is my test suite. Coverage is 100%.
