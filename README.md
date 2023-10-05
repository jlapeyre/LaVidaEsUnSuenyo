# *La Vida Es Un Sueño*

*La Vida Es Un Sueño* was composed by [Arsenio Rodriguez](https://en.wikipedia.org/wiki/Arsenio_Rodr%C3%ADguez) and performed by
his *conjunto*[^1].

This repository contains a [transcription](la_vida_es_un_sueño.pdf) of the guitar ([Marc Ribot](https://en.wikipedia.org/wiki/Marc_Ribot)) and
bass ([Brad Jones](https://en.wikipedia.org/wiki/Brad_Jones_(bassist))) parts from a recording of an arrangement by
[*Marc Ribot y Los Cubanos Postizos*](https://www.marcribot.com/marc-ribot-y-los-cubanos-postizos).

I made this transcription in 2005. This page is an edited and updated version of what I wrote then.

* [Files](#files-in-the-repository)
* [Some recordings](#some-recordings)
* [Notes on transcription](#notes-on-transcription)
    * [Annotations for guitar](#annotations-for-guitar)
        * [Chords and Frets](#chords-and-frets)
        * [Articulation](#articulation)
    * [Midi](#midi)
    * [Structure of the Piece](#structure-of-the-piece)
    * [Small performance hints](#small-performance-hints)
    * [Detailed bar-by-bar notes](#detailed-bar-by-bar-notes)
        
## Files in the repository

* [`la_vida_es_un_sueño.pdf`](la_vida_es_un_sueño.pdf) Score (engraving) of guitar and bass parts.
* [`la_vida_es_un_sueño.midi`](la_vida_es_un_sueño.midi) Midi file generated (crudely) from the score.
* [`la_vida_es_un_sueño.ly`](la_vida_es_un_sueño.ly) LilyPond source for the guitar parts
* [`la_vida_es_un_sueño-bass.ly`](la_vida_es_un_sueño-bass.ly) LilyPond source for the bass parts.

A transcription in LilyPond is a plain-text source file (with suffix `ly`). So it is
well suited for living in a git repo. If you care about mistakes or improvements, you can
open an issue here.

### Building the pdf and midi

You can build the pdf and midi files with the command
```shell
lilypond la_vida_es_un_sueño.ly
```

## Some recordings

Putting together this repo in 2023, I discovered that since I did the transcription 2005,
many more recordings of the song available. I don't want to list all that I found,
but here are a few that I find most interesting.

* [Arsenio Rodriguez](https://www.youtube.com/watch?v=8cwTPzxPdmE)
* [Johnny Rodriguez y su Trio](https://www.youtube.com/watch?v=bjBARq2RxTo)
* Arranged for [alto saxophone (Miguel Zenón) and piano (Luis Perdomo)](https://www.youtube.com/watch?v=3vigOkTKKew)
* [Daniel Santos](https://www.youtube.com/watch?v=-pgnnHcIYr4)
* [Charlie Figueroa](https://www.youtube.com/watch?v=JKUGsOkPdl8)
* [Los Provincianos](https://www.youtube.com/watch?v=32y2z_USMMs)
* [Carlos Cuevas y los Tres Reyes](https://www.youtube.com/watch?v=D20-dRzbV2Q), [and here too](https://www.youtube.com/watch?v=FL7z8PPt4t4).


## Notes on transcription

> [!IMPORTANT]  
> This is my first transcription, the first time I have
> written down music in any notational system, the first time
> I have studied chords, etc. I learned most of the music
> theory using the "this guy on the internet" method. My choices
> of notating enharmonic pitches may often be wrong.
> I don't recommend trying to learn about these subjects in
> general from this document.

### Annotations for guitar

#### Chords and Frets

  I began putting fret diagrams on the score simply to
notate easily where to put my fingers, because in several
sections Ribot plays a chord or broken chord or arpeggio
with an immobile left hand. I began to put chord symbols
(ie, names `G`, `Am`, etc.) over the fret diagrams that
corresponded to obvious chords. Then I began to try to find
the chords for all of the music. The result is that the
chord symbols don't have a single purpose. They may be a
literal interpretation of the fret diagram. They may
represent the chord that I think Ribot and Jones may have in
mind during a bar. They may represent what I think is the basic
chord in the progression without a substitution.

 Instead of fret diagrams, I sometimes use an approximation
of standard classical guitar notation by putting arabic
numerals above note heads to indicate left hand
fingering. Likewise I sometimes use italic roman numerals to
indicate left hand position, and circled arabic numerals to
indicate the string. A zero with a tail is borrowed from
cello notation to indicate fretting with the thumb. I would
like to indicate barres and the duration of positions more
accurately, but all of this is laborious in
LilyPond. Unfortunately, it is not possible include the
standard notation for string bends in transcribed blues
guitar. I have tried to indicate some of this with the word
"bend" and text notes below. I have used a cup above notes
to indicate a quarter bend. These are never really quarter
bends, but indications to listen carefully at that bar for
how the guitarist bends the note.  Slurs indicate hammerons
and pulloffs.  Glissandos are indicated by straight lines
(sometimes too short or misshapen, depending on how much
effort I was able to put into fighting LilyPond), and
represent slides.

Barres are not notated, but should not be hard to figure out.

#### Articulation

I use the tenuto symbol, a bar over a note head, to indicate
that a note is held; a staccato symbol, a dot, to indicate
that a note is shortened; and a portando symbol, a line and
a dot, to indicate that the note is shortened a bit more
than if playing legato or normally.  But they are a rather
crude approximation of the articulation and rubato on the
recording and are merely reminders to listen carefully to
the articulation at that postion in the piece.

### Midi

The midi file is generated automatically by LilyPond from the
score. It is useful for hearing wrong intervals and rhythms. However, if you listen to
it expecting to find music, you will find anti-music.

Generating the midi was rather complicated: (Note: Recent versions of LilyPond
are better than the description below, written in 2005)
The midi that LilyPond generates from is wrong
dynamically and the the bass and guitar will go out of
sync. Glissandos to and from nowhere must be marked by
making glissandos to hidden grace notes. The note is marked
grace so that it occupies no time in the bar. It is marked
hidden so that it doesn't print. But the midi file, not
only does not hide grace note, but lets it occupy time. So I
stripped these commands as well.

### Structure of the piece

The song (the recording of the song by *Los Cubanos Postizos*)
has an A B A B A A structure with variations in all repeated
parts. Each of A and B is a chord progression.  Bars 1-11
are A and consists of solo guitar, with tremelo and not too
much distortion and probably finger picked.  Bars 12-23 are
B and add spoken vocals.  Bars 24-31 are A played a bit
differently and with sung vocals.  Bars 33-45 are B and are
the guitar solo. The arrangement here uses distorted guitar,
electric bass guitar, organ (or something like that) and
some kind of stick, maybe claves. Bars 46-53 and 54-61 are A
done twice with the same instrumentation as the previous
section but added sung vocals and maybe some other
noises. Bars 62-64 are an outro consisting of solo guitar.

### Small performance hint

I play bars 1-32 mostly with my thumb and fingers when
necessary.  I use the side and a bit of nail for louder or
more percussive notes and rotate the thumb and use more pad
for the soft notes. I played it on a telecaster with the neck
pickup and electronic rotating tremelo.  ~~I don't know what
Ribot uses.~~ In the meantime I have found youtube videos of
Ribot playing LVEUS on a Gibson hollow body.
But, I've freuquently seen him play a telecaster.
It sounds like he arpeggiates, at least
slightly, every chord, which makes me think he may be
strumming somehow. I play the rest of the song with a pick
and more distortion and no tremelo.

### Detailed bar-by-bar notes

#### Introduction Bars 1 -- 11

##### Bar 4

I need to check this again. It is seems that the
space of five eight notes are occupied by seven even
beats. The notes are all in the `GMaj` scale except for
`Bb`. The first five notes form a `CMaj7`.

##### Bar 5

This maybe something like a `C#m` chord. It is probably
related to the last dyad of [bar 4](#bar-4).

##### Bar 7

The first five notes are `E7`. Almost the same as [bar 27](#bar-27).

##### Bar 8
The (1, 2, 3b and 5) from `A` major scale are here. Very
similar to [bar 28](#bar-28). In bar 8 dyads consisting of minor
thirds above each melody note are present (lowered an
octave). In bar 28, the same notes are present, but with
minor thirds below each melody note.

#### First Verse bars 12 -- 23

##### Bar 16

If the bass were here, it would be walking chromatically
down from A to F#. One might consider the root to be on A
the whole time, rather than walking down. I think the
chromatically changing root is probably the correct way to
think about it. Anyway I marked the chords both ways.

#### Second Verse bars 24 -- 31

##### Bar 25

This chord has the notes `C# G Bb E` and can be interpreted as
`1 3b 5b 6` with any of the four notes taken as the root (with inversions).
Since the chord is arpeggiated, the ambiguity over which is the
tonic may be enhanced.

#### Guitar Solo bars 32 -- 45

##### Bar 33

Starts with 3,5 of `G` chord. The `3b` appears as well.  These
plain major and minor chords (and distortion and volume)
produce a sudden rocky feel compared to the piece up to this
point.

##### Bar 34
  `G Maj`, or `Gmin` ?  Not clear whether this is a major or
minor or blues scale. Other than (`1`, `3`, `3b`, `5`) only `2`, the `A`
appears.  The bass plays (`1` `3` `5`) of `G Maj`. An alternate
position, that I prefer, for the notes after the rests is
the tenth position.

##### Bar 35

This measure fits well with a strummed `B` or `B7`. The bass
player plays `1` and `5` of `B`. The last note in the measure is
`3b`, but it does not give a minor character to the bar. The
guitar enters with `7b` and `4` of `B`. Most following notes are
in the `G` M scale. The 4th and 5th of `B` are present.

##### Bar 36

Starts with arpeggiating an `Am` triad, then walks the bass
down.

##### Bar 39

This software can't (check this) do notation for bends in blues
guitar. Both notes in this bend (written as a slur) are
struck. The first note is struck as a `C` and bent quickly to
a `D`. After holding the `D`, it is lowered quickly and struck
as a `C`. There is (no?) standard notation for this extremely common
blues licklet.

##### Bar 41

Hits all of and only `G` major scale. This makes an
obvious contrast with the blues scale in the previous bar.

##### Bar 42

The notation for the rhythm here is a bit awkward.  The
triplet counts for one eighth note. The actual rhythm steals
somewhere between a 32nd and a 64th from the eighth note. I
wonder if this is what Ribot meant when he talked about
Monk's rubato, I have not listened that closely to Monk.

##### Bar 43

Guitar enters playing `1` and `3` of `B`. Descends chromatically to
`B` and descends here with (`1` `5+` `4` `7`) then ascends
chromatically to `E` for the next bar. Bass plays (`1`,`3`,`5`,`7b`)
of `B`.

#### Verses without words, bars 46 -- 53, and 54 -- 61

##### Bar 46

Can barre with 3rg f. (what did I mean to write?) . An alternate fingering is to play
`g-3` and barre `c-4` and `e-4`.

### Footnotes

[^1]: There are a few well-known, but unrelated, songs also called *La Vida Es Un Sueño*. In
particular, one of these songs, covered by young, contemporary pop stars, has a bigger online
presence.


