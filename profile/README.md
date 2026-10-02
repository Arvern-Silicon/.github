<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)"
            srcset="https://raw.githubusercontent.com/Arvern-Silicon/arvern/main/doc/img/aRVern_dark_title.png">
    <img src="https://raw.githubusercontent.com/Arvern-Silicon/arvern/main/doc/img/aRVern_light_title.png"
         alt="aRVern" width="460">
  </picture>
</p>

<p align="center">
  <strong>Production-grade RISC-V. Plain Verilog. Zero bloat.</strong><br>
  An open-source RISC-V processor core and a complete SoC ecosystem engineered with decades of commercial silicon experience.
</p>

---

## What is aRVern?

**aRVern** is a highly configurable RV32 RISC-V core and an independent IP ecosystem built for IoT and microcontroller-class applications. Written entirely in clean, portable **Verilog-2001** and built on a standard **AHB-Lite** fabric, it delivers commercial-grade quality under a permissive **BSD 3-Clause** license.

No proprietary generators, no high-level synthesis wrappers, and no vendor lock-in. Just rock-solid RTL designed by industry veterans who know what it takes to bring a design to mass production.

The ecosystem is partitioned into four modular repositories:

## Repositories

| Repository | Focus | Description |
|------------|-------|-------------|
| 🧠 **[arvern](https://github.com/Arvern-Silicon/arvern)** | **CPU Core** | A single-issue, in-order, 4-stage **RV32I[E]MBC** RISC-V processor. Features optional M/B/C extensions, S+U privilege modes, PMP with Smepmp, Smrnmi resumable NMI, double-trap handling, hardware counters, **RISC-V Debug 1.0** external debug with Sdtrig triggers, and dual AHB-Lite manager interfaces. Highly parameterized to let designers dial in their perfect sweet spot between silicon area, frequency, and IPC. |
| 🧩 **[arvern-ips](https://github.com/Arvern-Silicon/arvern-ips)** | **IP Library** | Reusable AHB-Lite building blocks: a multi-manager interconnect fabric, ROM/SRAM controllers, ACLINT timer, PLIC interrupt controller, a custom-CSR peripheral, a reusable peripheral template, and the debug transport modules (**JTAG, cJTAG, UART and I2C**) that connect a host to the core's Debug Module. |
| 🔌 **[arvern-soc](https://github.com/Arvern-Silicon/arvern-soc)** | **Reference SoCs** | End-to-end integration examples: an ASIC chip example for synthesis and implementation trials, and a working FPGA system for the Terasic **DE0-Nano-SoC** board with firmware, external debug over any of the four transports, and prebuilt bitstreams. |
| 🛠️ **[arvern-tools](https://github.com/Arvern-Silicon/arvern-tools)** | **Host Tools** | Python host-side debug tools for Windows, Linux and macOS: a firmware loader, a command-line debugger, a GDB server for GDB, CLion or VS Code, and a GUI. They drive the UART, I2C and JTAG debug links over ordinary USB adapters. |

## Where to start

- **Exploring the architecture?** Read the [**arvern**](https://github.com/Arvern-Silicon/arvern) core README for the ISA specs, CSR inventory, and performance configuration options.
- **Building a custom system?** Grab the modular building blocks you need from [**arvern-ips**](https://github.com/Arvern-Silicon/arvern-ips).
- **Want to see it run?** Check out [**arvern-soc**](https://github.com/Arvern-Silicon/arvern-soc) for the DE0-Nano-SoC FPGA system and the ASIC synthesis example.
- **Debugging firmware?** Connect to the core with OpenOCD or a J-Link, or with [**arvern-tools**](https://github.com/Arvern-Silicon/arvern-tools) over UART, I2C or JTAG.

## Verification

- **100 % line, branch and toggle code coverage** of the core and of every IP with its own simulation flow (the shared primitives are exercised through the IPs that use them), with every exclusion argued in the repositories.
- Passes the official **RISC-V Architectural Certification Tests** on every reference configuration of the core.
- Directed regressions across timing variants and dozens of RTL configurations, with clean Verilator and VC Static lint.

## Latest releases

What changed, and how to upgrade from the preview: the release notes of the [core](https://github.com/Arvern-Silicon/arvern/blob/main/CHANGELOG.md), [IPs](https://github.com/Arvern-Silicon/arvern-ips/blob/main/CHANGELOG.md), [SoC examples](https://github.com/Arvern-Silicon/arvern-soc/blob/main/CHANGELOG.md) and [tools](https://github.com/Arvern-Silicon/arvern-tools/blob/main/CHANGELOG.md).

## License

All repositories in the Arvern Silicon ecosystem are licensed under the **BSD 3-Clause** license.