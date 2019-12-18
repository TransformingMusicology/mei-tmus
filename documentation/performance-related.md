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
Much of the core semantics of bends can be provided by `<bend>`. Currently, notes participating in a bend have explicit pitch. This is not the case in guitar tablature bends, where displacement from non-bent pitch must be specified.

Bend displacements (`@dis`) are specified in number of semitones, and the textual content of the element indicates how the bend is specified in the source.

The simplest bends involve two explicit notes:

#### Two-note, whole-tone bend
```
    <tabGrp dur="16">
      <note tab.course="2" tab.fret="14" xml:id="note1" />
    </tabGrp>
    <tabGrp dur="16">
      <note xml:id="note2"/>
    </tabGrp>
    <tie startid="#note1" endid="#note2" />
    <bend startid="#note1" endid="#note2" dis="2">Full</bend>
```
Grace-note bends can be shown with `@startid` and no `@endid`:
#### Quick, unmeasured bend
```
    <tabGrp dur="16">
      <note tab.course="2" tab.fret="14" xml:id="note1" />
    </tabGrp>
    <bend startid="#note1" dis="2">1</bend>
```
Prebends use another new attribute `@prebend`:
#### Simple prebend
```
    <tabGrp dur="16">
      <note tab.course="2" tab.fret="14" xml:id="note1" />
    </tabGrp>
    <bend startid="#note1" dis="1" prebend="true">1/2</bend>
```


### Sounding/striking techniques

### Tremolo bar techniques

### More-generic techniques
