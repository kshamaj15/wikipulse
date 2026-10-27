# WikiPulse

WikiPulse explores unusual changes in Wikipedia editing activity using live edits,
historical activity, and article context. The project will grow from a small local
Python pipeline into a streaming data engineering system.

## Current milestone: Week 1, Step 1

The workspace and Python environment are ready for development. Event collection,
cleaning, and analysis will be added in subsequent steps.

## Set up the environment

You need Python 3 with the `venv` module. From the project root, create and activate
an isolated environment:

```sh
python3 -m venv .venv
source .venv/bin/activate
python --version
```

The environment is already created in this checkout. On future visits, only run
the activation command. No third-party dependencies are needed for Step 1.
Dependencies for later stages will be recorded when they are introduced.

## Run the first script

With the environment active, run:

```sh
python src/hello_wikipulse.py
```

Expected output:

```text
WikiPulse development environment is ready.
Next: inspect a small sample of Wikipedia edit events.
```

Alternatively, run without activation:

```sh
.venv/bin/python src/hello_wikipulse.py
```

Run `deactivate` when you finish working in the environment.

## Project structure

```text
src/           Python scripts for the pipeline
tests/         Correctness checks and small test fixtures
data/raw/      Original captured events (ignored by Git)
data/clean/    Normalized records (ignored by Git)
notes/         Learning observations and development decisions
docs/          Existing project documentation
```

The `.gitkeep` files preserve empty folders in Git. Keep small, deliberately
constructed test fixtures under `tests/` so they can be versioned; captured data
belongs under `data/`. The virtual environment and local secrets are also ignored.

## Next learning task

Inspect a handful of real edit events and identify their wiki, article title,
event time, revision IDs, page lengths, and bot flag before writing a collector.
