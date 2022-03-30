[!Paladin](https://github.com/SamuraiDangyo/Paladin/blob/master/logo.png)

# Paladin

Linux mayhem chess variant engine.
Started as Mayhem chess960 engine.
100% UCI support as in Mayhem.
Designed to be GUI independent. You only need the binary.

## Mayhem chess variant

[mayhem variant](https://www.chessvariants.com/diffsetup.dir/mayhem.html)

## Demo / Release

v0.1 version of real Paladin is released to the public.

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

## Perft

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

perft
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
info depth 1 nodes 102 time 0 nps 102000 score cp 437 pv a1h8
info depth 2 nodes 799 time 0 nps 799000 score cp -175 pv a1h8
info depth 3 nodes 6249 time 2 nps 3124500 score cp -94 pv h1a8
info depth 4 nodes 18482 time 7 nps 2640285 score cp -165 pv h1a8
info depth 5 nodes 35830 time 13 nps 2756153 score cp -92 pv h1a8
info depth 6 nodes 92118 time 31 nps 2971548 score cp -168 pv h1a8
info depth 7 nodes 230730 time 48 nps 4806875 score cp -149 pv a1h8
info depth 8 nodes 442653 time 81 nps 5464851 score cp -167 pv a1h8
info depth 9 nodes 1019795 time 154 nps 6622045 score cp -160 pv a1h8
info depth 10 nodes 1746911 time 264 nps 6617087 score cp -147 pv a1h8
info depth 11 nodes 3625764 time 493 nps 7354490 score cp -148 pv a1h8
info depth 12 nodes 6780611 time 875 nps 7749269 score cp -115 pv a1h8
info depth 13 nodes 7655090 time 1000 nps 7655090 score cp -115 pv a1h8
Move: a1h8

...

[Event "Computer Mayhem Variant Game"]
[Site "Paladin 0.1"]
[Date "Wed Mar 30 16:47:04 2022"]
[White "Paladin 0.1"]
[Black "Paladin 0.1"]
[Result "0-1"]
[TimeControl "0+1000"]
a1h8 a8h1 h8d4 e6e5 d4b5 b8c6 f2f7 e8f7 g1f3 c6b4 c2c7 b6c7 b5c3 b4d3 e1e2 d3c5 f1f2 h1g2
c3d5 f7g7 d5c6 g8f6 b1c3 f8f7 g3g4 f6g4 d1g1 g4e3 f2e3 g2h3 g1g3 h3f5 b3b4 c5d7 c6d8 f5g3
h2g3 c7d8 e3e4 a7a6 a2a4 c8c7 f3d2 c7c6 d2c4 d7f8 c4a5 d8d7 e2d3 f8e6 a5c4 f7f5 c4b6 f5e4
d3e4 e6g5 e4d3 d6d5 a4a5 d7d6 b6a4 g5f3 c3d1 g6g5 d1f2 h7h5 a4b6 g5g4 c1c2 f3e1 d3d2 e1f3
d2d3 g7g6 c2c3 g6g5 f2d1 h5h4 g3h4 f3h4 b6a4 g4g3 d3e3 g5g4 e3e2 g4h3 d1f2 g3f2 e2f2 h4f5
a4b6 e5e4 f2e2 h3g4 b6a4 g4f4 a4b6 e4e3 b6c8 c6c5 c8a7 c5c4 a7c8 d5d4 c3d4 f5d4 e2d1 f4e4
d1e1 e4d3 e1f1 e3e2 f1f2 d3d2 f2g2 e2e1q c8d6 e1h4 d6c4 d2e2 c4e5 d4f3 e5f3 h4f2 g2h3 e2f3
b4b5 f2g3 { Black wins } 0-1
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
p                       Show ASCII art board
u64 [bb]                Show ASCII art u64
version                 Show version
quit                    Quit program
info                    Show program information
show                    Show history
clear                   Clear history
add [fen?]              Push position to history
pop                     Pop history
next                    Next history
prev                    Prev history
move [str]              Make a move
analyze [fen?]          Analyze a position (Write 'stop' to stop)
fen [fen]               Use [fen]
level [num]             Set AI level (0 -> 100)
                        0        : Random mover
                        1 -> 100 : Levels
monte [N] [fen]         MonteCarlo analysis
                        [N]   : Run for [N] rounds
                        [fen] : Fen
play [mode] [time]      Play a game
                        [mode = 0] : Human vs Human
                        [mode = 1] : Human vs AI
                        [mode = 2] : AI vs Human
                        [mode = 3] : AI vs AI
                        [time]     : Time for AI in ms
```

## License

Only binary is released.
