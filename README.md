
# Sports Bingo

It turns out that I get pretty repetitive when I'm watching sports, so I decided to build out a Bingo game that my friends and family can play while they're listening to me. It's inspired by [this Bingo board for the Carolina Hurricanes](https://bingo.svech.net) by Erin Morelli ([@ErinMorelli](https://github.com/ErinMorelli)).


# How to Use
You'll want to create a `squares.json` in the same folder as the `index.html`, and create "squares" with the following syntax:

```json
{
    "title": "Ari claps rapidly",
    "description": "Specifically, rapid claps in a row.",
    "type": "*"
}
```

* The `title` is what'll appear on the square itself,
* The `description` will appear when you hover on the square, and
* The `type` will determine which game type it'll be eligible for (see below).

## Game Types

By default, the board supports the NHL (as `nhl`) and the NFL (as `nfl`), both of the sports that I watch (Go Hurricanes, Go Commanders!). You can also set a `type` value to `*` to allow it to show up in any game type.

If you want to add a new game type/sport, just add it to the dropdown at index.html:92, and start creating squares in `squares.json`.

## Game Modes

There are two "modes that you can play in:
1.  **One Player Mode**<br>When you click on a square, it'll toggle between a dark gray (to represent that a square has been "activated) and the white default mode.<br><br>
2. **Two Player Mode**<br>When you click a square, it'll toggle between pink (when Player 1 has gotten the square) a light blue (when Player 2 has gotten the square), and a diagonal split of the two (to show that both players have gotten it). 

## Seeding
Each time you generate a new board, you can find that board's seed by looking at the bottom of the board. If you want to have multiple folks on the same board, they can go into "Game Options" and put the seed into the box there.
