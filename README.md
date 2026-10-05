# PandemicAI — HRI 2027 Short Contributions (Code)

This directory contains the working manuscript source. It is not the runnable software supplement required by the Code track.

## Build

Upload the ZIP to Overleaf and select `main.tex`, using pdfLaTeX. With a full local TeX Live installation:

```sh
latexmk -pdf main.tex
```

The original `acmart.cls` and `ACM-Reference-Format.bst` are included. Standard ACM font dependencies include Libertine, Inconsolata, and newtx. The manuscript retains standard margins and type sizes.

## Contents

- `main.tex`: source for the anonymous review PDF, including source-only editorial comments.
- `references.bib`: 24 cited references, including original related work, FurChat, BML, and the two VR theses.
- `figures/platform.png`: original setup and architecture illustration.
- `acmart.cls`, `ACM-Reference-Format.bst`: ACM class and bibliography style.

The supplied PDF has four main-text pages followed by one reference page. Its abstract contains 157 words. Check pagination after edits; `\clearpage` starts references outside the four-page main-text limit, and `\balance` balances the reference columns. The manuscript contains no tables.

The title is model-agnostic. The architecture describes configurable language-model backends; Gemma 3 and GPT-4.1 are named as pilot settings. LLM and RL planning policies are concrete extension routes, not implemented training systems assumed to be included in the release.

The structure is: motivation → related work → platform and reusable interfaces → pilot and lessons → release, reuse and VR prototyping → maintenance and future work → conclusion. The pilot's selected descriptive results do not establish causal architecture differences.

Search for `% RICARDO` in §5.3 for the full-duplex editorial comment. It asks Ricardo to improve or remove that paragraph and verify the replay details; it does not appear in the PDF. The other author-check comment concerns the final TTS participant count.

The review URL is defined once in `\reviewrepository`; confirm it targets the intended code revision and prepare the separate software supplement. Funding text, the change map, the anonymity guidance, and author checks are in the separate author notes, excluded from this package.

The approximately 33-person TTS collection is being prepared as a separate dataset contribution. Full-duplex work concerns offline reuse of recordings and appears under future work. The cited VR theses concern earlier adaptations; Quest Pro/Meta-avatar prototyping and comparison with the physical robot are described separately from validated transfer. The Furhat–Unity toolkit integration is planned, and maintenance commitments describe the continuing repository.
