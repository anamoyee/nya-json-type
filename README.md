# nya-json-type

Provide a `Json` type that is defined as follows:
```py
type Json = dict[str, Json] | list[Json] | str | int | float | bool | None
```

This type is supposed to be a typed return value of the builtin library `json`'s `.loads()`/`.load()` function

## Usage

```py
import json
from nya_json_type import Json

x: Json = json.load(open("data.json"))
```

## Motivation
This allows for typechecker narrowing. I know PyPI is not npm, but this small packages work fine for me and i was sick of having to cupy-paste that snippet of code everywhere.
	~nya
