# SnD
Spec, newline, Data

```
example.com/some-struct#v3
<binary>
```

## Inspection

```bash
cat <file path> | head -n 1 | xargs curl
```

## Recommendations

### Byte alignment

For binary formats that require non-byte alignment you might need to control the byte length of the first line, for example, if the data format is an array of `u64`, you should prepend `%20` (space) characters before the `\n` (newline) to round the first line's byte length to the nearest multiple of 8 bytes.


## Acknowledgements

Thanks to [Age](https://github.com/C2SP/C2SP/blob/main/age.md#header) for the inspiring example.

Thanks to [Aaron Goldman](https://github.com/AaronGoldman) for the name.

Thanks to [Rüdiger Klaehn](https://github.com/rklaehn) for the byte alignment note.
