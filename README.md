# asic-bitcoin-miner
How to build an ASIC SHA-256 miner

##Nand to Tetris (nand2tetris.org)
Quite a few years ago, I heard about this project.  I've always wanted to complete the sylabus, but without a good goal, I find it hard to stay motivated.  Inspired by "Mining bitcoin the hardway" blog post, I decided to give this project a revisit and try and build a bitcoin mining chip.

##Build SHA-256 on a chip.
After reading chapters 1-4, the first requirement I need to build, is a way to hold the SHA-256 constants in the algorithm http://en.wikipedia.org/wiki/SHA-2.

(first 32 bits of the fractional parts of the square roots of the first 8 primes 2..19):
h0 := 0x6a09e667
h1 := 0xbb67ae85
h2 := 0x3c6ef372
h3 := 0xa54ff53a
h4 := 0x510e527f
h5 := 0x9b05688c
h6 := 0x1f83d9ab
h7 := 0x5be0cd19

A series of registers, pre programmed might do the trick.

#First 80bytes
When bitcoin mining, we take the first 80 block bytes, also known as the block header.  The consist of:

###Store 80 bytes

