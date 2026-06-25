<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)"
            srcset="https://raw.githubusercontent.com/Arvern-Silicon/arvern/main/doc/img/aRVern_dark_title.png">
    <img src="https://raw.githubusercontent.com/Arvern-Silicon/arvern/main/doc/img/aRVern_light_title.png"
         alt="aRVern" width="460">
  </picture>
</p>

<p align="center">
  An open-source <strong>RISC-V</strong> processor core and a complete,
  vendor-lock-in-free <strong>SoC ecosystem</strong> in plain Verilog.
</p>

---

## What is aRVern?

**aRVern** is a small, highly configurable RV32 RISC-V core and the surrounding IP fabric needed to turn it into a working silicon or FPGA bitstream. Written entirely in portable **Verilog-2001**, everything connects over standard **AHB-Lite** and is released under the permissive **BSD 3-Clause** license — drop it into your design without proprietary IP or tool lock-in.

The ecosystem is cleanly partitioned into three modular repositories:

## Repositories

| Repository | Focus | Description |
|------------|-------|-------------|
| 🧠 **[arvern](https://github.com/Arvern-Silicon/arvern)** | **CPU Core** | A single-issue, in-order, 4-stage **RV32I[E]MBC** RISC-V processor. Features optional M/B/C extensions, S+U privilege modes, Smrnmi NMI, hardware counters, and dual AHB-Lite manager interfaces. Configurable for area, frequency, or IPC. |
| 🧩 **[arvern-ips](https://github.com/Arvern-Silicon/arvern-ips)** | **IP Library** | Reusable AHB-Lite building blocks: a multi-manager interconnect fabric, ROM/SRAM controllers, ACLINT timer, PLIC interrupt controller, a custom-CSR peripheral, and a reusable peripheral template. |
| 🔌 **[arvern-soc](https://github.com/Arvern-Silicon/arvern-soc)** | **Reference SoCs** | End-to-end integration examples. Includes an ASIC chip example (with complete synthesis flow) and an FPGA target for the Terasic **DE0-Nano-SoC** board. |

## Where to start

- **Exploring the architecture?** Read the [**arvern**](https://github.com/Arvern-Silicon/arvern) core README for the ISA specs, CSR inventory, and performance configuration options.
- **Building a custom system?** Grab the modular building blocks you need from [**arvern-ips**](https://github.com/Arvern-Silicon/arvern-ips).
- **Want to see it run?** Check out [**arvern-soc**](https://github.com/Arvern-Silicon/arvern-soc) for ready-to-use ASIC and FPGA reference designs.

## License

All repositories in the Arvern Silicon ecosystem are licensed under the **BSD 3-Clause** license.