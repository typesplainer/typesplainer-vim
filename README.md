# vim-typesplainer

A Vim plugin for the Python tool [typesplainer](https://github.com/wasi-master/typesplainer).

## Example

File:

```python
from typing import *

class Text:
  pass

def life(
  f: Callable[[str, int], Generator[int, str, bool]],
  g: Awaitable[Sequence[Text]]
) -> Dict[List[Set[FrozenSet[int]]], str]:
  return {[{frozenset(42)}]: "Hello World!"}

fromkeys: Callable[[List[int]], Dict[int, List[Union[Segment, None]]]]
```

Output:

```
Callable[[str, int], Generator[int, str, bool]] (example.py:7:6) : A callable that accepts a string and a integer and returns a generator that yields a integer, sends a string, and returns a boolean.
Awaitable[Sequence[Text]] (example.py:8:6) : A awaitable that returns a sequence of texts.
Dict[List[Set[FrozenSet[int]]], str] (example.py:9:6) : A dictionary that maps lists of sets of frozensets of integers onto a string.
Callable[[List[int]], Dict[int, List[Union[Segment, None]]]] (example.py:12:11) : A callable that accepts a list of integers and returns a dictionary that maps integers onto a list of optional segments.

Press ENTER or type command to continue
```

## Usage

The plugin can be used by executing either `:Typesplainer` or `:Tps`.

## Installation

Installing [typesplainer](https://pypi.org/project/typesplainer/) is required.

```bash
python -m pip install typesplainer
```

### [vim-plug](https://github.com/junegunn/vim-plug)

```vimscript
Plug 'KrazyKirby99999/vim-typesplainer'
```

## Misc

Thank you to wasi-master for creating typesplainer.
