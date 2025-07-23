# ✂️ Cutout Operation (FlatCAM)

## Steps:
1. Select **Board Outline** layer
2. Use **Cutout Tool**:
   - Tool: `1/8" flat end mill` (`3.175 mm`)
   - Cut Depth: `-1.55 mm` (or full board thickness + margin)
   - Pass Depth: `0.5 mm`
   - Feedrate: `300 mm/min`
   - Spindle: `10000 RPM`

3. Save G-code as `cutout.nc`
