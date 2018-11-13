# Performance-related notations
## Fingerings


## Techniques
### Bends
Much of the core semantics of bends can be provided by `<bend>`.
#### Half-step and whole-step bend
```
<staff n="1">
  <layer>
    <note pname="e" oct="5" xml:id="note1" />
    <note pname="f" oct="5" xml:id="note2" />
    <bend startid="note1" endid="note2" />
  </layer>
</staff>
<staff n="2">
  <layer>
    <note tab.fret="9" tab.course="4" xml:id="note3" />
    <bend startid="note1" amount="" />
  </layer>
</staff>

```
### Sounding/striking techniques

### Tremolo bar techniques

### More-generic techniques
