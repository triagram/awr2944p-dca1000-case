# AWR2944PEVM + DCA1000 enclosure

English | [简体中文](README.zh-CN.md)

A 3D-printed PLA case for a TI AWR2944PEVM radar board and a DCA1000EVM capture card.
The front guard stays on while you measure.

![The assembled case and the assembly order](images/overview.png)

This is v2.0. The latest version is on the `main` branch; every version is a git tag with its own
files and instructions, and the tag message says what changed.

## What it is

- The two boards stand one behind the other: the DCA1000 at the back, resting on 4 posts;
  the radar board in front, antenna facing out. They are 20 mm apart.
- Case 138 × 141 × 56 mm (width × height × depth), plus a 2.3 mm rail along the front of the floor;
  on the desk foot about 150 × 146 × 120 mm.
- Front guard: a 74 × 42 mm antenna window open to the right, and a 45 × 37 mm window on the left over
  the DCA1000 status LEDs. Two hand knobs hold the top left and the lower edge sits behind the rail.
- Every screw ends in a steel nut: no thread is cut in plastic.
- Cooling: 18 slots in the back, 8 in the top, 8 intake slots in the guard.
- Tripod: take the desk foot off; a 1/4"-20 nut in the floor takes the tripod screw.

## Files

| Folder | Content |
| --- | --- |
| `stl/` | print files, already in print orientation |
| `stl/test_fit/` | optional dummy boards for a test fit |
| `images/` | figures used in this README |

## Print

| File | Print | Notes |
| --- | --- | --- |
| `stl/body.stl` | 1 | |
| `stl/front_guard.stl` | 1 | |
| `stl/knob_x2.stl` | 2 | 4 walls, 100 % infill |
| `stl/spacer_x3.stl` | 3 | 4 walls, 100 % infill |
| `stl/collar_x3.stl` | 3 | 4 walls, 100 % infill |
| `stl/desk_foot.stl` | 1 | not needed if the case only goes on a tripod |
| `stl/test_fit/*.stl` | 1 each | optional; each board is two halves, stacked flat face to flat face |

All files are already in print orientation: print them as imported, without rotating.

Settings (made for a Bambu Lab A1 with a 0.4 mm nozzle):

- 0.20 mm layers. Keep this height: the bridging steps above the nut slots in the spacers and in the
  two bosses of the case are sized for it.
- 3 walls, 15 % infill, no supports, no brim; small parts 4 walls, 100 % infill.
- Print the small parts first and try the nuts: if a nut slides into a spacer slot, it also fits the
  slots in the case.

## Hardware

- M3×20 countersunk × 9: 4 from the back, 3 for the radar board (with the collars), 2 in the knobs.
- M3×10 pan head × 4: desk foot.
- M3 nut × 15: 4 in the floor, 1 on the fourth DCA1000 hole, 2 in the knobs, 2 in the bosses at the top
  left of the case, 2 in each of the 3 spacers.
- 1/4"-20 UNC hex nut × 1, optional, for a tripod (11.1 mm across flats).
- 12 mm self-adhesive rubber feet × 4, optional, under the desk foot.

Also needed: the two boards and the 60-pin ribbon cable from the DCA1000 kit. The only tool is a
screwdriver that fits the countersunk screws.

## Assembly

![How the boards and the front guard are fastened](images/fastening.png)

### Preparation (once)

![New features inside the case body](images/body_inside.png)

![The hand knob](images/knob.png)

1. Knobs × 2: push an M3×20 into the knob from the side with the cone, put an M3 nut in the hex pocket
   on the other side and tighten with a screwdriver. Screw and knob then turn as one, with the screw
   sticking out about 14 mm.
2. Spacers × 3: push an M3 nut into each of the two side slots, all the way in. Looking down the hole
   from the top, the two nut holes line up.
3. The two bosses at the top left of the case: push an M3 nut into each from its side slot (the left
   boss opens to the right, the right boss to the left). This can also be done after the boards are in.
4. Floor nuts and desk foot: drop 4 M3 nuts into the 4 small hex pockets inside the floor (and the
   1/4" nut into the large middle pocket for a tripod), then drive 4 M3×10 from below through the foot
   into them. Do this before any board goes in: the rear pockets are out of reach afterwards.
5. Remove the metal feet TI fitted to the radar board: they take two of its mounting holes.

### Steps

The case stands on the desk with its opening toward you.

1. DCA1000: components toward you, 5 V jack on the left; stand it in. It sits on the two bottom ledges,
   and leaning back on the 4 posts puts the 4 holes in place.
2. Lower left, lower right and upper left holes: hold a spacer on the hole with one hand (thick end on
   the board, slots facing left or right), and with the other push an M3×20 through from the back
   until it catches the lower nut and the spacer sits tight on the board. Stop when it gets tight.
3. Upper right hole (the radar board has no hole there): an M3×20 from the back into an M3 nut held on
   the front of the board.
4. Radar board: antenna toward you, CAN terminal at the bottom, onto the necks of the 3 spacers. Put a
   collar on each hole (cone outward) and drive an M3×20 into the upper nut until the collar clamps the
   board. If the screw stops before the collar is tight, it has met the back screw (a collar is missing
   or the screw is longer than 20 mm): do not force it.
5. Ribbon cable: DCA1000 J3 to radar J7 (lower left on its front).
6. Cables: radar 12 V (J12) and XDS USB (J8) on the right, radar FTDI USB (J10) through the upper left
   window, DCA1000 5 V through the left window, Ethernet through the right cut-out.
7. Front guard, below.

Spacer orientation: keep the two long flats on the spacer level, so the slots open sideways. The nuts
cannot drop out, and at the upper left hole the spacer passes between the connector blocks of the
dummy radar board. With the real board any rotation fits.

If the boards keep tipping forward in steps 1 and 2, put a 1 to 2 cm book under the front edge of the
desk foot so the case leans back.

### Front guard

1. LED window on the left, the two holes at the top left, ribs inward. Hold the guard about 2 mm above
   its final position against the front, then slide it down: the bevelled lower edge drops behind the
   rail.
2. Screw in the two knobs, about 6 turns each, hand tight.

To take the guard off, unscrew the knobs, lift the guard 2 mm and take it away. With the knobs out,
the two boss nuts only sit in their slots and can slide out if the case lies on its side; a piece of
tape over the slots keeps them in. If a knob spins without tightening, tighten the screw inside it
again, or add a drop of cyanoacrylate glue.

## License

Copyright Mengyuan Liu 2026.

The hardware design files (`stl/`) describe Open Hardware and are licensed under the CERN-OHL-P v2.
You may redistribute and modify them and make products using them under the terms of the CERN-OHL-P v2
([LICENSE](LICENSE), https://ohwr.org/cern_ohl_p_v2.txt). They are distributed WITHOUT ANY EXPRESS OR
IMPLIED WARRANTY, INCLUDING OF MERCHANTABILITY, SATISFACTORY QUALITY AND FITNESS FOR A PARTICULAR
PURPOSE. Please see the CERN-OHL-P v2 for applicable conditions.

Source location: https://github.com/triagram/awr2944p-dca1000-case

The documentation and images are licensed under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## References

- TI design files for the board outlines, holes, components and LEDs:
  [DCA1000EVM (SPRR350)](https://www.ti.com/lit/zip/SPRR350),
  [AWR2944EVM (SPRR440)](https://www.ti.com/lit/zip/SPRR440),
  [AWR2944PEVM (SPRR507)](https://www.ti.com/lit/zip/SPRR507).
