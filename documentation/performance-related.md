# Performance-related notations

## Fingerings


## Techniques
### Slides

Slides are to be encoded with the `<gliss>` element. The element has a tablature specific attribute `@slide` with possible values `legato` and `shift`. `@show.dirmark` indicates whether the `sl.` direction should be shown.

`@slide.to` and `@slide.from` attributes can take values `upwards` and `downwards` for slides with only one note (e.g., with only `@startid`)

### Legato techniques -- hammer on & pull off 

Hammer on and pull off are notated in a similar way – a slur over notes on the same course. Additional letters (H and P respectively) may optionally indicate which is involved, but this can be deduced from the direction – `hammer on` is up the finger board, `pull off` is down.
`<slur>` indicates the set of notes covered (see guidelines option 2 for meaning 'performance technique'), using `@startid` and `@endid`. `@show.dirmark` indicates whether letters are present. For more complex cases, the element can contain `<dirMark>` subelements whose text content indicates the letters used and whose startid *must* give the first note of the gesture.

### and tapping


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
