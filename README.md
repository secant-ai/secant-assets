# secant-assets

Files that Secant's local install downloads once, published as GitHub releases so the download is a call to GitHub
and nothing else. No code lives here.

## embedder-potion-base-32M-1

`potion-base-32M-1e5a03f8.tar.gz` (sha256 `77259e12023055a5b8b1c5f510a1835e5b81fa76cb76abfd951ef1cd4c0b0925`): the
static embedding model `secant init` uses to build a team's store on their own machine (numpy only, no torch).

- Model: [minishlab/potion-base-32M](https://huggingface.co/minishlab/potion-base-32M) at revision
  `1e5a03f8eeb2c98b928fbbd846f22f816360919f`, MIT licence (`LICENSE`).
- Distilled from [BAAI/bge-base-en-v1.5](https://huggingface.co/BAAI/bge-base-en-v1.5), MIT licence
  (`LICENSE.teacher`).
- Contents: `model.safetensors` (the embedding matrix), `tokenizer.json`, `config.json`, the model's `README.md`,
  both licences, and `manifest.json` (model id, upstream revision, sha256 of every file).

Secant pins the archive's sha256 and checks it before extracting.
