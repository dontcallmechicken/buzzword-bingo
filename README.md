# Buzzword Bingo

A buzzword bingo with automatically generated bingo cards.

The project is a copy of bullshit-bingo:
https://github.com/domahidizoltan/bullshit-bingo

## General directory structure

```
buzzword-bingo/
├── index.html
├── cards
│   ├── buzzword
│   └── mybingo
└── files
    ├── css
    ├── js
    └── media
```

+ `index.html` – Home page with list of bingo cards
+ `cards` – Folder containing the bingo cards (each in its own subdirectory)
+ `files` – Globally used files
  - `css` – Stylecheets
  - `js` – JavaScript game files
  - `media` – Audio file
 
# Bingo cards
Create a new directory under the cards directory and copy existing sample files into the new directory.
Or copy an existing sample directory with existing files.

Required files:

+ `index.html`
+ `words.js`

```
buzzword-bingo/
└── cards
    ├── buzzword
    │   ├── index.html
    │   └── words.js
    └── mybingo
        ├── index.html
        └── words.js
```

## List of terms

Replace the words in the `words.js` file with your own ones. Keep the first and last line!  
Like this:

```
const words = `

Here comes your own words
Each one goes in a separate line

`;
```

## Bingo fields

There are three variations of the bingo grid, with different numbers of playable fields:

+ `index.html` – 4x4 grid, 16 fields
+ `index24.html` – 5x5 grid, 25 fields, one free (24 actively playable)
+ `index25.html` – 5x5 grid, 25 fields

### JavaScript game files

```
buzzword-bingo/
└── files
    └── js
        ├── content16.js
        ├── content24.js
        ├── content25.js
        ├── game16.js
        └── game.js
```

The `index.html` uses the `game16.js` and the `content16.js` for the bingo game.

The `index24.html` and `index.25.html` use the `game.js` and the appropriate content JavaScript file for the bingo game.

## Bingo Title 
The following HTML tags or elements should be adjusted in the `index.html` for the Bingo card:

+ `<title>` – The title of the HTML document
+ `<caption>` – The  table caption

Additionally for index24.html:

+ `<td class="freecell">` – A name, word, term for the free field in the middle of the bingo card

## Layout

There are stylecheet files that can be used globally.
Otherwise, you can copy one of the existing stylecheet files into the directory of the bingo card, rename it to `style.css` and adapt it.
You can also create your own stylesheet in the `files/css/` directory to use it globally.

```
buzzword-bingo/
└── files
    └── css
        ├── standard.css
        ├── summer.css
        └── winter.css
```

Within the `index.html` file for the bingo card, the following sequence is automatically loaded:

1. `files/css/standard.css`
2. `files/css/summer.css`  
or another predefined stylesheet file from the global directory
3. `style.css`

The last specified file that could be loaded is used.
This ensures that the bingo card is always displayed correctly.

If you want to use the standard stylesheet, it is sufficient to comment out the second CSS file.

## Audio

Every time the bingo cards page loads, an audio file is played.

Within the `index.html` file for the bingo card, the following sequence is automatically loaded:

1. bingo.ogg
2. bingo.mp3
3. files/media/bingo.ogg
4. files/media/bingo.mp3


First an audio file is loaded from the direct directory of the bingo card and then from the global directory.
The first audio file that could be loaded will be played automatically.

If you do not want audio output, you can comment out the audio element in the `index.html`.
Or you can rename or delete the audio file in the global directory.

> [!NOTE]
> Some browsers do not allow autoplay in most cases.  
> The audio will only play the first time the page loads, or never.  
> As a browser source within [OBS (Open Broadcaster Software)](https://obsproject.com/), the audio file will play every time it loads.

### Volume

In the `index.html` for the bingo card you can adjust the output volume in this script element:
```
<script>
  var audio = document.getElementById("bingosound");
  audio.volume = 0.2;
</script>
```

### Audio sample file

This is the example audio file used in this project:  
"Blop sound" by [helloIJustWantSomeSounds](https://freesound.org/s/609207/) at [Freesound](https://freesound.org/) under [Creative Commons 0](https://creativecommons.org/publicdomain/zero/1.0/) License.


# How to play

Open the `index.html` from the bingo card directory in a browser or add a link to the list of bingo cards in the `index.html` of the root directory.
Every time you refresh the page it will generate a new Bingo card.

Clicking on the caption of the bingo card takes you back to the home page, which is the `index.html` in the root directory.
The caption is formatted using the stylecheet so that it is not displayed as a regular link in the browser.

# Overview

Only required files:
```
buzzword-bingo/
└── cards
    └── mybingo
        ├── index.html
        └── words.js
```

Including all optional files:
```
buzzword-bingo/
└── cards
    └── mybingo
        ├── bingo.mp3
        ├── index24.html
        ├── index25.html
        ├── index.html
        ├── style.css
        └── words.js
```

Complete directory structure:
```
buzzword-bingo/
├── index.html
├── README.md
├── cards
│   ├── buzzword
│   │   ├── index24.html
│   │   ├── index25.html
│   │   ├── index.html
│   │   └── words.js
│   └── insult
│       ├── de
│       │   ├── index.html
│       │   └── words.js
│       └── en
│           ├── index.html
│           └── words.js
└── files
    ├── css
    │   ├── standard.css
    │   ├── summer.css
    │   └── winter.css
    ├── js
    │   ├── content16.js
    │   ├── content24.js
    │   ├── content25.js
    │   ├── game16.js
    │   └── game.js
    └── media
        └── bingo.mp3
```
