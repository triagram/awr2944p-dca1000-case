# AWR2944PEVM + DCA1000 enclosure

English | [简体中文](README.zh-CN.md)

A 3D-printed PLA case for a TI AWR2944PEVM radar board and a DCA1000EVM capture card.
The front guard stays on while you measure.

This is v3.0. The latest version is on the `main` branch; every version is a git tag with its own
files and instructions, and the tag message says what changed.

## What it is

- The two boards stand one behind the other: the DCA1000 at the back, resting on 4 posts;
  the radar board in front, antenna facing out. They are 20 mm apart.
- Case 138 × 141 × 56 mm (width × height × depth); on the desk foot about 150 × 146 × 120 mm.
- Front guard: a 74 × 42 mm antenna window open to the right, so nothing sits in the antenna beam,
  and a 45 × 37 mm window on the left over the DCA1000 status LEDs. Two hand knobs hold the top left,
  two clips hook inside the right wall, and the lower edge sits behind a rail on the case.
- Cooling: 18 slots in the back, 8 in the top, 8 intake slots in the guard.
- Tripod: take the desk foot off; a 1/4"-20 nut in the floor takes the tripod screw.

## Files

| Folder | Content |
| --- | --- |
| `stl/` | print files, already in print orientation |
| `stl/test_fit/` | optional dummy boards for a test fit |
| `images/` | figures used in the design notes |
| `design/` | why the case is built this way |

## Print

| File | Print | Notes |
| --- | --- | --- |
| `stl/body_pause_at_47.00mm.stl` | 1 | pause at 47.00 mm to drop in two M3 nuts, see below |
| `stl/front_guard.stl` | 1 | |
| `stl/knob_x2.stl` | 2 | 4 walls, 100 % infill |
| `stl/spacer_x3.stl` | 3 | 4 walls, 100 % infill |
| `stl/desk_foot.stl` | 1 | not needed if the case only goes on a tripod |
| `stl/test_fit/*.stl` | 1 each | optional; each board is two halves, stacked flat face to flat face |

All files are already in print orientation: print them as imported, without rotating.

Settings (made for a Bambu Lab A1 with a 0.4 mm nozzle):

- 0.20 mm layers. Keep this height: the bridging steps above the nut pockets and the spacer slots
  are sized for it.
- 3 walls, 15 % infill, no supports, no brim; knob and spacer 4 walls, 100 % infill.
- Plain PLA. No silver, metal-filled or carbon-filled filament: the guard and the right wall sit
  next to the antenna.
- Print the spacers first. If an M3 nut slides into a spacer slot, the nuts are the right size.

### Print pause in the case body

1. After slicing, move the layer slider to the 47.00 mm layer (layer 235 at 0.20 mm, the first layer
   above the two nut pockets) and add a pause there. With another layer height, pause at the first
   layer above 46.8 mm.
2. When the printer stops, a hex pocket is open on top of each of the two bosses at the top left.
   Drop an M3 nut flat into each and turn it until it falls in.
3. Resume. The next layers close over the nuts, so they cannot fall out when the knobs come off.
   A faint line may show on the outer wall at that layer.

Save the sliced project with the pause as a `.3mf` and print from it next time.

## Hardware

- M3×20 countersunk × 6: 4 from the back, 2 in the knobs. Countersunk screws are measured
  including the head; check with calipers that they are 19.5 to 20.5 mm overall, since labels
  are often wrong and a longer screw runs into the next one.
- M3×12 pan head × 7: 3 for the radar board, 4 for the desk foot. Pan head means any head that sits
  on top (round, pan or cheese head), measured from under the head.
- M3 nut × 15: 4 in the floor, 1 on the fourth DCA1000 hole, 2 in the knobs, 2 sealed into the case
  at the print pause, 2 in each of the 3 spacers.
- 1/4"-20 UNC hex nut × 1, optional, for a tripod (11.1 mm across flats).
- 12 mm self-adhesive rubber feet × 4, optional, under the desk foot.

Also needed: the two boards and the 60-pin ribbon cable from the DCA1000 kit. The TI plastic standoffs
are not used: the boards must be 20 mm apart, or the radar board hits the guard and the side openings
no longer line up.

## Assembly

The case stands on the desk with its opening toward you. Step 1 must come before any board goes in.

### Step 0: prepare the small parts (once)

1. Knobs × 2: push an M3×20 countersunk into the knob from the side with the cone, put an M3 nut in
   the hex pocket on the other side and tighten with a screwdriver. Screw and knob then turn as one,
   with the screw sticking out about 14 mm.
2. Spacers × 3: push an M3 nut into each of the two side slots, all the way in. Looking down the hole
   from the thin end, the two nut holes line up.
