# Hardwired Control Unit Simulator

Interactive Computer Organization and Architecture simulator with a 3D datapath, equation-driven control logic, assembler workflow, diagnostics, advanced timing, pipeline and architecture comparison, fault injection, labs, and visualization controls.

## 1. What this project is

This simulator helps you learn how a hardwired control unit works across fetch, decode, execute, memory, and writeback phases.

Core capabilities:
- 16-instruction ISA with cycle-stepped execution
- 3D visualization of CU, ALU, registers, and memory
- Real-time control signal activation and equation viewer
- Assembler and machine-code encode/decode workflow
- Validation, diagnostics, golden tests, and report export
- Pipeline/hazard and hardwired-vs-microprogrammed comparison
- Fault injection, scenarios, and guided labs
- Quality presets, label overlays, heatmaps, and compare overlays

## 2. Quick start

### 2.1 Open the simulator
1. Open [hardwired_cu_simulator.html](hardwired_cu_simulator.html) in a modern browser.
2. Wait for the 3D banner to show ready status.
3. If the 3D scene does not appear immediately, switch to another tab and back to 3D Simulator.

### 2.2 Basic run flow
1. In Instruction Set, click an instruction.
2. Click Start Simulation.
3. Watch phase chips, control signals, bus monitor, and 3D animation update.
4. Use Pause Simulation anytime.
5. Use Reset to clear runtime state.

## 3. UI map

- Center area:
  - 3D canvas and HUD
  - Instruction list
  - Assembler panel
  - Execution log
- Right sidebar:
  - Register file
  - Control signals and equation engine
  - ALU and flags
  - Bus monitor
  - ISA overview
  - Timing and CPI metrics
  - Breakpoints and watchpoints
  - Pipeline and hazard panel
  - Hardwired vs microprogrammed side-by-side panel
  - Fault injection panel
  - Scenarios manager
  - Guided labs
  - Visualization controls
  - Validation monitor
- Top nav tabs:
  - 3D Simulator, Architecture, Timing Diagram, Truth Table, Micro-Operations, Theory

## 4. Feature tutorials

## 4.1 Simulation tuning and execution controls

### Goal
Change architectural parameters and rerun execution under new constraints.

### Steps
1. In the tuning panel, set Data Width, Registers, Memory Cells, and Memory Latency.
2. Click Apply Config.
3. Select an instruction and start simulation.
4. Observe ALU/flags and control signals under your selected width and latency.

### Tips
- Smaller data width is useful to visualize overflow and truncation quickly.
- Higher memory latency makes memory phases more visible.

## 4.2 Width-accurate ALU and flags

### Goal
See C, V, Z, and N behavior with arithmetic and logic operations.

### Steps
1. Pick ADD or SUB.
2. Start simulation and run until execute/writeback.
3. Monitor ALU result and flag fields in the sidebar.
4. Repeat with different data width settings.

### What to look for
- Z set when result equals zero
- N based on sign bit in configured width
- C and V set according to addition/subtraction rules

## 4.3 Diagnostics, validation, and golden tests

### Goal
Validate correctness and export evidence.

### Steps
1. Click Golden Tests in Validation Monitor.
2. Review checks/errors counters.
3. Read the trace list for detail.
4. Click Export Report to download JSON diagnostics.

## 4.4 Equation-driven control signals

### Goal
Inspect signal equations and compare expected vs emitted values.

### Steps
1. In Control Signals, click any signal row.
2. Read the equation in Equation Engine.
3. Run simulation and observe Current value updates by phase.
4. Open Truth Table tab to correlate instruction and phase rows.

## 4.5 Assembler and program workflow

### Goal
Write, assemble, import/export, and load programs to memory.

### Steps
1. Enter assembly text in Assembler.
2. Click Assemble.
3. Review diagnostics and encoded outputs.
4. Click Load to Mem.
5. Run simulation.

### Import/export
- Import: click Import and choose a JSON program file.
- Export: click Export to save current source and assembled output.

## 4.6 Timing, breakpoints, and watch behavior

### Goal
Control execution at specific points and study cycle behavior.

### Steps
1. Add a breakpoint address in Breakpoints panel.
2. Start simulation.
3. Execution pauses when breakpoint condition matches.
4. Use step controls to inspect phase-by-phase behavior.

### Timing/CPI
- Review global CPI and instruction-level metrics in the timing panel.
- Export CPI report if available in panel controls.

## 4.7 Pipeline mode and hazard controls

### Goal
Explore hazard behavior with forwarding on/off.

### Steps
1. In Pipeline panel, enable 5-Stage Pipeline.
2. Toggle Data Forwarding.
3. Run simulation.
4. Inspect hazard list and stalled cycles.

