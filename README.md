## TO BE DONE
* Grin vanity slatepack address generator
* Directly start from random seed, not mnemonic for better performance
* Thee optional X-args, begin'= 'string, end = 'string' contains = ['m','i','m','b','l','e','w','i','m','b','l','e']
  * Use default None as boolean to skipp check, searching for substring is likely to slow down search compared to begin and end string
* Optionally use two step script to create easy parillization using gnu-parallel

## Example use

## Benchmark results

## Testing
* Double check by going from seed-phrase to seed and back (rounway conversion) to avoid any loss of funds.
* Compare performance and add reference to Rust vainity address generator from Makis
* https://github.com/MakisChristou/grin-vanity
* Seed part is fast, 6.6 million valid seeds per second
* Bottleneck appears to be curve25519 Public Key generation (8/second)
  * Check out https://github.com/dalek-cryptography/curve25519-dalek for optional outsourcing that part
  * => Solution appears to be outsourcing to https://github.com/niurenyige/ed25519-dalek-blake3, which can do it in batch, small malability of 8 bytes, should be fine
