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

## Bench

```
bench inf 10000
[ 1/6 ; 6k1/7p/2pA1p2/p7/1p4a1/1PKN1p2/P4P2/2P5 w 0 1 ; bm c3c2 ]
info depth 1 nodes 14 time 0 nps 14000 score cp 210 pv d3b4
info depth 2 nodes 296 time 0 nps 296000 score cp 150 pv c3c2
info depth 3 nodes 1118 time 0 nps 1118000 score cp 104 pv c3c2
info depth 4 nodes 1706 time 0 nps 1706000 score cp 125 pv c3c2
info depth 5 nodes 4165 time 0 nps 4165000 score cp 119 pv c3c2
info depth 6 nodes 7010 time 1 nps 7010000 score cp 133 pv c3c2
info depth 7 nodes 20000 time 2 nps 10000000 score cp 95 pv c3c2
info depth 8 nodes 31265 time 3 nps 10421666 score cp 108 pv c3c2
info depth 9 nodes 54960 time 5 nps 10992000 score cp 101 pv c3c2
info depth 10 nodes 105503 time 11 nps 9591181 score cp 146 pv c3c2
info depth 11 nodes 217332 time 22 nps 9878727 score cp 128 pv c3c2
info depth 12 nodes 473444 time 49 nps 9662122 score cp 122 pv c3c2
info depth 13 nodes 1321263 time 130 nps 10163561 score cp 108 pv c3c2
info depth 14 nodes 2799773 time 285 nps 9823764 score cp 113 pv c3c2
info depth 15 nodes 4640824 time 466 nps 9958849 score cp 121 pv c3c2
info depth 16 nodes 9638064 time 996 nps 9676771 score cp 144 pv c3c2
info depth 17 nodes 27481573 time 2723 nps 10092388 score cp 134 pv c3c2
info depth 18 nodes 50782049 time 5133 nps 9893249 score cp 118 pv c3c2
info depth 19 nodes 89798938 time 8913 nps 10075051 score cp 140 pv c3c2
info depth 20 nodes 99923433 time 10000 nps 9992343 score cp 140 pv c3c2

[ 2/6 ; 4k3/8/4Ap2/p1p5/Pp2a3/1P3N1p/4KP2/2P5 w 38 1 ; bm e6h3 ]
info depth 1 nodes 60 time 0 nps 60000 score cp 244 pv e6h3
info depth 2 nodes 415 time 0 nps 415000 score cp 277 pv e6h3
info depth 3 nodes 2319 time 0 nps 2319000 score cp 278 pv e6h3
info depth 4 nodes 4501 time 0 nps 4501000 score cp 302 pv e6h3
info depth 5 nodes 7694 time 0 nps 7694000 score cp 293 pv e6h3
info depth 6 nodes 15136 time 1 nps 15136000 score cp 297 pv e6h3
info depth 7 nodes 34494 time 3 nps 11498000 score cp 299 pv e6h3
info depth 8 nodes 59838 time 6 nps 9973000 score cp 309 pv e6h3
info depth 9 nodes 120679 time 12 nps 10056583 score cp 301 pv e6h3
info depth 10 nodes 234569 time 25 nps 9382760 score cp 301 pv e6h3
info depth 11 nodes 408291 time 42 nps 9721214 score cp 302 pv e6h3
info depth 12 nodes 661989 time 69 nps 9594043 score cp 314 pv e6h3
info depth 13 nodes 1039245 time 107 nps 9712570 score cp 308 pv e6h3
info depth 14 nodes 1683809 time 173 nps 9733000 score cp 310 pv e6h3
info depth 15 nodes 4526402 time 457 nps 9904599 score cp 306 pv e6h3
info depth 16 nodes 7600144 time 760 nps 10000189 score cp 323 pv e6h3
info depth 17 nodes 12994211 time 1295 nps 10034139 score cp 315 pv e6h3
info depth 18 nodes 31522090 time 3200 nps 9850653 score cp 304 pv e6h3
info depth 19 nodes 48745213 time 4985 nps 9778377 score cp 307 pv e6h3
info depth 20 nodes 94978800 time 9934 nps 9560982 score cp 304 pv e6h3
info depth 21 nodes 95468166 time 10000 nps 9546816 score cp 304 pv e6h3

[ 3/6 ; 8/5ak1/8/p1p5/Pp3N2/1P1A1P2/6K1/8 w 6 1 ; bm d3f5 ]
info depth 1 nodes 62 time 0 nps 62000 score cp 402 pv d3c5
info depth 2 nodes 1239 time 0 nps 1239000 score cp 352 pv d3b2
info depth 3 nodes 2915 time 0 nps 2915000 score cp 352 pv d3b2
info depth 4 nodes 4932 time 0 nps 4932000 score cp 368 pv d3b2
info depth 5 nodes 10388 time 1 nps 10388000 score cp 337 pv d3b2
info depth 6 nodes 16075 time 1 nps 16075000 score cp 369 pv d3b2
info depth 7 nodes 70543 time 6 nps 11757166 score cp 332 pv d3b2
info depth 8 nodes 107841 time 10 nps 10784100 score cp 347 pv d3b2
info depth 9 nodes 175839 time 17 nps 10343470 score cp 347 pv d3b2
info depth 10 nodes 333415 time 33 nps 10103484 score cp 347 pv d3b2
info depth 11 nodes 718953 time 68 nps 10572838 score cp 329 pv d3b2
info depth 12 nodes 1984280 time 191 nps 10388900 score cp 333 pv d3f5
info depth 13 nodes 3676678 time 340 nps 10813758 score cp 325 pv d3b2
info depth 14 nodes 5020089 time 465 nps 10795890 score cp 335 pv d3b2
info depth 15 nodes 11358414 time 1043 nps 10890138 score cp 328 pv d3b2
info depth 16 nodes 17533681 time 1624 nps 10796601 score cp 333 pv d3b2
info depth 17 nodes 29488320 time 2647 nps 11140279 score cp 327 pv d3f5
info depth 18 nodes 105673025 time 9842 nps 10736946 score cp 323 pv d3f5
info depth 19 nodes 107656403 time 10000 nps 10765640 score cp 323 pv d3f5

[ 4/6 ; Anp1kpn1/p6p/1pp1p1p1/4N3/3P4/1PN1P3/P4P1P/a1PK1P2 w 0 1 ; bm e5c6 ]
info depth 1 nodes 62 time 0 nps 62000 score cp 300 pv a8c6
info depth 2 nodes 762 time 0 nps 762000 score cp 133 pv e5c6
info depth 3 nodes 4630 time 0 nps 4630000 score cp 140 pv e5c6
info depth 4 nodes 6104 time 1 nps 6104000 score cp 149 pv e5c6
info depth 5 nodes 19968 time 2 nps 9984000 score cp 118 pv e5c6
info depth 6 nodes 33674 time 4 nps 8418500 score cp 128 pv e5c6
info depth 7 nodes 76601 time 9 nps 8511222 score cp 142 pv e5c6
info depth 8 nodes 129375 time 17 nps 7610294 score cp 137 pv e5c6
info depth 9 nodes 235549 time 30 nps 7851633 score cp 137 pv e5c6
info depth 10 nodes 445087 time 57 nps 7808543 score cp 220 pv e5c6
info depth 11 nodes 649455 time 80 nps 8118187 score cp 223 pv e5c6
info depth 12 nodes 981361 time 119 nps 8246731 score cp 223 pv e5c6
info depth 13 nodes 2275796 time 276 nps 8245637 score cp 259 pv e5c6
info depth 14 nodes 12005097 time 1362 nps 8814314 score cp 302 pv e5c6
info depth 15 nodes 20244970 time 2306 nps 8779258 score cp 273 pv e5c6
info depth 16 nodes 39528735 time 4278 nps 9240003 score cp 273 pv e5c6
info depth 17 nodes 59245293 time 6478 nps 9145614 score cp 273 pv e5c6
info depth 18 nodes 82917540 time 9059 nps 9153056 score cp 286 pv e5c6
info depth 19 nodes 91925543 time 10000 nps 9192554 score cp 286 pv e5c6

[ 5/6 ; 8/1K6/8/p4Qp1/q6p/k6P/8/8 w 1 1 ; bm b7a6 ]
info depth 1 nodes 58 time 0 nps 58000 score cp -61 pv f5g5
info depth 2 nodes 604 time 0 nps 604000 score cp -153 pv f5e5
info depth 3 nodes 3035 time 0 nps 3035000 score cp -163 pv b7a6
info depth 4 nodes 5522 time 1 nps 5522000 score cp -141 pv b7a6
info depth 5 nodes 12426 time 1 nps 12426000 score cp -173 pv b7a6
info depth 6 nodes 27031 time 3 nps 9010333 score cp -167 pv b7a6
info depth 7 nodes 46252 time 5 nps 9250400 score cp -167 pv b7a6
info depth 8 nodes 109695 time 11 nps 9972272 score cp -152 pv b7a6
info depth 9 nodes 178968 time 17 nps 10527529 score cp -152 pv b7a6
info depth 10 nodes 372133 time 34 nps 10945088 score cp -143 pv b7a6
info depth 11 nodes 765988 time 70 nps 10942685 score cp -146 pv b7a6
info depth 12 nodes 2226491 time 201 nps 11077069 score cp -137 pv b7a6
info depth 13 nodes 3456384 time 311 nps 11113774 score cp -145 pv b7a6
info depth 14 nodes 5486029 time 489 nps 11218873 score cp -137 pv b7a6
info depth 15 nodes 11541448 time 1019 nps 11326249 score cp -143 pv b7a6
info depth 16 nodes 26868708 time 2393 nps 11228043 score cp -133 pv b7a6
info depth 17 nodes 57396176 time 5059 nps 11345359 score cp -143 pv b7a6
info depth 18 nodes 87590438 time 7695 nps 11382772 score cp -139 pv b7a6
info depth 19 nodes 114019918 time 10000 nps 11401991 score cp -139 pv b7a6

[ 6/6 ; 8/3K4/8/p1pP2p1/Pk5p/7P/8/5P2 w 0 1 ; bm d7c6 ]
info depth 1 nodes 18 time 0 nps 18000 score cp 16 pv d5d6
info depth 2 nodes 99 time 0 nps 99000 score cp -15 pv d7c6
info depth 3 nodes 259 time 0 nps 259000 score cp -15 pv d7c6
info depth 4 nodes 403 time 0 nps 403000 score cp 4 pv d7c6
info depth 5 nodes 664 time 0 nps 664000 score cp 5 pv d7c6
info depth 6 nodes 1111 time 0 nps 1111000 score cp 6 pv d7c6
info depth 7 nodes 2063 time 0 nps 2063000 score cp 1 pv d7c6
info depth 8 nodes 3560 time 0 nps 3560000 score cp -3 pv d7c6
info depth 9 nodes 5064 time 0 nps 5064000 score cp -8 pv d7c6
info depth 10 nodes 7229 time 0 nps 7229000 score cp 0 pv d7c6
info depth 11 nodes 48074 time 3 nps 16024666 score cp -89 pv d7c6
info depth 12 nodes 68414 time 5 nps 13682800 score cp -74 pv d7c6
info depth 13 nodes 91344 time 6 nps 15224000 score cp -88 pv d7c6
info depth 14 nodes 179247 time 12 nps 14937250 score cp -104 pv d7c6
info depth 15 nodes 265641 time 19 nps 13981105 score cp -110 pv d7c6
info depth 16 nodes 699699 time 45 nps 15548866 score cp -110 pv d7c6
info depth 17 nodes 1506218 time 89 nps 16923797 score cp -129 pv d7c6
info depth 18 nodes 2984211 time 183 nps 16307163 score cp -130 pv d7c6
info depth 19 nodes 10420743 time 656 nps 15885278 score cp -133 pv d7c6
info depth 20 nodes 22311931 time 1415 nps 15768149 score cp -129 pv d7c6
info depth 21 nodes 34065485 time 2190 nps 15555015 score cp -143 pv d7c6
info depth 22 nodes 49524595 time 3210 nps 15428222 score cp -131 pv d7c6
info depth 23 nodes 67099332 time 4354 nps 15410962 score cp -140 pv d7c6
info depth 24 nodes 102559367 time 6958 nps 14739776 score cp -170 pv d7c6
info depth 25 nodes 139125862 time 9338 nps 14898892 score cp -122 pv d7c6
info depth 26 nodes 150447908 time 10000 nps 15044790 score cp -122 pv d7c6

===========================

Nodes:    659441371
Time(ms): 60000
NPS:      10990689
quit
Bye!

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
