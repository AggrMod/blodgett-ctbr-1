# Blodgett CTBR-1 — interactive 3D model, wiring and test bench

**Live:** https://aggrmod.github.io/blodgett-ctbr-1/

An interactive 3D model of the **Blodgett CTBR-1** countertop electric convection oven (9.0 kW, 208–220 V, 3-phase) on its pedestal stand, built for commercial kitchen technicians. It runs in any browser — phone or desktop — with nothing to install.

Everything you see is driven by a **live circuit solver** running on the oven's actual control wiring, traced point-to-point from Blodgett print **RB&CD 7404** (the schematic sticker inside the control compartment). Flip a switch and every wire, reading and indicator updates from the math, not from a script.

## What it does

- **Orbit, zoom, open things.** Drag to orbit, pinch or scroll to zoom. Tap the door or the control panel and they swing open.
- **Operate the oven.** Blower on/off, cool-down Auto/Manual, call for heat. The contactor pulls in only when the wiring says it should. Elements glow with real dissipated power.
- **Show wiring.** X-ray the cabinet and see every conductor with current flow animated along it — print colors or as-built colors.
- **Focus.** Isolate one system (motor, door switches, contactor, fuses, supply, brake capacitor, cool-down switch, thermostat, heaters) and everything wired to it.
- **Data plate.** The nameplate, readable.
- **Motor swap.** A seven-step walkthrough of replacing the blower motor with the current Blodgett service part — **Nidec FIR 2799.2492 (Blodgett 59288)** — including which lead lands where per Blodgett L‑1243, which lead gets capped, and what to expect on the clamp meter afterward.
- **Test bench.** Put a voltmeter across any two terminals, clamp any wire, plant a dead short or a ground fault, open a wire — and watch the 10 A fuses and the branch breaker respond with real inverse-time and instantaneous trip behavior. Choose 240 V delta (high-leg) or 208Y/120 service.
- **Run wiring check.** Twenty-odd automated checks that run the modeled oven through its states and compare against the plate: line currents per leg, element kW, door-interlock behavior, brake-capacitor rating, chassis potential, fault clearing. Includes a self-test that deliberately mis-lands the capacitor leads to prove the checker catches it.

## Why

Because the schematic sticker is 2 inches wide, the print is 40 years old, and the first time you swap a motor with a six-lead electronic-switch replacement you want to see it before you do it. This is a study and teaching aid.

## Run it locally

Open `index.html`. That's it. The only external dependencies are three.js (r128) and two Google fonts, loaded from CDNs.

## Accuracy and safety

This is a model, not the manufacturer's documentation. Geometry is approximate; the electrical network follows print RB&CD 7404 and measured plate values, with component impedances chosen to reproduce nameplate currents. **Always verify against the current Blodgett service manual and the wiring diagram in the unit in front of you. Work de-energized, lock out, and test before touch.** Nothing here is a substitute for a licensed technician's judgment.

Blodgett, Nidec and FIR are trademarks of their respective owners; this project is not affiliated with or endorsed by any of them.

## License

MIT — see [LICENSE](LICENSE). Use it, fork it, fix it, teach with it.

---

*Keywords: Blodgett CTBR-1, CTB-1, convection oven, commercial kitchen equipment repair, wiring diagram RB&CD 7404, blower motor replacement, Nidec FIR 2799.2492, Blodgett 59288, brake capacitor, door interlock, contactor, circuit simulator, three.js, technician training.*
