# AWR2944PEVM + DCA1000 enclosure

English | [简体中文](README.zh-CN.md)

A 3D-printed PLA case for a TI AWR2944PEVM radar board and a DCA1000EVM capture card.

![The assembled case and the assembly order](images/overview.png)

This is v1.0, the first version. The latest version is on the `main` branch; every version is a git
tag with its own files and instructions, and the tag message says what changed.

## What it is

- The two boards stand one behind the other: the DCA1000 at the back, on 4 posts 15 mm high;
  the radar board in front, antenna facing out. They are 20 mm apart.
- Case 138 × 141 × 56 mm (width × height × depth); on the desk foot about 150 × 146 × 120 mm.
- Next to the antenna the right wall only reaches the back of the radar board, and above the antenna
  the top wall reaches only 5.4 mm past the antenna face, so the walls stay out of the antenna's view.
- A transport lid covers the front for carrying; it comes off before measuring.
- Expansion bay at the top left: about 40 × 38 mm, with 4 × 3 holes of 3.2 mm (10 mm pitch) in the
  back and a 26 × 18 mm cable exit in the left wall.
- Tripod: take the desk foot off; a 1/4"-20 nut in the floor takes the tripod screw.

## Files

| Folder | Content |
| --- | --- |
| `stl/` | print files, already in print orientation |
| `stl/test_fit/` | optional dummy boards for a test fit |
| `step/` | STEP model of the case body, for editing in CAD |
| `images/` | figures used in this README |

## Print

| File | Print | Notes |
| --- | --- | --- |
| `stl/body.stl` | 1 | |
| `stl/desk_foot.stl` | 1 | not needed if the case only goes on a tripod |
| `stl/transport_lid.stl` | 1 | |
| `stl/spacer_x3.stl` | 3 | 4 walls, 100 % infill |
| `stl/test_fit/*.stl` | 1 each | optional dummy boards, see below |

All files are already in print orientation: print them as imported, without rotating.

Settings (made for a Bambu Lab A1 with a 0.4 mm nozzle): 0.20 mm layers, 3 walls, 15 % infill,
no supports, no brim; the spacers 4 walls, 100 % infill. Print the small parts first.

**Dummy boards.** Each real board has parts on both sides, so a one-piece dummy would need supports.
Each dummy is therefore split through the middle of the PCB: every half is a 0.8 mm plate with the
parts of one side, printed flat side down. Stack the two halves flat face to flat face, with the
mounting holes aligned and the lettered sides out; together they are 1.6 mm, as thick as the real
board. No glue is needed: the M3 screws through the mounting holes clamp both halves. The dummies only
model parts taller than 1.4 mm, and their holes are 0.2 mm larger than the real ones.

**Spacers.** The two boards must be 20 mm apart (at least 18.5 mm, or the radar board's Ethernet
jack hits the DCA1000). The printed spacer stands between them, 3 in total. It has a 2.8 mm core hole,
and the M3 screws cut their own thread in it from both ends. The TI plastic standoffs can replace it
if they have an M3 female thread and are 19 to 21 mm long.

## Hardware

- M3×25 pan head × 4 with flat washers × 4: from the back, through the posts and the DCA1000 into the
  spacers.
- M3 nut × 1: the fourth DCA1000 hole at the upper right (the radar board has no hole there).
- M3×8 pan head × 3: the radar board onto the spacers, from the front.
- M3×10 pan head × 4 with M3 nuts × 4: desk foot.
- 1/4"-20 UNC hex nut × 1, optional, for a tripod (11.1 mm across flats).
- 12 mm self-adhesive rubber feet × 4, optional, in the shallow recesses under the desk foot.

Also needed: the two boards and the 60-pin ribbon cable from the DCA1000 kit.

## Assembly

Test-fit with the dummy boards first, then fit the real boards. Before fitting the real radar board,
remove the metal feet TI fitted to it: they take two of its mounting holes.

1. Drop the 4 M3 nuts and the 1/4" nut into the hex pockets in the floor, from inside the case.
   Do this before any board goes in.
2. Fix the desk foot with 4 M3×10 from below.
3. DCA1000: components toward the front of the case, 5 V jack on the left, onto the 4 posts.
4. From the back, put the 4 M3×25 with washers through the posts and the DCA1000. On the front, screw
   a spacer onto the lower left, lower right and upper left screws, and an M3 nut onto the upper right
   one.
5. Radar board: antenna toward the front, CAN terminal at the bottom, onto the 3 spacers; fix it with
   3 M3×8.
6. Ribbon cable: DCA1000 J3 to radar J7 (lower left on its front).
7. Cables: radar 12 V (J12) and XDS USB (J8) on the right; radar FTDI USB (J10) through the upper left
   window; DCA1000 5 V through the left window; Ethernet through the right cut-out.
8. Put the transport lid on for carrying and take it off before measuring: it must not sit in front of
   the antenna.

## License

Copyright Mengyuan Liu 2026.

The hardware design files (`stl/`, `step/`) describe Open Hardware and are licensed under the
CERN-OHL-P v2. You may redistribute and modify them and make products using them under the terms of
the CERN-OHL-P v2 ([LICENSE](LICENSE), https://ohwr.org/cern_ohl_p_v2.txt). They are distributed
WITHOUT ANY EXPRESS OR IMPLIED WARRANTY, INCLUDING OF MERCHANTABILITY, SATISFACTORY QUALITY AND
FITNESS FOR A PARTICULAR PURPOSE. Please see the CERN-OHL-P v2 for applicable conditions.

Source location: https://github.com/triagram/awr2944p-dca1000-case

The documentation and images are licensed under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## References

- TI design files for the board outlines, holes and components:
  [DCA1000EVM (SPRR350)](https://www.ti.com/lit/zip/SPRR350),
  [AWR2944EVM (SPRR440)](https://www.ti.com/lit/zip/SPRR440),
  [AWR2944PEVM (SPRR507)](https://www.ti.com/lit/zip/SPRR507).
