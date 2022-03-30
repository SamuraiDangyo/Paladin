![Paladin](https://github.com/SamuraiDangyo/Paladin/blob/main/logo.png)

# Paladin

Linux mayhem chess variant engine.
Started as Mayhem chess960 engine.
100% UCI support as in Mayhem.
Designed to be GUI independent. You only need the binary.

## Link to the variant

[Mayhem Chess variant](https://www.chessvariants.com/diffsetup.dir/mayhem.html)

## Demo / Release

v0.1 of real Paladin is released to the public

## Signatures

```
perft -> 222447094
bench -> 9154591
```

## Mayhem variant StartPos

```
anpqkpna/p1r2r1p/1p1pp1p1/8/8/1P1PP1P1/P1R2R1P/ANPQKPNA w 0 1
```

## Mayhem chess Rules

Normal chess rules except ...

- The paladin is archbishop N+B
- The Janus pawns (= pawns) may capture forward and backward
- Castling is not permitted
- En passant captures are not legal
- The Queen is restricted to 4 moves max

## Board

```
p

 +---+---+---+---+---+---+---+---+
 | a | n | p | q | k | p | n | a | 8
 +---+---+---+---+---+---+---+---+
 | p |   | r |   |   | r |   | p | 7
 +---+---+---+---+---+---+---+---+
 |   | p |   | p | p |   | p |   | 6
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 5
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 4
 +---+---+---+---+---+---+---+---+
 |   | P |   | P | P |   | P |   | 3
 +---+---+---+---+---+---+---+---+
 | P |   | R |   |   | R |   | P | 2
 +---+---+---+---+---+---+---+---+
 | A | N | P | Q | K | P | N | A | 1
 +---+---+---+---+---+---+---+---+
   a   b   c   d   e   f   g   h
> anpqkpna/p1r2r1p/1p1pp1p1/8/8/1P1PP1P1/P1R2R1P/ANPQKPNA w 0 1
```

## Perft (startpos)

```
perft 5 anpqkpna/p1r2r1p/1p1pp1p1/8/8/1P1PP1P1/P1R2R1P/ANPQKPNA_w_0_1
1. a2a3 -> 4727934 (94 ms)
2. a2a4 -> 4920704 (87 ms)
3. h2h3 -> 4721448 (83 ms)
4. h2h4 -> 4921393 (87 ms)
5. b3b4 -> 5156646 (91 ms)
6. d3d4 -> 4103216 (71 ms)
7. e3e4 -> 3958820 (69 ms)
8. g3g4 -> 4641706 (84 ms)
9. b1d2 -> 4325597 (77 ms)
10. b1a3 -> 4589317 (83 ms)
11. b1c3 -> 3443355 (61 ms)
12. g1e2 -> 3712932 (69 ms)
13. g1f3 -> 3069883 (54 ms)
14. g1h3 -> 4604362 (82 ms)
15. a1b2 -> 5061733 (91 ms)
16. a1c3 -> 4684728 (84 ms)
17. a1d4 -> 5625168 (100 ms)
18. a1e5 -> 5256626 (95 ms)
19. a1f6 -> 293990 (5 ms)
20. a1g7 -> 436647 (8 ms)
21. a1h8 -> 3944857 (70 ms)
22. d1e2 -> 4323892 (77 ms)
23. d1f3 -> 4305133 (72 ms)
24. d1g4 -> 6869211 (119 ms)
25. d1h5 -> 6988017 (119 ms)
26. h1g2 -> 5141167 (92 ms)
27. h1f3 -> 4508861 (81 ms)
28. h1e4 -> 5755226 (101 ms)
29. h1d5 -> 5699149 (100 ms)
30. h1c6 -> 651716 (12 ms)
31. h1b7 -> 5158941 (91 ms)
32. h1a8 -> 4185375 (73 ms)
33. d1d2 -> 4399728 (76 ms)
34. c2b2 -> 3747195 (67 ms)
35. c2d2 -> 4156687 (74 ms)
36. c2e2 -> 3408403 (62 ms)
37. c2c3 -> 3829865 (67 ms)
38. c2c4 -> 6132120 (109 ms)
39. c2c5 -> 6207610 (109 ms)
40. c2c6 -> 3946799 (68 ms)
41. c2c7 -> 4947973 (89 ms)
42. f2d2 -> 3755143 (67 ms)
43. f2e2 -> 3303464 (62 ms)
44. f2g2 -> 3461057 (63 ms)
45. f2f3 -> 3396833 (61 ms)
46. f2f4 -> 6098381 (110 ms)
47. f2f5 -> 6165016 (112 ms)
48. f2f6 -> 3427461 (62 ms)
49. f2f7 -> 4897644 (91 ms)
50. e1d2 -> 3924681 (75 ms)
51. e1e2 -> 3453284 (66 ms)

===========================

Nodes:    222447094
Time(ms): 3972
NPS:      56003800
```

## Play (AI vs AI 1s per move)

```
play 3 1000

 +---+---+---+---+---+---+---+---+
 | a | n | p | q | k | p | n | a | 8
 +---+---+---+---+---+---+---+---+
 | p |   | r |   |   | r |   | p | 7
 +---+---+---+---+---+---+---+---+
 |   | p |   | p | p |   | p |   | 6
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 5
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 4
 +---+---+---+---+---+---+---+---+
 |   | P |   | P | P |   | P |   | 3
 +---+---+---+---+---+---+---+---+
 | P |   | R |   |   | R |   | P | 2
 +---+---+---+---+---+---+---+---+
 | A | N | P | Q | K | P | N | A | 1
 +---+---+---+---+---+---+---+---+
   a   b   c   d   e   f   g   h
> anpqkpna/p1r2r1p/1p1pp1p1/8/8/1P1PP1P1/P1R2R1P/ANPQKPNA w 0 1
info depth 1 nodes 102 time 0 nps 102000 score cp 837 pv a1h8
info depth 2 nodes 799 time 0 nps 799000 score cp 25 pv a1h8
info depth 3 nodes 6265 time 2 nps 3132500 score cp 105 pv h1a8
info depth 4 nodes 18435 time 8 nps 2304375 score cp 34 pv h1a8
info depth 5 nodes 37136 time 13 nps 2856615 score cp 107 pv h1a8
info depth 6 nodes 91841 time 23 nps 3993086 score cp 31 pv h1a8
info depth 7 nodes 229198 time 42 nps 5457095 score cp 50 pv a1h8
info depth 8 nodes 441505 time 79 nps 5588670 score cp 32 pv a1h8
info depth 9 nodes 1007895 time 159 nps 6338962 score cp 40 pv a1h8
info depth 10 nodes 1677117 time 263 nps 6376870 score cp 55 pv a1h8
info depth 11 nodes 3585039 time 522 nps 6867890 score cp 45 pv a1h8
info depth 12 nodes 6984823 time 1000 nps 6984823 score cp 45 pv a1h8
Move: a1h8


...

[Event "Computer Mayhem Variant Game"]
[Site "Paladin 0.2"]
[Date "Thu Mar 31 02:16:06 2022"]
[White "Paladin 0.2"]
[Black "Paladin 0.2"]
[Result "1/2-1/2"]
[TimeControl "0+1000"]
a1h8 a8h1 h8d4 f7f2 e3f2 b8c6 d4b5 a7a6 b5a6 c6d4 c2c7 b6c7
a6b4 c7c5 b4d2 h1c6 g1f3 d8e7 f3d4 c5d4 d2f3 d6d5 c1c2 c6b4
f3d2 b4c5 d2f3 c5b4 f3d2 b4c5 d1f3 g8f6 d2g5 c5b4 e1e2 e6e5
a2a3 b4d6 c2c4 d6b7 c4d5 h7h6 g5h6 b7d5 h6g5 d5f3 g5f3 e7f7
b1d2 f6d5 a3a4 f7b7 b3b4 b7d7 b4b5 d5c3 e2e1 e8f7 d2e4 c3e4
f3e4 f7g7 e1e2 d7g4 e4f3 g4d7 h2h4 d7e8 g3g4 e8f7 a4a5 f7b3
a5a6 b3a2 f3d2 f8f7 e2e1 a2a1 e1e2 a1a2 f2f3 g7f6 e2e1 a2a1
e1f2 a1b2 g4g5 f6g7 f2e1 b2a1 e1e2 a1a2 f3f4 e5f4 g5f4 g7f6
e2e1 a2a1 e1f2 a1b2 f2e2 b2a2 b5b6 a2a6 d2b3 a6a8 b3d4 f6e7
f4f5 a8a2 e2e3 a2h2 f5f6 e7f8 d4c5 f8e8 f1f2 h2h3 e3d4 h3g4
c5e4 g4h4 d4d5 e8d8 d5c6 h4f4 c6d5 f4h4 d5c5 d8d7 f2f3 h4h5
c5c4 h5h2 e4c5 d7d8 c5d4 h2d6 f3f4 c8c7 b6b7 d6f4 c4d5 f4d6
d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6
d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6
d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6
d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6
d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6
d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6
d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6
d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4d5 f4d6 d5c4 d6f4 c4c3 f4c1
c3b3 c1d1 b3c4 { Draw } 1/2-1/2
```

## Monte Carlo analysis

```
monte 20000
Finished: 5%
93 - 86 - 821 [0.5035] 1000

Finished: 10%
191 - 167 - 1642 [0.506] 2000

Finished: 15%
283 - 252 - 2465 [0.505167] 3000

...

Finished: 90%
1691 - 1646 - 14663 [0.50125] 18000

Finished: 95%
1794 - 1745 - 15461 [0.501289] 19000

Finished: 100%
1881 - 1842 - 16277 [0.500975] 20000

===========================

100% / 5683gps / 3519ms
1881 - 1842 - 16277 [0.500975] 20000

```

## Paladin help

```
help
perft [d?] [fen?]       Run Perft
bench [d?] [s?] [h?]    Run Bench
p [fen?]                Show ASCII art board
u64 [bb]                Show ASCII art u64
version                 Show version
flip                    Flip the board
quit                    Quit program
info                    Show program information
eval                    Show evaluation
show                    Show history
clear                   Clear history
add [fen?]              Push position to history
pop                     Pop history
next                    Next history
prev                    Prev history
move [str]              Make a move
analyze [fen?]          Analyze a position (Write 'stop' to stop)
fen [fen]               Set [fen]
level [num]             Set AI level (0 -> 100)
                        0        : Random mover
                        1 -> 100 : Levels 
monte [N] [fen?]        MonteCarlo analysis
                        [N]   : Run for [N] rounds
                        [fen] : Set [fen]
play [mode] [time]      Play a game
                        [mode = 0] : Human vs Human
                        [mode = 1] : Human vs AI
                        [mode = 2] : AI vs Human
                        [mode = 3] : AI vs AI
                        [time]     : Time for AI in ms
```

## License

Only binary is released.
