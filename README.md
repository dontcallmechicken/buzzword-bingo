The project is a fork of bullshit-bingo:
https://github.com/domahidizoltan/bullshit-bingo


# Bullshit Bingo

This is an offline copy of the Bullshit Bingo game from the [Bullshit Bingo site](https://www.bullshitbingo.net/).  

Replace the words in the `words.js` file with your own ones. Keep the first and last line!

Like this:
```
const words = `

Here comes your own bullshits
Each one goes in a separate line

`;
```

Open the `index.html` in a browser. Every time you refresh the page it will generate a new Bingo card.  
Print it or play it on your laptop. Have fun!



# Struktur und Aufbau
## Verzeichnis parts
Das Verzeichnis `parts` beinhaltet die JavaScript Dateien, die zum generieren und spielen der jeweiligen Bingokarten benötigt werden:

- `content.js`
- `game.js`

Im selben Verzeichnis befindet sich auch eine Standard Stylecheet Datei, die u.a. die Bingokarte `buzzword` verwendet.

## Verzeichnis cards
In dem Verzeichnis `cards` liegen alle Bingokarten in je einem eigenen Verzeichnis, benannt nach dem jeweiligen Bingo-Thema.

### Struktur Bingo-Verzeichnis

- `index.html`
- `words.js`
- `style.css` (optional)
- `bingo.mp3` oder `bingo.ogg` (optional)

### Verzeichnis files
- `style.css`

