# 📍 Origin Handling in FlatCAM

Correct origin alignment is critical for precise routing, drilling, and cutout. This guide explains how to set up and manage origin positioning in FlatCAM.

---

## What Is the Origin?
The **origin (0,0)** is where the CNC machine begins cutting, it must align with the bottom-left corner of your physical copper board. All FlatCAM layers must be aligned to this same origin.

---

## How to Align Files to Origin in FlatCAM

### ✅ Move All Layers Together:
> ⚠️ **Important**: All jobs (copper, drill, cutout) must be moved to origin **at the same time**. If moved separately, they may become misaligned due to different offsets or rounding errors.

### Step-by-Step:
1. Select **all imported files** (hold Ctrl and click Bottom Copper, Drill, Outline)
2. Go to the **Selected** tab
3. Click **Move** button in toolbar

---

## ⚠️ Tips
- If files are not moved together, drill holes and traces will not align correctly.
- You can simulate each G-code file in Candle before cutting to verify alignment.
- Make sure to never shift your board once probing is done.

---

📎 Return to:
- [Isolation Routing](./isolation_routing.md)
- [Drilling Process](./drilling.md)
- [Cutout Job](./cutout.md)
- [Candle Execution](./candle.md)
