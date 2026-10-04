# Asterion Solver catalogs

Star catalogs indexed for [Asterion Solver](https://github.com/asterion-solver/asterion), a fast blind
astrometric plate solver. They are published in the [releases](https://github.com/asterion-solver/catalogs/releases)
of this repository, and installed by Asterion itself:

```
asterion --download-catalog gaia-500
```

There is no need to download these files by hand: Asterion picks the release which matches the format of
index files it reads (`catalogs-v1`, …), checks the files and decompresses them.

| Catalog     | Content                                                   | Fields of view    |
|-------------|-----------------------------------------------------------|-------------------|
| `tycho2`    | Tycho-2: 2.5 million stars, to magnitude 12               | 0.7° (42′) and up |
| `gaia-500`  | Gaia DR3, the 500 brightest stars of each square degree: 21 million stars | 0.15° (9′) and up |
| `gaia-1000` | Gaia DR3, 1000 stars per square degree: 41 million stars  | 0.15° (9′) and up, sometimes 0.12° (7′) |
| `gaia-2000` | Gaia DR3, 2000 stars per square degree: 83 million stars  | 0.1° (6′) and up  |

See the [README of Asterion](https://github.com/asterion-solver/asterion#which-catalog) to choose one, and
its [developer guide](https://github.com/asterion-solver/asterion/blob/main/DEVELOPERS.md#publishing-catalogs)
for how these files are built and published.

## Files

Each release contains the index files compressed with gzip and split in parts of less than 2 GB
(`<catalog>.astx.gz.000`, `.001`, …), and a manifest, `catalogs.properties`, which lists the size and the
SHA-256 checksum of each part and of each index file.

## Credits and license

- **Gaia DR3** (`gaia-*`): this work has made use of data from the European Space Agency (ESA) mission
  [Gaia](https://www.cosmos.esa.int/gaia), processed by the Gaia Data Processing and Analysis Consortium
  ([DPAC](https://www.cosmos.esa.int/web/gaia/dpac/consortium)). Funding for the DPAC has been provided by
  national institutions, in particular the institutions participating in the Gaia Multilateral Agreement.
  Gaia Collaboration, Vallenari et al. (2023), A&A 674, A1. The indexes derived from Gaia DR3 are distributed
  under the [CC BY-SA 3.0 IGO](https://creativecommons.org/licenses/by-sa/3.0/igo/) license, like Gaia DR3.
- **Tycho-2** (`tycho2`): Høg et al. (2000), A&A 355, L27. This research has made use of the VizieR
  catalogue access tool, [CDS](https://cdsarc.cds.unistra.fr/viz-bin/cat/I/259), Strasbourg, France.
