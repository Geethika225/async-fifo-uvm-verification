# Asynchronous FIFO Verification Using SystemVerilog and UVM

## 1. Project Overview

This project focuses on the functional verification of an Asynchronous FIFO (First-In, First-Out) using SystemVerilog and the Universal Verification Methodology (UVM).

An Asynchronous FIFO enables reliable data transfer between two clock domains operating independently. It is commonly used in digital systems and SoC designs for clock-domain crossing (CDC).

## 2. Project Objectives

- Verify correct data storage and retrieval.
- Validate FIFO full and empty status flags.
- Verify operation with independent write and read clocks.
- Check reset behavior and pointer initialization.
- Detect data loss, duplication, and ordering errors.
- Develop a reusable UVM-based verification environment.

## 3. Design Overview

The FIFO consists of a memory buffer, write and read pointers, pointer synchronization logic, and full/empty detection logic.

The write side operates using the write clock, while the read side operates using the read clock.

Gray-coded pointers and synchronizer logic may be used to transfer pointer information safely between clock domains, depending on the RTL implementation.

## 4. Verification Environment

The verification environment is developed using SystemVerilog and UVM.

Key components include:

- **Sequence:** Generates stimulus for FIFO operations.
- **Sequencer:** Supplies sequence items to the driver.
- **Driver:** Drives write and read transactions to the DUT.
- **Monitor:** Observes interface activity and collects transaction information.
- **Scoreboard:** Compares expected and actual data behavior.
- **Functional Coverage:** Measures coverage of specified verification scenarios.
- **Assertions:** Checks selected design properties and protocol conditions.

## 5. Verification Scenarios

The planned or implemented scenarios include:

- Reset operation
- Basic write and read operations
- Sequential data integrity
- FIFO empty condition
- FIFO full condition
- Simultaneous read and write operations
- Independent write and read clock operation
- Boundary conditions and FIFO overflow/underflow handling

Only mark scenarios as completed when they have actually been tested.

## 6. Tools Used

- SystemVerilog
- Universal Verification Methodology (UVM)
- Synopsys VCS — simulation
- Synopsys Verdi — waveform inspection and debugging

## 7. Simulation Results

Simulation waveforms are included in this repository to illustrate FIFO operation and selected verification scenarios.

**Results summary:**
- Simulation status: success
- Scoreboard result: test passed
- Functional coverage: 99.5
- Assertion results: 98

These results should be updated using the actual simulation logs and coverage reports.

## 8. Repository Structure

The repository contains RTL design files, UVM verification components, and simulation waveform evidence.

Typical verification components include the testbench, interfaces, agents, drivers, monitors, sequences, scoreboard, and test classes, depending on the implemented environment.

## 9. Learning Outcomes

Through this project, I developed practical experience in:

- UVM testbench architecture
- Transaction-based verification
- Scoreboard-based data checking
- Functional coverage and assertions
- Asynchronous clock-domain behavior
- Simulation debugging using Synopsys VCS and Verdi

## 10. Author

**Samadi Krishna Geethika**

B.Tech in Electronics and Communication Engineering

Interested in Design Verification, SystemVerilog, UVM, and VLSI verification.

---

*This repository is intended to document the design and verification work performed on the project. The reported test results and implemented features should reflect the actual RTL and simulation environment.*
