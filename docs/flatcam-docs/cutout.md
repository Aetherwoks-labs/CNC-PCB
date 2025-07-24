# PCB Cutout Process (FlatCAM)

## General Setup
- Tool: Flat End Mill (e.g., `1/8"` or `3.175 mm`)
- Total Depth: `-1.55 mm` (for standard 1.6 mm FR4 with margin)
- Margin: `2 mm` (recommended)

## Job Creation Steps
1. Load **Board Outline** layer (Gerber mechanical or generated from copper layer)
2. Go to **Cutout Tool** tab in FlatCAM
3. Enter parameters:
   - Tool dia: `3.175 mm`
   - Cut Z: `-1.55 mm`
   - Travel Z: `3 mm`
   - Depth per pass: `0.5 mm`
   - Feedrate X/Y: `300 mm/min`
   - Feedrate Z: `60 mm/min`
   - Spindle: `10000 RPM`
   - Margin: `2 mm`
4. Click **"Generate Geometry"** then **"Generate CNC Job"**
5. Export G-code as `cutout.nc`

## ⚠️ Tips
- Use **tabs** (bridges) to hold the board in place — or strong adhesive
- Always check **alignment** before final cut
- **Feedrate values have been tested only with Masuter Pro 4000**

---

🏁 Final step: [Candle Workflow](../candle.md)
