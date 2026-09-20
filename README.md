# FPGA QEC Stream Processing

## Verified FPGA Detector-Stream Processing with CPU/GPU Global Decoding

Hardware–software co-design research project investigating which deterministic
quantum-error-correction stream operations should execute close to the
quantum controller on FPGA.

### Core pipeline

measurement stream  
→ round tracking  
→ detector generation  
→ parity processing  
→ FIFO buffering  
→ sparse event packing  
→ timestamp / metadata  
→ host transport  
→ CPU/GPU global decoder

### Technical areas

- SystemVerilog
- Verilog
- FPGA architecture
- streaming datapaths
- detector generation
- parity processing
- FIFOs
- backpressure
- sparse-event encoding
- timestamps
- packet framing
- cocotb verification
- Quartus Prime
- synthesis
- timing closure
- C++ host software
- CPU/GPU decoding
- hardware/software co-design

### Initial hardware

Terasic DE0-Nano.

The host transport is deliberately modular so that later FPGA, Ethernet,
PCIe or RFSoC hardware can be introduced without redesigning the research
core.

Measured DE0-Nano performance must remain explicitly separate from any
modelled high-speed transport architecture.
