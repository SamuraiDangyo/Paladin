![Paladin](https://github.com/SamuraiDangyo/Paladin/blob/main/logo.png)

# Paladin

Linux mayhem chess engine. Written in C++17
Started as Mayhem chess960 engine.
Only mayhem chess variant supported.

## Design goals

- Paladin is designed to be GUI independent. Full UCI support as in Mayhem.
- Paladin is lightweight and simple
- OOP / modular design. No globals as in Mayhem
- Robust and small codebase. Paladin is super stable
- Nice internal GUI. You only need the binary

## Link to the variant

[Mayhem Chess variant](https://www.chessvariants.com/diffsetup.dir/mayhem.html)

## Versions

- v0.1: Initial release
- v1.0: Current. First really good version.
  Tons of bug fixes / improvements. Whole codebase is modular and OOP.

## Demo / Release

v0.1 of real Paladin is released to the public.
Paladins are given for free to testers. (Please contact by email).
And sold to public.

## Signatures

```
perft -> 220873071
bench -> 10773562
```

## Mayhem chess startpos

`anpqkpna/p1r2r1p/1p1pp1p1/8/8/1P1PP1P1/P1R2R1P/ANPQKPNA w 0 1`

## Mayhem chess rules

Normal chess rules except ...

- The paladin is archbishop N+B
- The Janus pawns (= pawns) may capture forward and backward
- Castling is not permitted
- En passant captures are not legal
- The Queen is restricted to 4 moves max

## Nice ASCII art board

`> p`

```
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

## Full perft support

`> perft`

```
1. a2a3 -> 4708983 (175 ms)
2. a2a4 -> 4903248 (176 ms)
3. h2h3 -> 4702557 (169 ms)
4. h2h4 -> 4902192 (175 ms)
5. b3b4 -> 5141188 (185 ms)
6. d3d4 -> 4094107 (147 ms)
7. e3e4 -> 3950318 (142 ms)
8. g3g4 -> 4635327 (169 ms)
9. b1d2 -> 4305516 (155 ms)
10. b1a3 -> 4570894 (165 ms)
11. b1c3 -> 3427298 (126 ms)
12. g1e2 -> 3706298 (135 ms)
13. g1f3 -> 3063821 (112 ms)
14. g1h3 -> 4585751 (165 ms)
15. a1b2 -> 5043975 (180 ms)
16. a1c3 -> 4666344 (165 ms)
17. a1d4 -> 5614281 (198 ms)
18. a1e5 -> 5243773 (184 ms)
19. a1f6 -> 291536 (11 ms)
20. a1g7 -> 435566 (15 ms)
21. a1h8 -> 3927224 (139 ms)
22. h1g2 -> 5121856 (183 ms)
23. h1f3 -> 4499997 (160 ms)
24. h1e4 -> 5743586 (201 ms)
25. h1d5 -> 5686627 (199 ms)
26. h1c6 -> 650539 (23 ms)
27. h1b7 -> 5140149 (180 ms)
28. h1a8 -> 4168807 (146 ms)
29. c2b2 -> 3729746 (139 ms)
30. c2d2 -> 4135037 (150 ms)
31. c2e2 -> 3400384 (126 ms)
32. c2c3 -> 3812732 (139 ms)
33. c2c4 -> 6117619 (217 ms)
34. c2c5 -> 6191279 (219 ms)
35. c2c6 -> 3930853 (139 ms)
36. c2c7 -> 4922875 (177 ms)
37. f2d2 -> 3736239 (140 ms)
38. f2e2 -> 3297285 (125 ms)
39. f2g2 -> 3444747 (132 ms)
40. f2f3 -> 3389916 (125 ms)
41. f2f4 -> 6085595 (217 ms)
42. f2f5 -> 6150690 (219 ms)
43. f2f6 -> 3419216 (123 ms)
44. f2f7 -> 4877887 (177 ms)
45. d1d2 -> 4379675 (157 ms)
46. d1e2 -> 4305949 (156 ms)
47. d1f3 -> 4153199 (148 ms)
48. d1g4 -> 6557033 (233 ms)
49. d1h5 -> 6550530 (232 ms)
50. e1d2 -> 3908200 (149 ms)
51. e1e2 -> 3444627 (133 ms)

===========================

Nodes:    220873071
Time(ms): 7952
NPS:      27775788
```

## Perft (2)

`> perft 6 2k5/3pnA2/1p6/p2P4/P5p1/1P3P2/5P2/2P1K2a_w_1_1`

```
1. c1c2 -> 1440569 (64 ms)
2. b3b4 -> 1647910 (66 ms)
3. f3g4 -> 1725711 (66 ms)
4. f3f4 -> 1810289 (71 ms)
5. d5d6 -> 1078242 (43 ms)
6. f7e5 -> 1905425 (77 ms)
7. f7g5 -> 1631733 (64 ms)
8. f7h5 -> 1260144 (50 ms)
9. f7d6 -> 98670 (4 ms)
10. f7e6 -> 1332987 (54 ms)
11. f7g6 -> 1791672 (71 ms)
12. f7h6 -> 1463272 (56 ms)
13. f7d8 -> 729099 (32 ms)
14. f7e8 -> 1050358 (44 ms)
15. f7g8 -> 945079 (37 ms)
16. f7h8 -> 1474279 (56 ms)
17. e1d1 -> 1483881 (60 ms)
18. e1f1 -> 1311623 (52 ms)
19. e1d2 -> 2069975 (83 ms)
20. e1e2 -> 1607556 (64 ms)

===========================

Nodes:    27858474
Time(ms): 1114
NPS:      25007606
```

## Perft (3)

`> perft 6 1npqkpn1/p1r4p/1p1ppap1/8/3A4/1PNPP3/P1R2P1P/2PQKPN1_w_1_1`

```
1. a2a3 -> 71881680 (2666 ms)
2. a2a4 -> 68352956 (2539 ms)
3. f2f3 -> 58550706 (2179 ms)
4. f2f4 -> 77362694 (2848 ms)
5. h2h3 -> 61167666 (2280 ms)
6. h2h4 -> 64539270 (2407 ms)
7. b3b4 -> 71821086 (2661 ms)
8. e3e4 -> 67821030 (2511 ms)
9. g1e2 -> 45662051 (1713 ms)
10. g1f3 -> 55326523 (2073 ms)
11. g1h3 -> 62315198 (2326 ms)
12. c3b1 -> 88240839 (3230 ms)
13. c3e2 -> 60160350 (2224 ms)
14. c3a4 -> 87711701 (3218 ms)
15. c3e4 -> 91630710 (3481 ms)
16. c3b5 -> 82953778 (3135 ms)
17. c3d5 -> 90427686 (3472 ms)
18. d4e2 -> 44236928 (1532 ms)
19. d4f3 -> 71944922 (2540 ms)
20. d4b5 -> 10429958 (408 ms)
21. d4c5 -> 70026075 (2572 ms)
22. d4e5 -> 58823522 (2331 ms)
23. d4f5 -> 81950508 (3026 ms)
24. d4b6 -> 74590431 (2709 ms)
25. d4c6 -> 11228841 (417 ms)
26. d4e6 -> 79196088 (3009 ms)
27. d4f6 -> 3014684 (114 ms)
28. c2b2 -> 80621736 (2961 ms)
29. c2d2 -> 70729966 (2611 ms)
30. c2e2 -> 52051500 (1937 ms)
31. d1d2 -> 56171188 (2082 ms)
32. d1e2 -> 60581200 (2259 ms)
33. d1f3 -> 92737872 (3526 ms)
34. d1g4 -> 103470912 (3910 ms)
35. d1h5 -> 93500363 (3546 ms)
36. e1d2 -> 58163214 (2168 ms)
37. e1e2 -> 43942346 (1649 ms)

===========================

Nodes:    2423338178
Time(ms): 90270
NPS:      26845443
```

## Play or watch games in Paladin

Game: AI vs AI (1000ms + 1000ms)

`> play 3 1000+1000`

```
 +---+---+---+---+---+---+---+---+
 |   |   | p |   |   |   |   |   | 8
 +---+---+---+---+---+---+---+---+
 | p |   | k |   |   | p |   |   | 7
 +---+---+---+---+---+---+---+---+
 | P | p |   |   |   |   | p |   | 6
 +---+---+---+---+---+---+---+---+
 |   | P | n |   | P |   |   |   | 5
 +---+---+---+---+---+---+---+---+
 |   | K | P |   |   | P |   |   | 4
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   | P |   |   | 3
 +---+---+---+---+---+---+---+---+
 |   | q |   |   |   |   |   |   | 2
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 1
 +---+---+---+---+---+---+---+---+
   a   b   c   d   e   f   g   h
> 2p5/p1k2p2/Pp4p1/1Pn1P3/1KP2P2/5P2/1q6/8 w 3 1

[Event "Mayhem chess game"]
[Site  "Paladin 1.0"]
[Date  "Tue Apr  5 13:15:42 2022"]
[Fen   "anpqkpna/p1r2r1p/1p1pp1p1/8/8/1P1PP1P1/P1R2R1P/ANPQKPNA w 0 1"]
[White "Paladin 1.0"]
[Black "Paladin 1.0"]
[Result "0-1"]
[TimeControl "1000+1000"]
a1h8 a8h1 h8d4 f7f2 g3f2 h1d5 b1c3 d5f6 d4e6 c7c3 e6d8 e8d8
b3b4 c3c2 d1c2 g8e7 a2a3 d6d5 b4b5 d8c7 g1e2 b8d7 e2c3 f6g4
e3e4 d5e4 d3e4 g4h2 c2d2 h2e5 d2e3 d7c5 f2f4 e5g7 a3a4 g7e6
c3e2 h7h5 e2d4 e6g4 e3c3 c7b7 e4e5 g4f2 e1e2 e7d5 c3a3 f2e4
c1c2 d5c3 e2e3 c3d5 e3e2 d5c3 e2e3 h5h4 a3c1 h4h3 d4f3 e4f5
e3d2 f5g4 f3h2 g4h2 d2c3 h2f3 a4a5 h3h2 c3b2 h2h1q a5a6 b7c7
c2c4 h1g1 b2a2 g1f2 a2a3 f8f7 a3a2 f3d2 c1d2 f2d2 a2a3 d2c2
f1f2 c2b1 f2f3 b1a1 a3b4 a1b2 { Black wins } 0-1
```

## Monte Carlo analysis

`> monte 30000`

```
Finished: 3.33333%
80 - 90 - 830 [0.495] 1000

...

Finished: 100%
2624 - 2620 - 24756 [0.500067] 30000

===========================

100% / 2897gps / 10355ms
2624 - 2620 - 24756 [0.500067] 30000
```

## Help. All commands

`> help`

```
help                    This help
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
monte [N] [fen?]        Run monte carlo analysis
                        [N]   : Run for [N] rounds
                        [fen] : Set [fen]
play [mode] [time]      Play a game
                        [mode = 0] : Human vs Human
                        [mode = 1] : Human vs AI
                        [mode = 2] : AI vs Human
                        [mode = 3] : AI vs AI
                        [time]     : base + inc
```

## License

Only binary is released
