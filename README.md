# asic-bitcoin-miner
How to build an ASIC SHA-256 miner

#Using the Nand to Tetris (nand2tetris.org)

##Build SHA-256 on a chip.
SHA 256 uses some 32bit constants in the algorithm http://en.wikipedia.org/wiki/SHA-2.  We will need to store these on a memory chip.

(first 32 bits of the fractional parts of the square roots of the first 8 primes 2..19):
h0 := 0x6a09e667
h1 := 0xbb67ae85
h2 := 0x3c6ef372
h3 := 0xa54ff53a
h4 := 0x510e527f
h5 := 0x9b05688c
h6 := 0x1f83d9ab
h7 := 0x5be0cd19



#First 80bytes
When bitcoin mining, we take the first 80 block bytes, also known as the block header.  The consist of:

###Store 80 bytes

