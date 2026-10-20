# torch-mpsradeon-python

A minimal Apple Metal Performance Shaders (MPS) smoke test for macOS with AMD Radeon graphics.

## Tested stack

- Python 3.10
- PyTorch 2.2.2 — the latest PyPI release with a CPython 3.10 macOS x86_64 wheel
- torchvision 0.17.2
- torchaudio 2.2.2

This configuration was tested on an Intel Mac with an AMD Radeon GPU. PyTorch reports MPS availability at runtime and, when available, creates a tensor on `mps:0`. The pinned Torch version is the newest x86_64 macOS build available on PyPI for this Python version.

## Run

```sh
uv sync
uv run torch-mpsradeon-python
```

The command prints an MPS tensor when the backend is available; otherwise it prints `MPS device not found.`