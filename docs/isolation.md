# 🌀 2. Isolation Routing (FlatCAM)

## Step-by-step:
1. **Load Gerber File**: Load the Bottom Copper layer (`.gbr`) into FlatCAM.
2. **Isolation Routing Tool**:
   - Select `Tool Type`: `V` or `C` depending on your bit (Choose 'C' to specify cut depth even with v-bit
   - Tool Diameter: `0.1 mm` (for V-bit) or `0.2–0.3 mm` (flat-end)
   - Number of passes: `1–2` (recommended if trace clearance < 0.3 mm)
   - Pass overlap: `30–50%`

3. **Set Tool Parameters**:
   - Feed rate (x, y) : `200 mm/min`
   - Feed rate (z) : `60 mm/min`
   - Spindle speed: `10000 RPM`
   - Cut Z: `-0.25 to -0.3 mm` (for reliable isolation)
   - Travel Z: `3 mm`
   - Dwell: `0.5 s` (optional for precision)

4. **Generate and Save G-code**:
   - Name it clearly: e.g., `isolation_83x69.nc`
