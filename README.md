# punxa
Python-based RISC-V Full System Simulator.

Punxa provides HDL models of different parts of a full RISC-V system designed in different design styles using py4hw.

For the processor, we currently support two 64-bit models :

- Behavioral Model of a single-cycle execution processor without pipeline
- Microprogrammed structural design with an algorithmic Control Unit implementation
 

The single-cycle version suppports full system simulation and proxy-kernel simulation (as in Spike).
We also introduce a Linux proxy-kernel to simulate applications compiled with riscv64-unknown-linux-gnu-gcc.

We also support one 32-bit model:

- Behavioral Model of a single-cycle execution processor without pipeline

## Testing

We started focussing on RV64 and Baremetal applications (compiled with risc64-unknown-elf-gcc).
Then, we moved to RV32.
When completed, next goal is Linux boot.

### RISC-V ISA Tests

***RV64*** ISA tests progress: 

<table>
 <tr><td>Version</td><td>Progress</td></tr>
 <tr>
  <td>Single Cycle </td><td>99.7 %   |█████████████████████████████████████████████|</td>
 </tr>
 <tr>
  <td>Microprogrammed </td><td>30.1 %   |██████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░|</td>  
 </tr>
</table>


***RV32*** ISA tests progress:

<table>
<tr><td>Version</td><td>Progress</td></tr>
<tr>
 <td>Single Cycle </td><td>99.6 %   |█████████████████████████████████████████████|</td>
</tr>
</table>

check [riscv-tests](https://github.com/davidcastells/punxa/blob/main/test/riscv-tests/README.md) for a complete list

### Proxy-kernel Apps

- [Hello World](https://github.com/davidcastells/punxa/blob/main/test/proxykernel_software/hello/README.md)
- [Mandelbrot](https://github.com/davidcastells/punxa/blob/main/test/proxykernel_software/mandelbrot/README.md)
- [File sort](https://github.com/davidcastells/punxa/tree/main/test/proxykernel_software/sort/README.md)
- [Paranoia](https://github.com/davidcastells/punxa/tree/main/test/proxykernel_software/paranoia/README.md)
