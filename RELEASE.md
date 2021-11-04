Release type: minor

This release updates how we generated names when creating concrete types
from generic types. It also introdiced support for passing lists and optional
to generic types.

So now `Value[Optional[List[str]]]` will generate `ValueOptionalListStr` instead of
`StrListOptionalValue` which was the previous behaviour.

**Note:** the name generation is a breaking change if you use generic types,
so you might need to update your clients.
