# Updating a TitanMUX to SP-2026.09.2

Everything here is done on the topside screen. You do not need a laptop, a
terminal or a login.

**This update installs Service Pack SP-2026.09.2, containing the following
components**

| Component | Version |
| --- | --- |
| Topside GUI | v26.09.16 |
| Web portal | v26.09.1 |
| CMB / CMB-TS firmware | 3.0.80 |
| CMM firmware | 3.0.23 |
| PIC firmware | 1.14 |

**Before you start**

- **The topside and the subsea bottle must both be powered on and connected to
  each other**, and stay that way. The bottle's boards are updated over that
  link, so anything not powered and talking to the topside is skipped.
- The topside must be connected to a network with internet access (the same
  connection used for normal updates).
- Allow time to finish in one go. Do not switch the topside off part way
  through, and leave the network plugged in.
- You will be asked to power cycle the subsea bottle once during the update,
  and the topside restarts at the end.
- **When the dialog confirms the service pack is installed, power the whole
  system off and back on** - topside and bottle together - before using the
  unit or checking the versions.

---

## Step 1 — Which route does your unit take?

On the topside: **Settings**, and look at the buttons.

| What you see on the Settings screen | Go to |
| --- | --- |
| An **OS Update** button | **Route A** |
| A **System Update** button | **Route B** |

---

## Route A — older units (Settings has an OS Update button)

These units update in two parts: the software first, then the service pack.

1. **Settings → OS Update → Yes.**
2. Wait for **Update successful**, then answer **Yes** to *Reboot now?*
3. When the topside has restarted, **continue with Route B**. The updated
   software has a *System Update* button in place of *OS Update*.

**If OS Update reports a failure, or it says it was successful but the Topside
version on the Versions screen has not changed, stop and contact engineering.**
Do not keep pressing it.

---

## Route B — units with a System Update button

1. **Settings → System Update.**
2. Press **Check for Updates**. It should show
   *Target Service Package: SP-2026.09.2*.
3. Press **Install Selected Pack** and follow the screen.
4. When it asks you to **power cycle the bottle**, do it, then let the update
   finish. The topside restarts on its own.
5. Wait for the dialog confirming the service pack is installed, then **power
   the whole system off and back on**, topside and bottle.
6. Check the result — see *When it has finished* below.

---

## When it has finished

After the full power cycle, check all three:

- **Settings → System Update** shows *Installed Service Package:
  **SP-2026.09.2***.
- **Settings → Firmware/Software Versions** shows Topside **v26.09.16** and
  Web Portal **v26.09.1**.
- The same screen shows CMB and CMB-TS **3.0.80**, CMM **3.0.23**, PIC **1.14**.

If a firmware version is still the old one, power cycle the bottle and run
**Check for Updates** again — the update page will offer whatever is still
outstanding.

---

## If something goes wrong

| What you see | What to do |
| --- | --- |
| *Update Failed* with a network or git message | Check the unit is online, then try once more. If it fails again, contact engineering. |
| The update finished but a board still shows old firmware | Power cycle the bottle, then **Check for Updates** again. |
| *Installed Service Package* still shows the old pack | Open **System Update** once more; it corrects itself. If not, contact engineering. |

If you have to stop part way through, leave the unit powered and contact
engineering rather than starting again.
