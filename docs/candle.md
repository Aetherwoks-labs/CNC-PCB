# Candle CNC Job Execution Workflow

This section outlines how to execute your PCB job in **Candle** after generating G-code in FlatCAM.

---

##  Preparation
1. **Secure the copper board** to your bed using clamps
2. **Clean the board** with isopropyl alcohol
3. **Insert the first bit** (usually V-bit for isolation)
4. Connect your **Z-probe clamp**:
   - Verify continuity (metal clip + copper)
   - Set your (x,y) origin
   - Set probe feedrate: `10–15 mm/min`

---

## Z-Probing
1. In Candle, click on the Z-probe button
2. Set your Z origin
3. Go to the heightmap tab
   - Set Interpolation and probe grid values based on your board size
5. Hit **"Probe"**
6. Save the map once done probing and select **"use height map"** 

> ⚠️ **Important**: Do not re-zero after heightmap probing unless you redo the probe.

---

## Running Jobs
1. Load `isolation.nc`
2. Start spindle manually (if required)
3. Hit **send** and observe closely
4. After isolation, **change to drill bit**
   - Re-zero **Z only** (do not move X/Y)
   - Load `drill.nc`, run
5. Switch to **cutout bit**, re-zero Z
   - Load `cutout.nc`, run

---

## Tips
- Save workspace before shutdown in case of mid-job stop
- Use scrap test boards to verify isolation depth
- Use heightmap for all jobs
- Never zero x, y after initial zeroing 
- Watch for **skips during isolation** — caused by shallow probing or speed

---

🚀 Once complete, clean the board, inspect traces, and test continuity with a multimeter.