3. Remove the metal feet TI fitted to the radar board: they take two of its mounting holes.

### Step 1: nuts in the floor, then the desk foot

1. Drop 4 M3 nuts into the 4 small hex pockets inside the floor, all the way down. For a tripod,
   put the 1/4" nut into the large pocket in the middle.
2. Stand the case on the desk foot and drive 4 M3×12 from below through the foot into the nuts.
   The heads sit in the counterbores under the foot.
3. To reach from below, slide the case over the edge of the desk so the corner you are working on
   sticks out, or tape over the pockets and turn the case upside down.

The two rear pockets are behind the DCA1000 once it is in, which is why this step comes first.

### Step 2: DCA1000

1. Set the DCA1000 DIP switches first (TI SPRUJ22C, section 2.9); it is easiest before the board
   goes in.
2. Components toward you, 5 V jack on the left, Ethernet on the right: stand the board in. Its lower
   edge sits on the two bottom ledges, the ledges on the left, top and right line it up, and leaning
   back on the 4 posts puts the 4 holes in place.
3. If the board keeps tipping forward, put a 1 to 2 cm book under the front edge of the desk foot so
   the case leans back.

### Step 3: spacers and the 4 back screws

Spacers go on the lower left, lower right and upper left holes. The upper right hole only takes a
screw and a nut: the radar board has no hole there.

1. Hold a spacer on the hole with one hand: flat end on the board, thin tip toward you, slots facing
   left and right with the two flats level, so the nuts cannot drop out. This also holds the board.
2. With the other hand, push an M3×20 countersunk through from the back and turn it until the spacer
   sits tight on the board. Stop as soon as it gets tight: the spacer is PLA.
3. Upper right hole: an M3×20 countersunk from the back into an M3 nut held on the front with pliers.

With the dummy boards, place the upper left spacer exactly as in point 1: the dummy's connector block
is wider than the real one and only clears in that orientation.

### Step 4: radar board

1. Set the radar board SOP jumpers first (TI SPRUJ22C, section 2.9).
2. Antenna toward you, blue CAN terminal at the bottom, antenna at the upper right: place the board on
   the 3 spacers.
3. Drive one M3×12 pan head through each hole into the upper nut of the spacer and stop when the head
   clamps the board. Do not use an M3×20 here: it would run into the back screw.

### Step 5: ribbon cable and the other cables

1. Ribbon cable: one end into DCA1000 J3 (outside the left edge of the radar board), the other into
   radar J7 (lower left on its front). Let the spare length bulge to the left, beside the radar board,
   not over it.
2. The other cables enter through the side walls:

   | Cable | Plugs into | Enters through |
   | --- | --- | --- |
   | 5 V supply | DCA1000 J2 | left wall, lower rear window |
   | micro USB to the PC | radar FTDI port J10 | left wall, upper front window (not the rear one) |
   | Ethernet to the PC | DCA1000 J6 | right wall, middle rear cut-out |
   | 12 V supply | radar J12 | right wall, lowest front window |
   | USB, optional | radar XDS110 port J8 | right wall, front notch |

3. Connect power first, then USB: TI notes that plugging USB in first can hold the board in reset.
4. To unplug the Ethernet cable, press its latch with a finger through the cut-out on the right of
   the back.
5. Cable ties through the slits low on both side walls keep the cables from pulling on the connectors.

The radar Ethernet port J9 and the two DCA1000 micro USB ports also have openings, but TI's capture
setup does not use them.

### Step 6: front guard

1. LED window on the left, the two holes at the top left, ribs and clips inward. Hold the guard about
   2 mm above its final position and press it flat on the front: the two clips on the right drop into
   the entry slots inside the right wall. Slide it down: the bevelled lower edge drops behind the rail
   and the clips slide under the slot edges.
2. Screw in the two knobs, about 6 turns each, hand tight.

To take the guard off, unscrew the knobs, push the guard up 2 mm so the clips come back to the entry
slots, and lift it away. The DIP switches, jumpers and CAN terminal are all on the front of the boards
and reachable with the guard off.

If a knob spins without tightening, tighten the screw inside it again, or add a drop of
cyanoacrylate glue.

### Tripod

Remove the 4 screws and the desk foot, then screw the tripod or quick-release plate into the 1/4" nut
in the middle of the floor. The 4 M3 nuts stay in their pockets while the case stands upright.

## Design notes

- [design/radar-assessment.md](design/radar-assessment.md): whether the case blocks or reflects the
  antenna beam, and why the right wall ends in a vertical drop.

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
- [AWR2944EVM / AWR2944PEVM user guide (SPRUJ22C)](https://www.ti.com/lit/ug/spruj22c/spruj22c.pdf):
  connector names, the switch and jumper settings for the DCA1000 (section 2.9).
