## TO BE DONE
* Grin vanity slatepack address generator
* Directly start from random seed, not mnemonic for better performance
* Thee optional X-args, begin'= 'string, end = 'string' contains = ['m','i','m','b','l','e','w','i','m','b','l','e']
  * Use default None as boolean to skipp check, searching for substring is likely to slow down search compared to begin and end string
* Check if mimble-wimble-py has a .from(seed) function similar to bip_utils library it uses.
* Optionally use two step script to create easy parillization using gnu-parallel

## Example use

## Benchmark results

## Testing
* Double check by going from seed-phrase to seed and back (rounway conversion) to avoid any loss of funds.
* Compare performance and add reference to Rust vainity address generator from Makis
* https://github.com/MakisChristou/grin-vanity
* Just a feeling but I think I can make a faster implementation...we will see.