### What to compare
- Forwarding enabled usually reduces RAW stall penalties.
- Hazard panel reports detection and pipeline impact.

## 4.8 Hardwired vs microprogrammed comparison

### Goal
Compare cycle overhead and performance gap.

### Steps
1. In the right sidebar, open Hardwired vs Microprogrammed Side-by-Side.
2. Click Run Side-by-Side Compare.
3. Review Hardwired and Microprogrammed cycles and PC values.
4. Inspect Performance Gap section for overhead percentage.

## 4.9 Fault injection

### Goal
Stress runtime behavior with controlled faults.

### Available fault types
- Stuck-at fault on register bit
- Delayed memory timing
- Clock jitter

### Steps
1. Open Fault Injection panel.
2. Enable faults.
3. Inject a stuck-at fault by selecting register, bit, and forced value.
4. Set memory delay and clock jitter as needed.
5. Run simulation and monitor diagnostics/trace.
6. Click Clear All Faults to return to normal mode.

## 4.10 Editable register and memory state while paused

### Goal
Manually craft machine state and observe deterministic effects.

### Steps
1. Pause simulation.
2. Click any register cell in Register File and enter value.
3. Click any memory cell in Memory grid and enter value.
4. Resume execution and inspect ALU, buses, and control signals.

## 4.11 Scenario manager

### Goal
Save and restore named experiments.

### Steps
1. Configure simulator state (registers, memory, flags, config, optional faults).
2. Enter a scenario name.
3. Click Save.
4. Click a saved scenario name to restore it.
5. Delete with the X button when no longer needed.

### Notes
- Restoring a scenario pauses active execution and reapplies saved visual settings.

## 4.12 Guided labs with auto-checks

### Goal
Run structured exercises and get automatic progress checks.

### Steps
1. Open Guided Labs panel.
2. Click Start Lab on a lab card.
3. Follow active lab instructions shown in panel.
4. Run or step simulation.
5. Watch auto-check rows update (passed and pending).
6. Complete all checks to mark lab complete.

## 4.13 3D visualization controls

### Goal
Adjust visual readability and performance.

### Controls
- Labels toggle
- Heatmap toggle for active units
- Compare Overlay toggle
- Quality preset: low, medium, high

### Steps
1. Open Visualization Controls panel.
2. Toggle Labels to show/hide component labels.
3. Toggle Heatmap to color active units by functional role.
4. Change Quality preset depending on GPU budget.
5. Enable Compare Overlay and change config or quality to view before/after snapshot.

## 4.14 Visual compare overlay

### Goal
Track impact of setting changes.

### Steps
1. Enable Compare Overlay.
2. Change simulation config or quality preset.
3. Observe on-canvas overlay showing Before and After values.
4. Use this for teaching trade-offs or documenting tuning decisions.

## 5. Suggested learning paths

## 5.1 Beginner path
1. Run single instruction in 3D simulator.
2. Open Micro-Operations tab and match each phase.
3. Inspect equation engine for 2-3 signals.
4. Run first guided lab.

## 5.2 Intermediate path
1. Assemble a small program with labels.
2. Set breakpoint and step through pipeline mode.
3. Compare hardwired vs microprogrammed mode.
4. Export validation and CPI reports.

## 5.3 Advanced path
1. Inject faults and observe resilience.
2. Save multiple scenarios and replay them.
3. Use compare overlay and quality presets for performance/readability trade-offs.
4. Complete all labs and document outcomes.

## 6. Troubleshooting

## 6.1 3D model not loading
- Reload the page once after edits.
- Ensure script has no syntax error in browser console.
- Verify network access to Three.js CDN resources.

## 6.2 Controls visible but no effect
- Confirm simulation is running for dynamic updates.
- For register/memory editing, ensure simulation is paused.
- For compare overlay, enable toggle and trigger a setting change.

## 6.3 Pipeline or comparison seems empty
- Enable pipeline mode explicitly in panel.
- Click Run Side-by-Side Compare in comparison panel.

## 7. Files in this workspace

- [hardwired_cu_simulator.html](hardwired_cu_simulator.html): full simulator app
- [IMPLEMENTATION_TASKS.md](IMPLEMENTATION_TASKS.md): implementation roadmap and work log
- [README.md](README.md): this documentation

## 8. Contributor notes

When extending the simulator:
- Keep phase semantics consistent with fetch/decode/execute/memory/writeback.
- Update UI panels and state logic together.
- Add validation traces whenever adding new execution behavior.
- Update [IMPLEMENTATION_TASKS.md](IMPLEMENTATION_TASKS.md) and [README.md](README.md) after major feature changes.
