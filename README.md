# WP Automation

Automation utilities, scripts and supporting libraries for workflow
automation projects — browser/task automation, data handling and
supporting tooling.

## Contents

| Path | Description |
| --- | --- |
| `app.js` | Main automation script (Node.js). |
| `pygtrie/` | **pygtrie** — a pure-Python implementation of a trie data structure, from Google's open-source project [google/pygtrie](https://github.com/google/pygtrie). Included under the Apache License 2.0 (see `pygtrie/LICENSE`). |

## About pygtrie

`pygtrie` is a drop-in trie library useful anywhere prefix lookups
matter — autocomplete, routing tables, keyword/command matching and
similar automation tasks:

- `Trie` — keys are tuples of elements (e.g. characters or words).
- `CharTrie` — string keys, with prefix queries such as
  `has_subtrie`, `longest_prefix` and `prefixes`.
- `StringTrie` — string keys split into components by a separator
  (handy for path-like keys such as `/home/user/photo.jpg`).

### Quick start

```python
import pygtrie

t = pygtrie.CharTrie()
t['foo'] = 'Foo'
t['foobar'] = 'FooBar'

print(t.prefixes('foobarbaz'))        # [('foobar', 'FooBar'), ('foo', 'Foo')]
print(t.longest_prefix('foobar'))     # ('foobar', 'FooBar')
print(t.has_subtrie('foo'))           # True
```

Run the bundled example and test suite:

```bash
cd pygtrie
python example.py
python test.py
```

## License

- `pygtrie/` is © Google and contributors, licensed under the
  **Apache License 2.0** — see [`pygtrie/LICENSE`](pygtrie/LICENSE)
  and the upstream project at https://github.com/google/pygtrie.
- The remaining content of this repository is the repository
  owner's own work.
