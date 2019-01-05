# JustifiedBar

[`JustifiedBar`](/src/components/JustifiedBar/index.js) renders up to three elements — `left`, `right`, and `center` — in a horizontal bar, guaranteeing consistent positioning regardless of the differing relative sizes (or existence) of the elements.

- `left` is always aligned to the left edge
- `center` is always at the horizontal center
- `right` is always aligned to the right edge

Each element can be anything renderable: String, Component, `null`, etc.

## Examples

**All equal-width elements**

```es6
<JustifiedBar left='A' center='B' right='C' />

.-----------------------.
| A         B         C |
‘-----------------------’
```

**Larger `right` element**

```es6
<JustifiedBar left='A' center='B' right='CCCCCCC' />

.-----------------------.
| A         B   CCCCCCC |
‘-----------------------’
```

**No `left` element**

```es6
<JustifiedBar center='B' right='C' />

.-----------------------.
|           B         C |
‘-----------------------’
```

**No `center` element**

```es6
<JustifiedBar left='A' right='C' />

.-----------------------.
| A                   C |
‘-----------------------’
```
