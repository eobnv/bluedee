# Bluedee games

These 48 games are bundled in this repository, so Bluedee serves all of them itself and never relies on another site.

## Source and licence

All game pages and the shared language file `i18n.js` come from [mashukui/web-games](https://github.com/mashukui/web-games), by mashukui, which publishes them under the MIT License. The original licence text is kept in [LICENSE](./LICENSE). Each game page keeps its author credit.

## Games

2048, Air Hockey, Ant Flap, Ant Jump, Balloon Pop, Battleship, Block Drop, Bowling, Breakout, Bubble Shooter, Checkers, Connect Four, Cross Road, Dino Run, Fruit Slice, Gem Match, Gomoku, Tower of Hanoi, Helicopter, Helix Drop, Hoop Shot, Lights Out, Mahjong Link, Mancala, Maze Muncher, Memory Match, Merge Drop, Minesweeper, Mini Golf, Nonogram, Paddle Duel, Penalty Kick, Piano Tap, Pipe Connect, Reversi, Rush Hour, Simon Says, Slide Puzzle, Slingshot, Snake, Snakes and Ladders, Sokoban, Stack Tower, Star Defender, Sudoku, Tic-Tac-Toe, Water Sort, Whack-a-Mole.

## Changes made to the upstream files

- **Analytics turned off.** In `i18n.js`, `GC_SITE` is set to an empty string, which is upstream's documented way to disable its visitor counter. Nothing is loaded and nothing is sent.
- **"More games" link.** It now returns to the Bluedee home page (`../../`) and leaves the game frame, instead of pointing at the upstream collection's index.
- **Promo removed.** The footer link to an unrelated video-downloader site was removed from every game page. The author credit and the link to the upstream GitHub project are kept.

## Notes

- These pages load nothing from other sites, so they keep working when opened in an `about:blank` tab. The page that contains them still has to be served from the Bluedee site.
- Games save their scores and settings in your browser's local storage.
