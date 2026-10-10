# PhysicsofTime.jl

A Julia project for studying the physics of time.

## Layout

```text
PhysicsofTime.jl/
├── Project.toml           # Package metadata, dependencies, and compatibility
├── Manifest.toml          # Exact dependency versions for the shared environment
├── src/
│   └── PhysicsofTime.jl    # Package module and public API
├── test/
│   └── runtests.jl        # Test entry point
├── notebooks/            # Pluto notebooks and exploratory work
└── Physics_of_Time_100_Stage_Student_Guide.pdf
```

## Setup

Run these commands from the repository root. The existing `Manifest.toml` was
generated with Julia 1.13.1; use that version to reproduce the environment.

```sh
julia --project=. -e 'using Pkg; Pkg.instantiate()'
julia --project=.
```

Load the package in the Julia REPL:

```julia
using PhysicsofTime
```

Put reusable code in `src/` and include it from `src/PhysicsofTime.jl`. The package
starts with an empty module, ready for models and calculations.

## Tests

```sh
julia --project=. -e 'using Pkg; Pkg.test()'
```

The test entry point loads the package and provides a test set for future API
tests. No physics functionality or assertions have been added yet.

## Notebooks

```sh
julia --project=. -e 'using Pluto; Pluto.run()'
```

Save notebooks in `notebooks/`. See [the notebook instructions](notebooks/README.md)
for loading the local package from Pluto.
