# JustifiedBar

[`JustifiedBar`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/JustifiedBar/index.js) renders up to three elements — `left`, `right`, and `center` — in a horizontal bar, guaranteeing consistent positioning regardless of the differing relative sizes \(or existence\) of the elements.

* `left` is always aligned to the left edge
* `center` is always at the horizontal center
* `right` is always aligned to the right edge

Each element can be anything renderable: String, Component, `null`, etc.

## Examples

**All equal-width elements**

```text
<JustifiedBar left='A' center='B' right='C' />

.-----------------------.
| A         B         C |
‘-----------------------’
```

**Larger** `right` **element**

```text
<JustifiedBar left='A' center='B' right='CCCCCCC' />

.-----------------------.
| A         B   CCCCCCC |
‘-----------------------’
```

**No** `left` **element**

```text
<JustifiedBar center='B' right='C' />

.-----------------------.
|           B         C |
‘-----------------------’
```

**No** `center` **element**

```text
<JustifiedBar left='A' right='C' />

.-----------------------.
| A                   C |
‘-----------------------’
```

