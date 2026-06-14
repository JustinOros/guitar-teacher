# 🎸 GuitarTeacher

An interactive, mobile-friendly web app for learning guitar - built entirely as a single HTML file with no dependencies or build tools required.

**Live app:** [https://justinoros.github.io/guitar-teacher](https://justinoros.github.io/guitar-teacher)

---

## Features

- **8 progressive lessons** - from how to hold a guitar all the way to playing real songs
- **Interactive fretboard** - visual dot-based tab display showing exactly which string and fret to play
- **Microphone pitch detection** - the app listens through your mic and confirms when you play the right note
- **🎸 Play Along mode** - a guitar icon moves across the fretboard dot by dot, waits for you to play each note, turns green when correct, and gives you encouragement when you finish
- **70+ songs** across Country, Rock, Classic Rock, Pop, Folk/Indie, and Rap - searchable by title, artist, genre, or difficulty
- **Browse by difficulty** - filter songs by Beginner, Intermediate, or Advanced
- **Lyrics links** - one tap opens the lyrics on Genius or Google so you can sing along
- **Morgan Wallen library** - 12+ Morgan Wallen songs built in
- **Offline-capable** - once loaded, works without an internet connection

## Song Library Includes

| Genre | Artists |
|-------|---------|
| Country | Morgan Wallen, Kane Brown, Luke Combs, Thomas Rhett, Luke Bryan, Brett Young, Ella Langley, Dierks Bentley, Keith Urban, Lady Antebellum, Josh Turner, Old Dominion, Bailey Zimmerman, Jason Aldean, Lee Brice |
| Classic Rock | Pink Floyd, Eagles, Eric Clapton, Van Morrison, Lynyrd Skynyrd, Bob Dylan, The Animals |
| Rock | Nirvana, Radiohead, The White Stripes, Deep Purple, The Cranberries, Bloodhound Gang, Gotye |
| Pop/Rock | Coldplay, Oasis, The Cranberries |
| Pop | Ed Sheeran, Sam Smith, Vance Joy, Lady Gaga |
| Folk/Indie | The Beatles, Jack Johnson, The Lumineers, Tracy Chapman |
| Rap | Dan Henig (acoustic Get Low) |

## How to Use

### Play Along
1. Search for a song or browse by genre/difficulty
2. Tap **🎸 Play Along** - the mic turns on automatically
3. Play the highlighted note on your guitar
4. The dot turns green, the 🎸 icon moves to the next note
5. Finish the song and get a word of encouragement!

### Lessons (beginners)
Work through all 8 lessons in order:
1. How to Hold a Guitar
2. Reading Guitar Tab
3. Your First Notes (open strings)
4. Your First Chord: Em
5. G, C, and D Chords
6. Play-Along Songs
7. Keep Going
8. Search Any Song

## Deployment

This is a single `index.html` file with no build step required.

### GitHub Pages setup
1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set Source to **Deploy from branch → main → / (root)**
4. Your app will be live at `https://[your-username].github.io/guitar-teacher`

### Run locally
Just open `index.html` in any browser. No server needed.

## Tech

- React 18 (loaded from CDN)
- Babel standalone (JSX transpiled in browser)
- Web Audio API for real-time pitch detection via autocorrelation
- SVG for fretboard rendering
- Zero npm dependencies, zero build tools

## Contributing

Pull requests welcome! To add songs, edit the `SONG_LIBRARY` array in `index.html`. Each song follows this shape:

```json
{
  "title": "Song Title",
  "artist": "Artist Name",
  "genre": "Country",
  "diff": "Beginner",
  "chords": ["G", "C", "D"],
  "capo": 0,
  "parts": [
    {
      "name": "Verse",
      "tab": {
        "e": "--3---0---",
        "B": "--3---1---",
        "G": "--0---0---",
        "D": "--0---2---",
        "A": "--2---3---",
        "E": "3---------"
      },
      "notes": ["G4", "C4", "D3"]
    }
  ],
  "tips": "Optional beginner tip for this song."
}
```

Tab strings must all be the same length. Notes use format `E4`, `A2`, `G3` etc.

---

Made with ❤️ for guitar beginners everywhere.
