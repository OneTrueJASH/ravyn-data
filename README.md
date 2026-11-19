# ravyn-data

Data files for [RAVYN](https://github.com/OneTrueJASH/ravyn), kept out of
the engine's source and crate and fetched on demand:

```bash
ravyn fetch-data          # into ~/.ravyn/data (or --data DIR)
```

Each version is a directory, `v<YYYYMMDD>/`, never changed once published;
`SHA256SUMS` lists every file's checksum, and `ravyn fetch-data` installs
nothing that does not match. The engine pins the version it fetches.

| File | What it is |
|---|---|
| `words.fst` | The word list as a finite-state transducer: Crossplay's, the 2023 American tournament list less the words Crossplay removed. The list itself belongs to its owners; it is not licensed by this repository. |
| `crossplay-removed.txt` | The words Crossplay removed from that list. |
| `leaves.rlv` | Leave values trained by RAVYN self-play (MIT, as RAVYN). |

## Versions

- `v20261118`: words.fst (196,419 words), leaves.rlv (921,298 leaves,
  three generations of 500,000 self-play games), crossplay-removed.txt.

RAVYN is an independent project, not affiliated with Crossplay or Scrabble.
