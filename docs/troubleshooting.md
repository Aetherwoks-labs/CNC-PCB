# Common Issues & Fixes

This guide covers frequent problems encountered during CNC PCB milling and how to resolve them.

---

## ❌ Isolation Issues
| Problem                           | Cause                                  | Fix                                  |
|----------------------------------|----------------------------------------|--------------------------------------|
| Traces still connected           | Depth too shallow, uneven board        | Increase cut depth, re-probe Z       |
| Isolation skips or lines missing| Bad heightmap, bit too fast            | Redo probing, lower feedrate         |
| Copper slivers remain            | Tool too small for spacing             | Use multiple passes or wider bit     |

---

## 🕳️ Drill Misalignment
| Problem              | Cause                          | Fix                                    |
|---------------------|-------------------------------|----------------------------------------|
| Holes off-center    | XY origin mismatch            | Move all files to origin in FlatCAM at the same time   |
| Depth too shallow   | Incorrect Cut Z or loose bit  | Recheck Z-zero, tighten bit            |
| Bit breaks          | Too long or thin for depth    | Use shorter bits, reduce feedrate      |

---

## ✂️ Cutout Problems
| Problem                | Cause                          | Fix                                      |
|-----------------------|-------------------------------|------------------------------------------|
| Board moves during cut| No tabs, weak hold            | Add tabs, use better tape/clamps         |
| Incomplete cut        | Not enough depth or passes    | Increase Cut Z or use more passes        |
| Bit chatter or noise  | Dull bit, high feedrate       | Use new bit, reduce feedrate             |

---

## ⚙️ Machine/Probing Errors
| Problem              | Cause                        | Fix                                      |
|---------------------|------------------------------|------------------------------------------|
| Probe not triggering| Loose wire, bad clip contact | Confirm continuity, clean copper         |
| Heightmap incorrect | Board warped, bad grid       | Use finer grid, re-tape board            |
| Bit skips Z motion  | Probe feedrate too fast      | Lower to 10–15 mm/min                    |

---

Return to: [Example Projects](../examples/)
