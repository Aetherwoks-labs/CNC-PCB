# Isolation Routing (FlatCAM)

## General Setup
- Tool Type: V-bit or Flat End Mill
- Tool Diameter: typically 0.1–0.2 mm for V-bit *(choose 'C1' under tooltype to have control over cut depth)*
- Number of passes: 1–2 (test trace clearance)
- Overlap: 30–50%

## Job Creation Steps
1. Load **bottom copper Gerber** (.gbr)
2. Click **"Select"** → Then go to **"Isolation Routing"**
3. Set parameters:
   - Tool dia: `0.1 mm` (V-bit assumed)
   - Passes: `1` for narrow trace spacing
   - Overlap: `0.1` (for closer overlap)
   - Combine: Leave unchecked
4. Click **"Generate Geometry"**
5. Open the newly created geometry
6. Set machining parameters:
   - Cut Z: `-0.25 mm to -0.3 mm`
   - Travel Z: `3 mm`
   - Feedrate X/Y: `200 mm/min`
   - Feedrate Z: `60 mm/min`
   - Spindle speed: `10000 RPM` (or your machine’s default)
   - Dwell: `0.5 s` (optional)
7. Click **"Generate CNC Job"**, then **"Export G-code"**
8. Save as `isolation.nc`

## ⚠️ Notes & Tips
- Always **delete border isolation** (if not, it will remove the copper at origin — you need it to Z-zero with probe.)
- If traces are still connected: increase depth slightly or do a second pass
- If trace clearance < 0.3 mm, always test first
- Run on scrap copper board before committing
- G-code can be simulated in Candle before real cutting

---

✅ You’re now ready to run `isolation.nc` in Candle.

Continue to: [Drilling Process](./drilling.md)
