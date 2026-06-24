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

**aRVern** is a small, configurable RV32 RISC-V core and the surrounding IP and
reference designs needed to turn it into a working chip. Everything is written
in portable **Verilog-2001**, connects over **AHB-Lite**, and is released under
the permissive **BSD 3-Clause** license — drop it into your fabric without
proprietary IP or tool lock-in.

The ecosystem is split into three repositories, from the core outward to a
full SoC:

## Repositories

| Repository | What it is |
|------------|------------|
| 🧠 **[arvern](https://github.com/Arvern-Silicon/arvern)** | The CPU core — a single-issue, in-order, 4-stage **RV32I[E]MBC** RISC-V processor. Optional M / B / C extensions, S+U privilege modes, Smrnmi NMI, counters, and two AHB-Lite masters. Configurable for area, frequency, or IPC. |
| 🧩 **[arvern-ips](https://github.com/Arvern-Silicon/arvern-ips)** | The IP library — reusable AHB-Lite building blocks: a multi-manager interconnect fabric, ROM / SRAM controllers, ACLINT timer and PLIC interrupt controller, a custom-CSR peripheral, and an example peripheral template. |
| 🔌 **[arvern-soc](https://github.com/Arvern-Silicon/arvern-soc)** | The reference SoCs — worked examples that wire the core and IPs together: an ASIC chip example (synthesis flow included) and an FPGA target for the Terasic **DE0-Nano-SoC** board. |

## Where to start

- **New here?** Read the [**arvern**](https://github.com/Arvern-Silicon/arvern) core README for the ISA, CSR inventory, and configuration options.
- **Building a system?** Grab the blocks you need from [**arvern-ips**](https://github.com/Arvern-Silicon/arvern-ips).
- **Want a full working example?** See [**arvern-soc**](https://github.com/Arvern-Silicon/arvern-soc) for end-to-end ASIC and FPGA integrations.

## License

All repositories are licensed under the **BSD 3-Clause** license.
