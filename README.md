# CRC32-Parallel-FPGA
256-bit parallel CRC-32 hardware accelerator with Castagnoli polynomial (Verilog implementation)
# CRC32-Parallel-FPGA

256-bit parallel CRC-32 (Castagnoli polynomial 0x1EDC6F41) hardware accelerator implementation.

## Features
- **Data Width**: 256-bit parallel input
- **Polynomial**: Castagnoli (0x1EDC6F41) - used in iSCSI, SCTP, etc.
- **Implementation**: Pure combinational logic with single-clock latency
- **Verification**: Matlab modeling + Python golden reference + Verilog simulation

## Algorithm
Derived parallel CRC calculation from serial LFSR using matrix method.
- Matlab used for algorithm validation and coefficient generation
- Python script for cross-verification

## Simulation Results
**Status**: ✅ Functional simulation passed (ModelSim/Vivado Simulator)
- Test vectors: [to be continued]
- Match rate: 100% against Python reference
- Clock frequency target: [yet to confirm]

## Usage
### 1. RTL Simulation
```bash
# Using Vivado
vivado -mode batch -source run_sim.tcl
# Or open Vivado GUI and add rtl/crc32_parallel.v + sim/tb_crc32.v
