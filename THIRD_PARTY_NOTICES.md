# Third-party notices

## PKHeX (format documentation only)

The Pokémon Sword/Shield, Legends: Arceus and Scarlet/Violet save container (static XOR pad, salted SHA-256,
block keystream) and the money/bag block layouts were taken as facts from https://github.com/kwsch/PKHeX (GPL-3) to
make the saves readable. No PKHeX code was copied; `src/editors/swish` is an independent implementation.
Item names come from PokeAPI (see below).

## EdiZon save research

The Mario Kart 8 Deluxe (`userdata.dat` header, CRC-32 and stat offsets) and Super Mario Odyssey (16-byte header,
BYML document, item list names) save formats are documented in the "Save research" notes and configs of
https://github.com/WerWolv/EdiZon_CheatsConfigsAndScripts (by Ac_K and contributors). That repository has no licence,
so only the format facts were used; no code was copied. The BYML reader and writer (`src/core/Byml.cpp`) were written
from the format description.

## marcrobledo/savegame-editors

The Breath of the Wild save layout (`src/editors/botw/BotwSave.cpp`), the item table generated into
`src/editors/botw/BotwItems.cpp` and the Super Smash Bros. Ultimate offsets (`src/editors/smash/SmashSave.cpp`) are
ported from https://github.com/marcrobledo/savegame-editors.

```
MIT License

Copyright (c) 2017-2023 Marc Robledo

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

Item names were datamined by MrCheeze (https://github.com/MrCheeze/botw-tools).

## PokeAPI

The Pokémon: Let's Go item names generated into `src/editors/lgpe/LgpeItems.cpp` come from
https://github.com/PokeAPI/pokeapi (`data/v2/csv/item_names.csv` and `item_game_indices.csv`).

```
BSD 3-Clause License

Copyright (c) © 2013–2023 Paul Hallett and PokéAPI contributors

Redistribution and use in source and binary forms, with or without modification, are permitted provided
that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this list of conditions and the
   following disclaimer.
2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and
   the following disclaimer in the documentation and/or other materials provided with the distribution.
3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or
   promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED
WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A
PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY
DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE
OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH
DAMAGE.
```

The Let's Go save layout was reimplemented from the format documented by the PKHeX project and
projectpokemon.org. No PKHeX code is included.

## bcdec

`third_party/bcdec/bcdec.h` (BC1–BC7 texture decoding) is by Sergii Kudlai, https://github.com/iOrange/bcdec,
used under its MIT licence option. The full licence text is in `third_party/bcdec/LICENSE`.

## Formats

Yaz0, BNTX and the Tegra X1 block-linear layout were implemented from public format descriptions
(zeldamods.org, the BNTX tooling community, tegra_swizzle). No code from GPL projects is included.

## Zstandard

`third_party/zstd/` holds the decompression part of Zstandard 1.5.6 (https://github.com/facebook/zstd), used under
its BSD licence. Copyright (c) Meta Platforms, Inc. and affiliates. The full text is in `third_party/zstd/LICENSE`.

## ARM astc-encoder

`third_party/astcenc/` holds the library sources of astc-encoder 4.8.0 (https://github.com/ARM-software/astc-encoder),
built decompression-only, under the Apache License 2.0. Copyright 2011-2024 Arm Limited. The full text is in
`third_party/astcenc/LICENSE.txt`. The files are unmodified.
