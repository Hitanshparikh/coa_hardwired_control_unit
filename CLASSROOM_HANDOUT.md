# Hardwired Control Unit Simulator
## Classroom Handout (Submission Version)

## Project Title
Hardwired Control Unit Interactive 3D Simulator

## Submitted By
Name: Hitansh Parikh
23CS054
Class/Section: CSE, CSPIT

Date: 06/04/2026
## 1. Project Description
This project is an interactive simulator developed to demonstrate the working of a Hardwired Control Unit in Computer Organization and Architecture. It visualizes instruction execution across fetch, decode, execute, memory, and writeback phases, while showing control signals, ALU behavior, register/memory updates, and datapath activity in real time.

The simulator combines both theoretical and practical learning through step-based execution, equation-driven control logic, assembler support, diagnostics, and guided experiments.

## 2. Main Objectives
- Explain how a hardwired control unit generates control signals.
- Demonstrate phase-wise instruction execution and signal flow.
- Provide hands-on understanding of ALU flags, memory operations, and timing.
- Compare hardwired and microprogrammed control approaches.
- Support lab-style learning with checkpoints and validation.

## 3. Key Features Implemented
- 3D datapath simulation of CU, ALU, Registers, and Memory.
- Real-time control signal monitor with Boolean equation viewer.
- Instruction set execution with cycle-by-cycle phase display.
- Assembler panel with label support and machine-code mapping.
- Validation monitor with diagnostics and golden reference tests.
- Timing analytics including CPI and latency behavior.
- Pipeline mode with hazard detection and forwarding controls.
- Side-by-side hardwired vs microprogrammed comparison.
- Fault injection:
  - Stuck-at register bit fault
  - Delayed memory behavior
  - Clock jitter
- Editable register and memory values while paused.
- Scenario manager to save/load named experiments.
- Guided labs with auto-check progress.
- Visualization controls:
  - Label overlays
  - Active-unit heatmaps
  - Before/after compare overlay
  - Quality presets (low/medium/high)

## 4. Educational Value
This simulator helps students connect textbook concepts with practical execution flow:
- Understand CU state transitions and control orchestration.
- Observe impact of timing, hazards, and memory latency.
- Learn architecture trade-offs through direct comparisons.
- Practice experimentation and verification using labs and diagnostics.

## 5. Tools and Technologies
- HTML, CSS, JavaScript
- Three.js for 3D rendering and visualization
- Browser-based interactive UI (no backend required)

## 6. How to Run
1. Open the project folder.
2. Open `hardwired_cu_simulator.html` in a browser.
3. Select an instruction and click Start Simulation.
4. Use side panels for diagnostics, labs, comparison, and visualization settings.

## 7. Conclusion
The Hardwired Control Unit Simulator successfully provides an interactive learning platform for understanding control-unit design and datapath behavior. It supports both conceptual clarity and practical experimentation, making it suitable for classroom demonstrations, lab activities, and student self-learning.

## 8. File Reference
- Main Simulator: `hardwired_cu_simulator.html`
- Detailed Documentation: `README.md`
- This Handout: `CLASSROOM_HANDOUT.md`
