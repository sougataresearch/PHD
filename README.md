# PHD

Umbrella workspace for PhD research projects. Each sub-project is an
independent git repository with its own remote and history, linked here
as a git submodule (or, for IMMSE_SIMU, a plain nested repo not yet
pushed anywhere).

- `IMMSE` — https://github.com/sougataresearch/IMMSE.git
- `gsa_uncertainty_analysis` — https://github.com/sougataresearch/Sensitivity_Analysis.git
- `micro_ellipsometry` — https://github.com/sougataresearch/micro_ellipsometry.git
- `OCD-LIBRARY` — https://github.com/sougataresearch/OCD-LIBRARY.git
- `IMMSE_SIMU` — local only, no remote yet

## Working with submodules

Clone with history:

```
git clone --recurse-submodules https://github.com/sougataresearch/PHD.git
```

Or, after a normal clone:

```
git submodule update --init --recursive
```

Each submodule is developed and pushed from inside its own folder, using
its own remote — commit/push there as usual. From PHD's root, after a
submodule has new commits pushed upstream, update the pointer:

```
cd <submodule>
git pull
cd ..
git add <submodule>
git commit -m "Update <submodule> pointer"
```
