# Notebooks

Save Pluto notebooks in this directory as `.jl` files. Keep reusable models and
calculations in `src/`, with their tests in `test/`.

Launch Pluto from the repository root:

```sh
julia --project=. -e 'using Pluto; Pluto.run()'
```

To use the local package in a notebook, put this in a cell:

```julia
begin
    import Pkg
    Pkg.activate(joinpath(@__DIR__, ".."))
    using PhysicsofTime
end
```

Save the notebook here before running that cell so `@__DIR__` points to this
directory. Activating the project makes the notebook use the repository's shared
environment instead of Pluto's per-notebook package environment.
