# Drilling Process (FlatCAM)

## Drill Tool Setup
- Use FlatCAM to import `.drl` drill file (Excellon format)
- Drill bits: typically `0.8 mm` or `1.0 mm` carbide bits

## Job Creation Steps
1. Load **drill file** (`.drl`)
2. Click **"Select"** → then go to **"Drill Tool"** tab
3. Configure drill parameters:
   - Tool dia: `0.8 mm` or appropriate bit 
  (*There is an option for tool change if you are drilling different sizes*) 
   - Cut Z: `-1.45 mm` (for FR4 board)
   - Travel Z: `3 mm`
   - Feedrate X/Y: `200 mm/min`
   - Feedrate Z: `60 mm/min`
   - Spindle speed: `10000 RPM`
   - Dwell Time: `0.5 s`
4. Click **"Generate CNC Job"**
5. Export G-code as `drill.nc`

## ⚠️ Notes & Tips
- Make sure the drill bit length is long enough for `1.8 mm` depth
- Always test spindle tightness and bit alignment
- Do not forget to re-zero Z after bit change
- Save job and run only **after isolation is complete**

---

🔁 Next step: [Cutout Process](./cutout.md)
