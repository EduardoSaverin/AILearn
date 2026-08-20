# Paper to Code — Notebooks

Google Colab notebooks for the AI/ML lessons on **[papertocode.dev](https://papertocode.dev)**.

Each notebook pairs a lesson's narrative with runnable code, so you can execute
the ideas on a GPU instead of reading about them.

## Which lessons are here

Only the ones that need a machine your browser cannot provide.

Most lessons on Paper to Code run in-browser via Pyodide — pure Python, numpy,
pandas, scikit-learn. Those need nothing from Colab and are not duplicated here.

A notebook exists when a lesson imports something outside the Pyodide wheel set:
PyTorch, transformers, diffusers, JAX, Whisper, and the rest of the stack that
wants real hardware.

```
phases/
  03-deep-learning-core/
    11-intro-to-pytorch/
      notebook.ipynb
```

## How to run one

Open the Colab link from the lesson page, or from a path here:

```
https://colab.research.google.com/github/EduardoSaverin/papertocode-notebooks/blob/main/phases/<phase>/<lesson>/notebook.ipynb
```

Notebooks that need packages beyond Colab's defaults start with a `pip install`
cell. Run it first.

Some cells expect a GPU runtime — Runtime → Change runtime type → T4.

## What a notebook contains

1. Title, phase, and a link back to the lesson
2. A setup cell, when extra packages are needed
3. The lesson's narrative as markdown, with its code as runnable cells
4. The complete `main.py` from the lesson, as a final reference cell

Code cells are only created for blocks that are genuinely executable. Pseudo-code,
sample output, shell transcripts and configuration snippets stay as displayed
text, so *everything you can run, runs*.

Every code cell is checked with a real Python parser before it ships. A cell that
would raise `NameError` because it references something defined only in the prose
is demoted to a text cell rather than handed to you broken.

## These files are generated

Do not edit notebooks here — changes will be overwritten.

They are produced from the lesson markdown and source files in the
[Paper to Code](https://github.com/EduardoSaverin/PaperToCode) repository and
synced automatically whenever a lesson changes.

Found a mistake? It belongs in the lesson, not the notebook. Open an issue on the
main repository and the fix flows through to here.

## Caveats

Some notebooks reference data files, model weights or gated Hugging Face
repositories that are not included. Where a cell will not run as-is, the
explanation above it says so.

## Licence

See [LICENSE](LICENSE).
