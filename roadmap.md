# Roadmap — Unified Engineering Workbench

Submission brief: 15-day internship assignment, 100-point rubric (parsed from uploaded PDF).
Deliverable decision: real C++17 core + tests delivered as source; this Lovable web app is the interface
(web preview mirrors the C++ numerics; packaged app will run the C++ core).

## Tasks

- [ ] **Task C — Thermal FEA core (C++ + UI)** — IN PROGRESS
  - [x] C++ solver: assembly, BCs, exact solution, midpoint errors, convergence (`cpp/`)
  - [x] C++ tests pass in sandbox
  - [x] Web UI: Thermal Analysis view (params, validation, profile + convergence plots, CSV export)
  - [ ] Unit chart (°C) + assumptions write-up in report docs
- [ ] **Task A — Interface/backend integration + one-click delivery**
  - [ ] Web views wiring; error/status/cancel handling patterns
  - [ ] Windows packaging (Launch.exe) — must be built on Windows; provide CMake + instructions
  - [ ] Editor run configuration (VS Code tasks/launch)
- [ ] **Task B — STL + ANSYS CSV visualization**
  - [ ] C++ ASCII STL parser + CSV nodal-temperature parser (validation, limits)
  - [ ] Example data files with provenance notes (synthetic CSV labelled)
  - [ ] 3D viewer (WebGL) with rotate/pan/zoom/fit, legend, node inspection
- [ ] **Task D — Multicore batch solves**
  - [ ] Serial + thread-pool parallel batch solve in C++ (deterministic order)
  - [ ] Fixed-seed batch generator, timing harness (1/2/4 workers, 5 reps, median)
  - [ ] Agreement check <= 1e-8 C; Performance view UI
- [ ] **Task E — Embedded integration design + mocks**
  - [ ] Block diagram + interface/voltage table (docs)
  - [ ] C++ mock adapters (discovery, capabilities, connect/disconnect, telemetry, timeout recovery)
  - [ ] Hardware view UI, clearly labelled simulated
- [ ] **Task F — Handwritten backprop**
  - [ ] Handwritten derivation (user must do this themselves — coach, don't substitute)
  - [ ] C++ backprop + central-difference gradient check (eps 1e-6, tol 1e-5), loss plot over 100 steps
- [ ] **Evidence & packaging**
  - [ ] Sample data with provenance, results/ CSVs + plots, docs/ report (<= 6 pages), README
  - [ ] AI-use log, ownership statement, commit history
  - [ ] Final ZIP: CandidateID_Workbench.zip (staged in /tmp, delivered to Files)

## Notes

- C++ compile check: `g++ -std=c++17 -O2 -Icpp/src ...` (no cmake in sandbox; CMakeLists provided for the real build).
- The web app runs only TS; it mirrors the C++ algorithms and both sides are tested to agree.
